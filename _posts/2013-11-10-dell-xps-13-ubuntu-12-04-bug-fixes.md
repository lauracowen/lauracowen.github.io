---
id: 1694
title: 'Dell XPS 13 Ubuntu: 12.04 bug fixes'
date: 2013-11-10T12:00:00+00:00
author: Laura
layout: post
guid: http://www.lauracowen.co.uk/blog/?p=1694
permalink: /blog/2013/11/10/dell-xps-13-ubuntu-12-04-bug-fixes/
tweet_this_url:
  - http://is.gd/CMcqkT
  - http://is.gd/CMcqkT
tmac_last_id:
  - "465491771238002688"
  - "465491771238002688"
dsq_thread_id:
  - "7699619277"
categories:
  - Open Source
  - Technology
tags:
  - Ubuntu
---
Back in July, I bought a <a href="http://www.dell.com/learn/us/en/555/campaigns/xps-linux-laptop">Dell XPS 13 Ubuntu (aka Developer Edition)</a> laptop. It is a thing of beauty; the screen, awesome (1920 x 1080; full HD). The XPS 13 comes with Ubuntu 12.04 installed by default, along with some additional software from Dell to make the hardware work. 12.04 was, afterall, a year old already by then.

Unfortunately, not everything works out the box. This post is about how to make them work. I might, another time, write about the pleasant but frustrating Dell &#8217;24/7&#8242; ProSupport  warranty process (though [@DellCaresPRO](https://twitter.com/DellCaresPRO) is pretty responsive).

##  Problems in 12.04 for the Dell XPS 13 Ubuntu laptop

These are the problems I found (almost all of them had already been reported as [bugs on Launchpad](https://launchpad.net/dell-sputnik) or on [Dell&#8217;s dedicated community forum](http://en.community.dell.com/techcenter/os-applications/f/4613.aspx)):

  1. Intermittent freezing.
  2. Wifi dropped out frequently.
  3. Logitech wireless trackball frequently not detected on boot.
  4. Problems mounting devices as harddrives using USB2.0 port.
  5. Touchpad &#8216;edge scrolling&#8217; doesn&#8217;t work and the acceleration/sensitivity settings don&#8217;t seem to do anything.
  6. Bluetooth file transfer from my phone doesn&#8217;t work.

##  Fixes

I installed the following two packages from the Ubuntu repositories:

`linux-generic-lts-quantal`

`xserver-xorg-lts-quantal`

These install kernels and associated graphics drivers from future versions of Ubuntu. Basically, it means that when the bugs are fixed in future versions, you can use those fixes without having to upgrade the rest of the machine. The packages you&#8217;ll get are [listed on the Ubuntu wiki](http://packages.ubuntu.com/quantal-updates/kernel/). You can check which kernel version you&#8217;re using on your laptop by running the command &#8216;uname -a&#8217;.

The newer kernel version fixed _problems 1 to 4_. It also seems to have fixed most of _problem 5_ except for &#8216;edge scrolling&#8217;. I now use two-finger scrolling on the rare occasions I use the touchpad so I&#8217;m not too worried about this.

_Problem 6_ (for anyone, like me, who didn&#8217;t know this) is intentional. Receiving files by bluetooth is switched off by default in Ubuntu 12.04. I can see why that might be, but it&#8217;s not obvious how to switch it on. Someone pointed me to [the answer on Ask Ubuntu](http://askubuntu.com/questions/131570/how-do-you-make-ubuntu-accept-files-sent-over-bluetooth).

## Upgrading Ubuntu

Alternatively, you could just try upgrading the whole laptop to a newer version of Ubuntu. A friend bought an XPS 13 at the same time as me and he immediately installed Kubuntu 13.04 (same as Ubuntu 13.04 where it matters here) on it and had no problems. Similarly, [a recent post on Dell&#8217;s forum suggests 13.10 works well](http://en.community.dell.com/techcenter/os-applications/f/4613/p/19528039/20461635.aspx#20461635).

There were three reasons I didn&#8217;t upgrade:

  1. I wanted to stay on the LTS (long-term support) version of Ubuntu which is currently 12.04.
  2. The XPS 13 Developer Edition is sold as working so I was keen for this to actually be the case!
  3. I use a Logitech universal receiver trackball and there were problems with the drivers in later kernels. However, I think this has now been fixed.

## My opinion

I think it&#8217;s pretty bad that all this stuff isn&#8217;t installed and working out-of-the-box and that the 24/7 ProSupport warranty isn&#8217;t really worth much in practice (the support people I spoke to were fine but Dell needs to improve its support processes for this product).

I do, however, love the laptop. Now it&#8217;s working, I&#8217;m very pleased with it. Did I mention how lovely the screen is?
