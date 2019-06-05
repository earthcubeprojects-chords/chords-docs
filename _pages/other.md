---
layout: single
title: Other
permalink: /gettingstarted/other/
classes: wide
---

A few recommendations include [Google Engine](https://cloud.google.com/cloud-services-platform/){:target="_blank"}, [Linode](https://www.linode.com/pricing){:target="_blank"}, [Vultr](https://www.vultr.com/pricing/){:target="_blank"}.

Recommended CHORDS Resources are
- At least 2 CPU’s
- 1 sample every 10 seconds data rates

Data are like music notes. If you try to play every single note at the same time you’ll run into problems. You couldn’t possibly play every note, unless you have extra hands, then kudos to you and play on, you would struggle to play the instrument at all. The same idea applies to your data, if you try to upload all your individual data points at the same exact time your system will likely freeze up. However, if you stagger your data to one after the other then your download will proceed smoothly. 

Future updates for CHORDS will include bulk upload, putting all the music notes onto a sheet of paper and then sending them. For example, if you have 10 instruments uploading data at 00:00:00, each request/url uses a request handler on the CHORDS backend. The number of these handlers is configured in *chords_control*, but the optimal number depends on the system resources available in your particular environment. If your instrument data uploads all hit at the exact same time and consume all the request handlers, your portal can briefly become unresponsive. Likewise if you have multiple simultaneous downloads of data. If data are staggered (00:00:00, 00:00:01, 00:00:02, etc) then you could likely go down to data rates of 5 seconds or less. If you truly wish to go lower it is recommended not to use a VM but hardware to speed up your data rate. We have run a couple instruments at 1s intervals in AWS with t2.medium or larger instances. 

Once you have your own server checkout [Run CHORDS Locally]({{site.baseurl}}/gettingstarted/os/) to set up CHORDS.


