---
id: 473
title: 'Installing Rational Software Architect 7.5.4 and WAS 7 on Ubuntu Karmic'
date: 2010-03-20T14:25:12+00:00
author: Laura
layout: post
guid: http://www.lauracowen.co.uk/blog/?p=473
permalink: /blog/2010/03/20/installing-rational-software-architect-7-5-4-on-ubuntu-karmic/
tweet_this_url:
  - getnew
  - getnew
tmac_last_id:
  - "465491826338959360"
  - "465491826338959360"
dsq_thread_id:
  - "7699621178"
categories:
  - Open Source
  - Technology
tags:
  - IBM
  - Ubuntu
  - WASdev
---
N.B. I updated the bit about dash/bash on 23rd March after feedback from Gavin and Dom (see below). 🙂

* * *

This week, I decided to install Rational Software Architect so that I could try out (again) the <a title="JT's blog post about UIG release" href="IBM InfoSphere Master Data Management Server" target="_blank">User Interface Generator which comes with IBM InfoSphere Master Data Management Server</a>&#8211;and other products too, I believe. You can find out more about what user modelling is and how you can use the UIG in RSA (lovin&#8217; the IBM TLAs yet? 😉 ) in this <a title="Series of articles on developerWorks about user modelling" href="http://www.ibm.com/developerworks/views/rational/libraryview.jsp?search_by=demystified" target="_blank">series of articles on developerWorks</a>. The rest of this post is not about the UIG but about how to install and configure Rational Software Architect for WebSphere, which is relevant to anyone wanting to do this, regardless of whether they&#8217;re wanting to use the UIG.

So I wanted to install Rational Software Architect (RSA; an Eclipse-based piece of software) on to Ubuntu, which is what I run on my work machine, a Thinkpad T61p. Not only that, but I wanted to install RSA for WebSphere, which includes WebSphere Application Server Test Environment (WAS). This meant that I was installing not one but two pieces of software that are not officially supported for Ubuntu Karmic (or indeed for Ubuntu/Debian as far as I know). But as the Linux binaries are .bin files rather than .rpm, life should be easy.

And indeed installing it is. It&#8217;s when you want to create a WAS profile that the fun starts. And that&#8217;s where it had all fallen apart for me when I tried much the same exercise this time last year. That time, I gave up.

This time, I tweeted my predicament, knowing there were people who might know the answer. Unfortunately, the person I thought might know the answer had failed in much the same way as me only 6 months ago and was now relegated to using Windows. Still, others came back to me, including <a title="Gavin Willingham on Twitter" href="http://twitter.com/gavinwillingham" target="_blank">Gavin Willingham</a>, who I&#8217;d not met before but who works possibly 10 minutes walk from my desk, and <a title="Jay Limburn on Twitter" href="http://twitter.com/jaylimburn" target="_blank">Jay Limburn</a>, who I&#8217;ve known for a year through Twitter and internal instant messaging but, though he also works max 10 minutes walk from my desk, never met in person until yesterday (<a title="Jay's tweet to me - I hadn't said anything!" href="http://twitter.com/jaylimburn/status/10737242668" target="_blank">he&#8217;s shorter and blonder in real life</a>).

So, if you&#8217;re trying to install RSA for WebSphere 7.5.4 with WAS Test Environment 7.0 (other versions probably work the same way), I&#8217;ll end the suspense and start here:

## Running the installer

  1. Download the many parts of RSA for WebSPhere 7.5.4 and WAS Test Environment 7.0 with licence/activation bits and pieces. (NB this isn&#8217;t free software; you have to buy it from IBM so I&#8217;m assuming you&#8217;ve got that far by now.)
  2. Extract all the zip files. If you do a right-click > &#8216;Extract All&#8217; on the zip file in Ubuntu, the extraction tool doesn&#8217;t like to overwrite directories of the same name, so you end up with directories called &#8216;RSA4WS&#8217;, &#8216;RSA4WS (2)&#8217;, &#8216;RSA4WS (3)&#8217;, and so on when actually, you want the contents of each of those directories to be in the same place. So move the directories around so that you have just 3 directories: 
      * RSA4WS (contains 7 directories called &#8216;disk1&#8217;, &#8216;disk2&#8217;, &#8216;disk3&#8217;, etc)
      * RSA4WS_SETUP (don&#8217;t do anything with the contents of this one)
      * WAS70 (contains 4 directories called &#8216;disk1&#8217;, &#8216;disk2&#8217;, etc)
  3. In the RSA4WS_SETUP directory, as sudo, run launchpad.sh to start the installation process.
  4. Follow the installer through but when it asks you for a user name and password to create a WAS profile, select that you will create a profile later and that you don&#8217;t want to create one now. The installation should run cleanly (if you let it try to create a profile, it will fail part-way through the installation).

You should now have a nice installation of RSA with WAS on your Ubuntu box. Next, you need to create a WAS profile so that you can use the in-built WAS server for development and testing (or in my case, to run the user interface generator).

## Creating a WAS profile in RSA

There are a few things that prevent this just happening (some are generic Linux things and some are specific to Ubuntu):

  * On Ubuntu, /bin/sh uses dash, not bash, but WAS scripts seem to use bash specifically, so the profile creation scripts fail.
  * Something extra that I have no understanding of is required in the eclipse.ini file (which is key in starting the Eclipse-based RSA environment).
  * The default location in WAS&#8217;s profile creation wizards is in the /opt part of the main file system which you typically won&#8217;t have write-access to as a normal user.

So here&#8217;s what you need to do (at least, this is what I did and hopefully will work for you to to get a running WAS server in RSA):

  1. Change Ubuntu&#8217;s /bin/sh to use bash instead of dash.  
    In a terminal (sorry it&#8217;s the command line but you&#8217;re changing some system settings here that you would very very rarely have to do normally, or just if WAS didn&#8217;t specify bash specifically), run the following command and select the bash option as the default for /bin/sh:</p> 
    <pre>sudo dpkg-reconfigure dash</pre>
    
    (As pointed out by <a title="Dom Evans's Twitter page" href="http://www.twitter.com/oldmanuk" target="_blank">@oldmanuk</a> (Dom Evans), this is the proper way to reconfigure where /bin/sh points to (though I used <a title="Gavin's blog post about installing Ubuntu on his Lenovo W500 laptop" href="http://www.gavinwillingham.com/linux-on-w500.html" target="_blank">Gavin&#8217;s method</a>). )
    
    After you&#8217;ve created your WAS profile and everything&#8217;s up and running nicely, run the command again to change back to using dash. The benefit of using dash is speedier boot time, which is lost if you leave the setting as bash (see <https://wiki.ubuntu.com/DashAsBinSh> &#8211; thanks Dom).
    
    Now you&#8217;ve sorted out the bash/dash problem. One down; two to go.</li> 
    
      * Check that you have a version of xulrunner installed (I have no idea what xulrunner is for but, looking in Synaptic Package Manager, my Ubuntu installation included xulrunner-1.9l.1-gnome-support, but not the xulrunner package itself, which seems to be fine for RSA purposes).
      * In your RSA installation, find the eclipse.ini file. I installed RSA to the default location so mine was in /opt/IBM/SDP. In a terminal change to that directory: 
        <pre>cd /opt/IBM/SDP</pre>
    
      * Open the eclipse.ini file in a text editor, such as gedit: 
        <pre>sudo gedit eclipse.ini</pre>
    
      * Add to the end of the file the following line: <pre dir="ltr">-Dorg.eclipse.swt.browser.XULRunnerPath=/usr/lib/xulrunner</pre>
        
        (From <a title="Ubuntu forum post about making Eclipse apps start on Karmic" href="http://ubuntuforums.org/showthread.php?t=923583" target="_blank">an Ubuntu forum post</a>.)
        
        Now you&#8217;ve sorted out the &#8216;xulrunner&#8217; problem and you can actually start RSA. Two down; one to go.</li> 
        
          * Start RSA from the Applications menu: **Applications > IBM Software Delivery Platform > IBM Rational Software Architect for WebSphere 7.5.4**.
          * RSA should suggest a directory in your home directory in which to put the RSA workspace. That&#8217;s fine; I just accepted the suggested location.
          * When RSA has opened (NB, my Welcome view doesn&#8217;t load &#8211; I don&#8217;t think that&#8217;s a problem), give it a moment to think, then it&#8217;ll pop up a wizard to create a WAS profile.
          * In the profile wizard, clear the option about security unless you know what you&#8217;re doing with WAS security and have a need to use it in a development environment.
          * You&#8217;ll also notice that there&#8217;s a warning about the currently selected location for creating the profile. This is the third problem I listed above. The default location shown is for creating the profile in the installation directory of RSA. Change the location to a directory in your home directory. For instance, I told it to use /home/laura/IBM/profiles.
          * When the wizard has created the profile (which will take a few moments &#8211; you can see the activity in the bottom-right of the RSA window), the default server for the profile is listed in the Servers view on the right-hand-side of the RSA window.  
            The server is listed as &#8216;stopped&#8217;.
          * Right-click the server then click Profile. This opens a dialog box about the profile; I just accepted the defaults then it failed to start the server (the error said it had failed to start within 300 seconds). But when I repeated this step, the server started.</ol> 
        
        And that&#8217;s as far as I&#8217;ve got but it&#8217;s further than ever before. If I come across any more gotchas, or take some screenshots, I&#8217;ll update this post.
        
        Yes, it is a pain to have to do all this but remember that WAS isn&#8217;t supported (as far as I know) on Ubuntu Karmic. If you want it easier, install it on something that is supported. If you want it on Ubuntu, I hope this post (and the others I cribbed information from) helps. 🙂
