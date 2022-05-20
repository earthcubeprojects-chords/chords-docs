---
layout: single
title: Install CHORDS For Various Operating Systems
permalink: /gettingstarted/os/
classes: wide
---

<div id="tabs">
  <ul>
    <li><a href="#tabs-Ubuntu">Ubuntu</a></li> <!-- Using JqueryUI to set names and colors on the tabs -->
    <li><a href="#tabs-RHEL">RHEL & Centos</a></li>
    <li><a href="#tabs-Macos">Mac</a></li>
    <li><a href="#tabs-W10">W10</a></li>
  </ul>

  <div id="tabs-Ubuntu"> <!-- content under tab -->
  <div id="ub" class="tab-pane active">
  {% highlight sh %}
  sudo -i
  apt-get install docker.io docker-compose git python-pip
  {% endhighlight %}
  {% include chords_control.md %}
  </div>
  </div>

  <div id="tabs-RHEL"> <!-- content under tab -->
  <div id="centos7" class="tab-pane">
  {% highlight sh %}
  sudo -i # Or 'su -' if you do not have sudo privileges
  yum -y install epel-release
  yum -y install docker docker-compose
  yum -y install git
  yum -y install python3-pip
  systemctl enable docker
  systemctl start docker
  {% endhighlight %}
  {% include chords_control.md %}
  </div>
  </div>

  <div id="tabs-Macos"> <!-- content under tab -->
  <div id="macos" class="tab-pane">
  <ol>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/jR_XToKChYI" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

  <li>Make sure you have Python 3 for Mac</a>.</li>
  <li>Verify that python is working:
  {% highlight python %} 
  python3
  Python 3.9.12 (main, Mar 26 2022, 15:51:15)  
  [Clang 13.1.6 (clang-1316.0.21.2)] on darwin
  Type "help", "copyright", "credits" or "license" for more information.
  >>> quit()
  {% endhighlight %}
  </li>
  <li>Install <a href="https://docs.docker.com/v17.09/docker-for-mac/install/">Docker for Mac</a>.</li>
  <li>Run Docker. Configure its preferences to start Docker automatically. </li>
  <li>Note when you see the whale in the menu bar (upper right corner of your screen) docker is up and running!</li>
  <li>Open a command window, and verify that docker is working:
  {% highlight sh %} 
  docker run hello-world
  Hello from Docker!
  This message shows that your installation appears to be working correctly.
  ...
 {% endhighlight %} </li>
  <li>Then in a terminal window:
  {% highlight sh %}
  mkdir chords
  cd chords

  # Fetch the control script:
  pip3 install sh
  curl -O -k https://raw.githubusercontent.com/earthcubeprojects-chords/chords/development/chords_control

  # Make sure the "future" module is installed
  pip3 install future

  # Initial installation:
  python3 chords_control --config
  python3 chords_control --update

  # To run CHORDS:
  python3 chords_control --run

  # To stop CHORDS:
  python3 chords_control --stop

  # To reconfigure and update:
  cd chords
  curl -O -k  https://raw.githubusercontent.com/earthcubeprojects-chords/chords/development/chords_control
  python3 chords_control --config
  python3 chords_control --update
  python3 chords_control --stop
  python3 chords_control --run
  {% endhighlight %} 
  </li>
  <li> Once the above script has been run all you need to do to start chords on your computer again is open the terminal and type </li>
  {% highlight sh %}
  cd chords
  python3 chords_control -- run
  {% endhighlight %}

  </ol>
  Now point your browser at the IP of the the system. <strong>localhost</strong>
  will often work as the IP, if the browser is on the same system.
  <strong>Be sure to use http:// (not https://)</strong>.
  </div>
  </div>

  <div id="tabs-W10"> <!-- content under tab -->
  <ol>
  <li>Open a command window and create a directory for chords files. The name and location are not important, but we suggest that you name it 'chords', and create it in your home directory.</li>
  {% highlight sh %}
  mkdir chords
  {% endhighlight %}

  <li>Download  and extract <a href="https://curl.haxx.se/windows/" target="_blank">curl</a>. Copy the files (curl.exe, etc.) in the 'curl.xxx/bin/' directory to your chords directory. For help with curl, visit this <a href="https://www.youtube.com/watch?v=8f9DfgRGOBo">video</a>.</li>

  <li>Download the <a href="https://www.python.org/ftp/python/2.7.16/python-2.7.16.amd64.msi">Windows python3 2 installer</a>. Double click on the downloaded .msi file to install it.</li>

  <li>Add Python3 paths to the Path environment variable. Hints:
  <ul>
    <li>Open the Start Search, type in “env”, and choose “Edit the system environment variables”</li>
    <li> Click the “Environment Variables…” button.</li>
    <li>Under the "User Variables” section (the upper half), find the row with “Path” in the first column. Click "Edit". “Edit environment variable” will appear.</li>
    <li>Select "New", and enter the Python3 directory. This will usually be C:\Python27.</li>
    <li>Select "New", and enter the Python3 scripts directory. This will usually be C:\Python27\scripts.</li>
    <li>Save your changes</li>
  </ul>
  </li>

  <li>Verify that python is working:
  {% highlight python %} 
  python3
  Python 3.9.7 (tags/v3.9.7:1016ef3, Aug 30 2021, 20:19:38) [MSC v.1929 64 bit (AMD64)] on win32
  Type "help", "copyright", "credits" or "license" for more information.
  >>> quit()
  {% endhighlight %}
  </li>

  <li>Install <a href="https://docs.docker.com/docker-for-windows/install/" target="_blank">Docker Desktop for Windows</a>. (You will be required to create a free docker hub account, and log into it.)</li>

  <li>Run the Docker Desktop. It may take a minute to start up.</li>

  <li>Open a command window, and verify that docker is working:
  {% highlight sh %} 
  docker run hello-world
  Hello from Docker!
  This message shows that your installation appears to be working correctly.
  ...
 {% endhighlight %} </li>

  <li>Install CHORDS from the command window:
  {% highlight sh %}
  cd chords

# Fetch the control script:
curl -O -k https://raw.githubusercontent.com/earthcubeprojects-chords/chords//development/chords_control

# Initial installation:
python3 chords_control --config
python3 chords_control --update

# To run CHORDS:
python3 chords_control --run

# To stop CHORDS:
python3 chords_control --stop

# To reconfigure and update:
cd chords
python3 chords_control --renew
python3 chords_control --config
python3 chords_control --update
python3 chords_control --stop
python3 chords_control --run
  {% endhighlight %} 
  </li>
  <li> Once the above script has been run all you need to do to start chords on your computer again is open the terminal and type </li>
  {% highlight sh %}
  cd chords
  python3 chords_control -- run
  {% endhighlight %}
  </ol>
Now point your browser at the IP of the the system. <strong>localhost</strong>
will often work as the IP, if the browser is on the same system.
<strong>Be sure to use http:// (not https://)</strong>.
  </div>
</div>
<br>
When you first start up your CHORDS portal don't panic if you get **502** error. It's a good sign!
<a href = "{{ site.baseurl }}/assets/images/goodError.png"><img class="img-responsive" src="{{ site.baseurl }}/assets/images/goodError.png"></a>
Just hit refresh on your browser until your portal shows up.
<a href = "{{ site.baseurl }}/assets/images/CHORDS success.png"><img class="img-responsive" src="{{ site.baseurl }}/assets/images/CHORDS success.png"></a>
See the [detailed instructions]({{site.baseurl}}/gettingstarted/os/control/) if the Quick Start recipes are not adequate
to get your portal running, and for additional information.
<script>
$("#tabs").tabs();
</script>

<!--## Once your portal is running visit [portal configuration]({{site.baseurl}}/admin/) to continue setting up your portal.-->
[Continue to Portal Configuration]({{site.baseurl}}/admin/){: .btn .btn--info}
