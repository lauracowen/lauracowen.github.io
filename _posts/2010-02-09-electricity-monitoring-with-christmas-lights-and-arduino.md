---
id: 443
title: Electricity monitoring with Christmas lights and Arduino
date: 2010-02-09T13:25:35+00:00
author: Laura
layout: post
guid: http://www.lauracowen.co.uk/blog/?p=443
permalink: /blog/2010/02/09/electricity-monitoring-with-christmas-lights-and-arduino/
tweet_this_url:
  - getnew
  - getnew
tmac_last_id:
  - "465491827059998720"
  - "465491827059998720"
dsq_thread_id:
  - "7699621188"
categories:
  - Making Things
  - Open Source
tags:
  - energy
  - geeky
  - Linux
---
This was my geeky Christmas project:

<iframe width="560" height="315" src="https://www.youtube.com/embed/7TL8Y9Y23mk" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


## What&#8217;s happening in the video&#8230;

The red/orange lights flash faster when the electricity usage in my house increase. The green/blue lights flash faster when the electricity usage in my Mum&#8217;s house increases (though in the video, the usage stays at a constant level so the lights don&#8217;t speed up).

Initially, the lights are flashing at the default reading of 1 kW. Then as the electricity usage levels vary, the red/orange lights start to flash out of sync with the green/blue lights. After a short time, though, I switch the kettle on (you can just about hear it in the background!) and you can see the red/orange lights start to flash a lot more quickly (as the kettle takes about 3 kW on top of whatever the current reading is). The lights slow down again as the kettle switches off.

## How does it work?

In my house I have a <a title="Current Cost website" href="http://www.currentcost.com" target="_blank">Current Cost</a> monitor, which reads the live power usage of the house and publishes it (using IBM messaging protocol <a title="MQTT.org website" href="http://mqtt.org" target="_blank">MQTT</a>) to a server on the Internet. An application on my laptop (to which my <a title="Arduino website" href="http://www.arduino.cc" target="_blank">Arduino</a> &#8211; small circuit board with a processor on it &#8211; is connected) subscribes to the readings in real time and passes the information to the Arduino. The Arduino does some calculations to convert the readings to speed of flashing so that the higher the reading, the faster the lights flash. The Arduino uses that speed calculation to control the relay switches connected to the Arduino, which in turn control the power to the lights &#8211; when the relay allows power to the lights, the lights come on; when the relay cuts the power to the lights, the lights go off, and so on.

This slideshow on Slideshare shows the overall connections between all the parts, and some pretty pictures:

<iframe src="//www.slideshare.net/slideshow/embed_code/key/9WDNbjvTiYp3om" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> <div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/lauracowen/arduino-christmas-lights-to-monitor-energy" title="Arduino Christmas Lights to Monitor Energy" target="_blank">Arduino Christmas Lights to Monitor Energy</a> </strong> from <strong><a href="https://www.slideshare.net/lauracowen" target="_blank">Laura Cowen</a></strong> </div>

**Update:**

This project got a brief mention in [an Imperica article](http://www.imperica.com/features/the-little-protocol-that-could): &#8220;A colleague of Piper has built a Christmas lights application using MQTT and Arduino, with the lights changing colour according to energy use in the house.&#8221;
