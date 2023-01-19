---
layout: single
title: Create an AWS Portal
permalink: /gettingstarted/create/
toc: true
toc_sticky: true
toc_label: "Table of Contents"
toc_icon: "cog"

---

If someone else has already created a Portal for you, you can skip Portal creation. Just point
your browser at the new Portal and perform the initial login as user: <em>admin@chordsrt.com</em>, 
password: <em>realtimedata</em>. You will be prompted to change the password during this first login.
You can then proceed to [Site configuration]({{site.baseurl}}/portalconfig).

The Portal runs as a standalone web server on Amazon Web Services (AWS). 
The interface to AWS can seem a bit overwhelming (currently offering 52
services!).

We use the **AWS CloudFormation** service to create a new portal. The steps are
simple.

<!--Gallery of picture instructions. This can be moved anywhere.-->
<!-- {% include gallery %} -->


Go ahead and log into your AWS account in your browser. We will come back to it shortly.
## 1. Fetch the CloudFormation template

CloudFormation uses a template file, which you need to get from the
CHORDS GitHub project. A simple way to do this is just to cut and paste the
text from your browser, into a local file on your computer.

In a new browser tab, open the CloudFormation [template file](https://raw.githubusercontent.com/earthcubeprojects-chords/chords/development/bin/cloud_formation/chords_cf_template.yml){:target="_blank"}.

Copy and paste the text into a local file named `chords_cf_template.yml` on your computer. It's
a long file, so be sure to scroll all of the way to the bottom and copy all of the text.

## 2. Run CloudFormation

* First click on <em>“Services”</em> and then click on <em>“Cloud Formation”</em> 
<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step1.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step1.png"></a> <!--Using liquid to set path for images.-->
</figure>      

## 3. Start stack creation and upload the template 
<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step2.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step2.png"></a><!--Using liquid to set path for images.-->
</figure>

* Click **Create new stack**

* Click on **Upload a template file** and then choose your local template file (`chords_cf_template.yml`) for uploading:
<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step3.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step3.png"></a><!--Using liquid to set path for images.-->
</figure>

* Click **Next**

## 4. Specify stack details

* Give the stack a name. The convention is _CHORDS-_ suffixed with your project or organization name, e.g. _CHORDS-CSURadar_.
* You will need to create a key pair for your Amazon account if you have not already done so. You can see instructions about how to do this on _Step 4_ of [Setting up your Amazon Account](http://ncar.github.io/chords/aws.html){:target="_blank"}.
Then select an EC2 KeyPair that you created for *KeyName*. This will allow you to ssh into the instance, if ever needed.

The `ChordsEmailAddress` and `ChordsEmailPassword` parameters are not required, but can be used to
specify an email account that can be used for email forwarding of password reset requests and grafana alerts.
Gmail is typically used for this. Since the email credentials are stored on this CHORDS server instance, 
**you really should create an email account to be used specifically and only for this purpose**.  
(Note: gmail will require you to allow insecure application access to the mail account, unlock Captcha, and finally
to authorize the CHORDS server when the first test email is sent from the CHHORDS admin account.
It can be tricky to get the email forwarding to work.)

For demonstrations and simple, low-bandwidth streaming feeds, select a _t2.micro_ instance type which are free
of charge for the first year. Otherwise, select a more capable instance. _t2.small_ provides good responsiveness
for sites with half a dozen instruments, and _t2.medium_ has succesfully hosted sites with 50 instruments, or those
with higher frequency (>1 Hz) data streams.

<figure>  
  <a href = "{{ site.baseurl }}/assets/images/Step4a.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step4a.png"></a><!--Using liquid to set path for images.-->
  <a href = "{{ site.baseurl }}/assets/images/Step4b.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step4b.png"></a><!--Using liquid to set path for images.-->
</figure>

* Hit **Next**

## 5. Configure stack options

* Click **Stack creation options**
* Rollback on failure: Disabled
* Termination protection: Enabled
<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step5.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step5a.png"></a><!--Using liquid to set path for images.-->
  <a href = "{{ site.baseurl }}/assets/images/Step6.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step5b.png"></a><!--Using liquid to set path for images.-->
</figure>

* Hit **Next**.

## 6. Review

* Verify that everything looks good and then click **Create Stack**
<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step7.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step7.png"></a><!--Using liquid to set path for images.-->
</figure>

## 7. Wait for the portal to be created
* After the creation has started, you will be taken 
to the stack summary page. Go to the *Events* tab to watch the progress 
of the stack creation. It usually takes about 6 minutes to complete, but it can take 
much longer (even 30 minutes), depending upon AWS performance.

<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step8.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step8.png"></a><!--Using liquid to set path for images.-->
</figure>

## 8. Accessing the new portal

Once your portal is created, select the **“Outputs”** tab.  **Click** on the URL to access your new portal.
<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step9.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step9.png"></a><!--Using liquid to set path for images.-->
</figure>

## 9. Log Into to Your Brand-New CHORDS Portal!

* Click on the **“Sign in”** 

<figure>
  <a href = "{{ site.baseurl }}/assets/images/Step10.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/Step10.png"></a><!--Using liquid to set path for images.-->
</figure>

Once the Portal is running, you will want to immediately change the admin acount and password to your
own email and password.

* Log into your new portal, as user: **admin@chordsrt.com**, and password: **realtimedata**
* Click on **Users**, then click on **admin@chordsrt.com**
* Click **Edit User**
* Change your email and then click **Change Password**
* Enter your new password and use **realtimedata** as your old password to confirm the change
* Click **Update**
 
# If something breaks
* If the provisioning fails, the instance will be stopped, and you probably won\'t know why :-). 
  Since the rollback was disabled, it may be possible to ssh into the portal in order to obtain
  some diagnostics related to the problem.

[Continue to Portal Configuration]({{site.baseurl}}/portalconfig/){: .btn .btn--info}
