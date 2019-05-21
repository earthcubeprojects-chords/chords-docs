---
layout: single
title: How to Jetstream
permalink: /gettingstarted/jetstream/
# toc: true
# toc_sticky: true
# toc_label: "Table of Contents"
# toc_icon: "cog"
classes: wide
---
  
{% include video id="1fKdFjAQU8U" provider="youtube" %}

If you are working in academia then you are eligible to use a jetstream server.
You will need to submit a request for an allocation on the system.

If you are NSF funded you can create a jetstream instance for free and use the larger sizes without worry. Allocations are available to faculty members and researchers, including postdoctoral researchers, at a U.S.-based institution. Eligible institutions include federal research labs or commercial organizations; however, special rules may apply if your institution is not a university or a two- or four-year college. Investigators with support from any funding source, not just NSF, are encouraged to apply. You can still set up a Trial Access account but you won’t be able to use an account with the same resources as the amazon t1 server. 
For more information please visit
 [XSEDE](https://portal.xsede.org/allocations/startup#eligibility) to check their eligibility requirements.  

The trial resources include  

- 1000 Service Units (per cloud provider)
- 2 m1.tiny (1-core) OR 1 m1.small (2-core) Virtual Machine (VM) instance per cloud at a time
- 1 VM backup snapshot per instance,
- 1 small 10 GB disk external storage volume.

## How to enroll in the Jetstream Trial Allocation  

1. Go to the [XSEDE portal](https://portal.xsede.org) 

2. Click "Create Account" on the left side of your screen.
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamCreateAccount.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamCreateAccount.png"></a><!--Using liquid to set path for images.-->
</figure>

3. Fill out the form and click Submit. 

4. Upon receipt of the email notification click the link in the email to verify your account and set your username and password. 

5. Following account verification, if not already logged in, go to [https://portal.xsede.org/](https://portal.xsede.org/), click "Sign In" and sign in with the username and password set in the verification step.
You will be asked to read and accept the User Responsibilities form. This form outlines acceptable use to protect shared resources and intellectual property.

6. Click on "MyXSEDE" tab in the XSEDE User Portal
<figure>
  <a href ="{{ site.baseurl }}/assets/images/JetstreamMyXsede.png"> <img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamMyXsede.png"></a><!--Using liquid to set path for images.-->
</figure>

7. On the lower left side of your screen there is an area called **Trial Allocations**. Under it Click “Enroll”
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamEnroll.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamEnroll.png"></a>
</figure>  
This will take you to a page describing Trial Access and allowing you to Enroll or Unenroll in a Trial account.

8. Click the “Enroll Trial Access Button”  
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamTrialAccess.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamTrialAccess.png"></a>  <!--Using liquid to set path for images.-->
</figure>
A Successful Enrollment will show:
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamSuccess.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamSuccess.png"></a><!--Using liquid to set path for images.-->
</figure>
Wait approximately 4 hours for your allocation to propagate through the authentication system.

9. Once you’ve set up your account go to [Jetstream](https://use.jetstream-cloud.org/application/images)

10. Select XSEDE and hit continue 
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamOrganization.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamOrganization.png"></a><!--Using liquid to set path for images.-->
</figure>


11. Sign in with your XSEDE credentials
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamCredentials.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamCredentials.png"></a><!--Using liquid to set path for images.-->
</figure>
You are now in your jetstream account!

## Setting up Jetstream Image
Before you can get started with CHORDS you will need to get an Image running.
1. Click launch Image
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamImage.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamImage.png"></a><!--Using liquid to set path for images.-->
</figure>


2. Since you’re set up with a trial account you can use Matlab Minimal and it will cover your temporary needs.
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamMatlab.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamMatlab.png"></a><!--Using liquid to set path for images.-->
</figure>

3. Click Launch and a window will pop up
4. Enter your:
  - project name
  - your version (if  there are multiple versions)
  - Create new project
  - Select Indiana or TACC for your provider
  - Select your size (for trial accounts you will use a small or tiny size)
5. Go to your projects tab
6. Click on your project
<figure>
  <a href = "{{ site.baseurl }}/assets/images/JetstreamProject.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamProject.png"></a><!--Using liquid to set path for images.-->
</figure>

7. Click on the image you selected for your project
8. On the right side of your screen under “Links” click Open Web Shell 
<figure>
  <img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamShell.png"><!--Using liquid to set path for images.-->
</figure>

9. Follow  [Run CHORDS Locally]({{site.baseurl}}/gettingstarted/os/) instructions for Ubuntu.
10. Once you’ve finished the instructions go back to your Jetstream page.
11. Copy the IP address
<figure> 
  <a href = "{{ site.baseurl }}/assets/images/JetstreamIP.png"><img  class="img-responsive" src="{{ site.baseurl }}/assets/images/JetstreamIP.png"></a><!--Using liquid to set path for images.-->
</figure>

12. Paste it in your browser and your CHORDS instance will pop up.

You now have a CHORDS portal that can be accessed from any computer! Congratulations! Use your newfound power wisely.



