---
id: 918
title: 'Mosquitto and Facebook&#8230;and OggCamp'
date: 2011-08-17T18:36:10+00:00
author: Laura
layout: post
guid: http://www.lauracowen.co.uk/blog/?p=918
permalink: /blog/2011/08/17/mosquitto-and-facebook-and-oggcamp/
tweet_this_url:
  - getnew
  - getnew
tmac_last_id:
  - "465491802246492160"
  - "465491802246492160"
dsq_thread_id:
  - "7699620800"
categories:
  - Blogging, Twittering, etc
  - Open Source
  - Technology
tags:
  - cool!
  - Facebook
  - geeky
  - IBM
  - OggCamp
---
Roger Light (<a title="Roger's Twitter page" href="http://www.twitter.com/ralight" target="_blank">@ralight</a>) has just <a title="Roger's blog post" href="http://mosquitto.org/2011/08/facebook-using-mqtt/" target="_blank">posted on his blog</a> that Facebook are using MQTT for their new messaging system and, specifically, they seem to be using some part of <a title="Mosquitto website" href="http://mosquitto.org/" target="_blank">Roger&#8217;s Mosquitto project</a> in it.

So why is this a big deal to me?

Last weekend was the third OggCamp conference, <a title="OggCamp website" href="http://oggcamp.org" target="_blank">OggCamp 11</a>, at the Farnham Maltings in Surrey. Two years ago, at the first OggCamp (a one-day event at the Connaught Hotel in Wolverhampton), we invited Andy Stanford-Clark (<a title="AndySC on Twitter" href="http://www.twitter.com/andysc" target="_blank">@andysc</a>) to be our opening keynote speaker. Andy co-invented the MQTT messaging protocol <a title="MQTT 10th birthday party" href="http://mqtt.org/2009/07/10th-birthday-party" target="_blank">about 10 years earlier</a> and, while there was a server implementation of MQTT (<a title="RSMB on IBM alphaWorks" href="http://www.alphaworks.ibm.com/tech/rsmb" target="_blank">Really Small Message Broker</a>; RSMB) that you could download for free from IBM&#8217;s website, it was proprietary and there was no open source implementation available.

Andy wrote <a title="Andy's slides on Slideshare" href="http://www.slideshare.net/andysc/the-house-that-twitters" target="_blank">a new presentation</a>, especially for OggCamp, describing the geeky innards of his Twittering house (<a title="The Twittering House on the BBC" href="http://news.bbc.co.uk/1/hi/technology/8113914.stm" target="_blank">as seen earlier that year on the BBC</a>). The presentation was a fantastic kickstart to the day and (somewhat predictably for a conference with its foundations firmly in the open source world) Andy was questioned about what bits of his home automation system were built on open source software and open standards. The one significant part of the system that was proprietary was RSMB (the core part that enabled all the parts of his house to communicate).

Then OggCamp started, we had a good time, and we went home exhausted but happy.

And then, just two weeks later, Roger announced that he&#8217;d registered a new project called <a title="Mosquitto on Launchpad" href="https://launchpad.net/mosquitto" target="_blank">Mosquitto</a> (as in MosQuiTTo) on Launchpad. He&#8217;d been inspired by Andy&#8217;s talk at OggCamp to write an open source alternative to RSMB. Within what seemed like days he had a working bit of code which was taken up and tested by others in the open source community and hardware-hacking communities like <a title="Homecamp website" href="http://homecamp.org.uk/" target="_blank">Homecamp</a>.

I cannot claim any credit at all for all the hard work that Roger and others put in developing and testing Mosquitto. I&#8217;ve always been proud, though, that Mosquitto was born at OggCamp &#8211; we played our small part in helping connect the previously mostly corporate/business MQTT with the open source communities.

That <a title="Facebook announcement described in MQTT.org blog" href="http://mqtt.org/2011/08/mqtt-used-by-facebook-messenger" target="_blank">Facebook announced they were adopting MQTT</a> for their new messaging system the day before OggCamp 11 meant we could vicariously revel in Roger&#8217;s glory while we tried to find out just whether Facebook had adopted his code or their own implementation. The answer seems to be somewhere between the two.

And while I&#8217;m proud for OggCamp (of course), I&#8217;m also excited for Roger in his own right that <a title="Facebook licence screenshot" href="http://mosquitto.org/wp-content//assets/uploads/2011/08/image.png" target="_blank">his name is now in the licence</a> agreement of apps from the mighty Facebook &#8211; that kind of recognition for your hard work must be such an amazing feeling!