---
id: 1815
title: Upgrading my Dell XPS 13 to Ubuntu 14.04 LTS
date: 2014-07-14T12:02:34+00:00
author: Laura
layout: post
guid: http://lauracowen.co.uk/?p=1815
permalink: /blog/2014/07/14/upgrading-my-dell-xps-13-to-ubuntu-14-04-lts/
categories:
  - Open Source
  - Technology
---
<blockquote class="twitter-tweet" lang="en">
  <p>
    Watching the first match of the 2014 Men's World Cup tonight. In HD, on BBC1. <a href="https://twitter.com/hashtag/WorldCupFinal?src=hash">#WorldCupFinal</a>
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488383751597342720">July 13, 2014</a>
  </p>
</blockquote>



But I&#8217;m really not that into football, so:

<blockquote class="twitter-tweet" lang="en">
  <p>
    Upgrading my Dell XPS to <a href="https://twitter.com/hashtag/ubuntu?src=hash">#ubuntu</a> 14.04&#8230;
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488390965305298944">July 13, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" lang="en">
  <p>
    Hopefully a very, very dull one. 🙂 RT <a href="https://twitter.com/popey">@popey</a>: <a href="https://twitter.com/lauracowen">@lauracowen</a> There's a blog post in that, maybe.
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488391181194510336">July 13, 2014</a>
  </p>
</blockquote>



And while that was going (my Thinkpad is my work laptop which I&#8217;d brought home with me on Friday):

<blockquote class="twitter-tweet" lang="en">
  <p>
    Whoop whoop! And, meanwhile, I've upgraded my Thinkpad's RAM to a cool 16 GB. <a href="https://twitter.com/hashtag/notreallythatintofootball?src=hash">#notreallythatintofootball</a> <a href="http://t.co/sd1spU9U8e">pic.twitter.com/sd1spU9U8e</a>
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488401921536163840">July 13, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    With this video. And it booted first time! How to Upgrade T430 Thinkpad Laptop to …: <a href="http://t.co/zyeTZ1Xfkb">http://t.co/zyeTZ1Xfkb</a>
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488402460315488256">July 13, 2014</a>
  </p>
</blockquote>



Back at the main story:

<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Hmm, Dell upgrade going less well. Finished upgrade with couple of errors. On reboot when entered pw, just threw me back to login screen.
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488406716758114304">July 13, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Rebooted again and can't mount cryptswap now. 🙁
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488406895028600832">July 13, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Aha. Another reboot gets me back to login screen. But still can't log in. Hmmm
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488407152143663104">July 13, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Neither as me nor as guest. Not my account then&#8230;
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488407517241032704">July 13, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Well, it upgraded. Now to work out what on earth went wrong with display&#8230; <a href="http://t.co/8uNqmpxiFa">pic.twitter.com/8uNqmpxiFa</a>
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488410004547190784">July 13, 2014</a>
  </p>
</blockquote>



Meanwhile, Germany had won the Men&#8217;s World Cup for the first time since reunification (but their fourth if you count West Germany&#8217;s wins), the first European team to win in South America:

<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Angela Merkel is said to be ecstatic after watching Germany win.&#10;&#10;"She's phoning and texting all her friends, she's so happy"&#10;&#10;Said the NSA
  </p>
  
  <p>
    &mdash; funny humour (@funnyhumour) <a href="https://twitter.com/funnyhumour/statuses/488440372083703808">July 13, 2014</a>
  </p>
</blockquote>



I decided to reinstall from scratch. I should probably have done this in the first place because the original installation was the one Dell did with all their custom packages to make the hardware work. The Dell XPS 13 packages (for the laptop I bought in July 2013 anyway) are now all in the official Ubuntu repositories. I think my problems were probably caused by clashes of some kind between the old and new packages.

Almost all my data files are backed up in Dropbox so that bit&#8217;s easy. The Windows 7 virtual machine I use for PhD software is about 26 GB but I can rebuild it if the HDD dies, so I don&#8217;t bother backing it up (the data on it goes into Dropbox). I figured, however, that backing it up to my USB stick might be useful and save me some time. Annoyingly, that&#8217;s the bit that took most of the time. Downloading the Ubuntu ISO and creating a USB installation disk took no time. Then installing it was pretty quick too.

<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    <a href="https://twitter.com/hashtag/Ubuntu?src=hash">#Ubuntu</a> upgrade and Dell XPS 13 fans, upgrade not so good. But fresh installation of 14.04 great so far&#8230;
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488606963740475392">July 14, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    &#8230;Think the mass of original Dell XPS 13 hardware packages got in a pickle with the ones now in the official repos. <a href="https://twitter.com/hashtag/Ubuntu?src=hash">#Ubuntu</a>
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488607168963567616">July 14, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    So far, no additional stuff needed to make laptop work.
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488607411520159744">July 14, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Now just waiting for my virtual machine to copy to USB stick to copy back to laptop&#8230;That's the bit that took most time last night. :-/
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488607668832305152">July 14, 2014</a>
  </p>
</blockquote>



<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Handy that I had both a 32GB USB stick and my work laptop at home though.
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488608068024823808">July 14, 2014</a>
  </p>
</blockquote>



It&#8217;s doubly annoying that the virtual machine took so much of the time (I finished about 1.30am, leaving Dropbox doing its thing while I slept). After waiting for the files to copy back to my newly-installed laptop this morning, I discovered that I&#8217;ve been working in a VirtualBox snapshot. So the 13 GB Snapshots folder that I&#8217;d not copied was kindof essential to things and the virtual machine wouldn&#8217;t boot without it:

<blockquote class="twitter-tweet" data-partner="tweetdeck">
  <p>
    Oh well, so much for backing up my VM. Forgot I was using the snapshot I didn't copy with it. 🙁 Now rebuilding afterall&#8230;
  </p>
  
  <p>
    &mdash; Laura Cowen (@lauracowen) <a href="https://twitter.com/lauracowen/statuses/488631054723727360">July 14, 2014</a>
  </p>
</blockquote>



I can&#8217;t find my Nvivo 10 CD either but I imagine installing Windows 7 and its updates will take most of today anyway. Fortunately it&#8217;s sunny so I might just leave it installing and go do (PhD) reading in the garden.