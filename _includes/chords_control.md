 <!--Using Liquid to highlight syntax-->
{% highlight sh %}
mkdir -p /var/lib/chords
cd /var/lib/chords

# Fetch the control script:
pip3 install sh==1.14.3
curl -O -k https://raw.githubusercontent.com/earthcubeprojects-chords/chords/development/chords_control

# Initial installation:
python3 chords_control --config
python3 chords_control --update

# To run CHORDS:
python3 chords_control --run

# To stop CHORDS:
python3 chords_control --stop

# To reconfigure and update:
cd /var/lib/chords
python3 chords_control --renew
python3 chords_control --config
python3 chords_control --update
python3 chords_control --stop
python3 chords_control --run
{% endhighlight %}
Now point your browser at the IP of the the system. <strong>localhost</strong>
will often work as the IP, if the browser is on the same system.
<strong>Be sure to use http:// (not https://)</strong>.
