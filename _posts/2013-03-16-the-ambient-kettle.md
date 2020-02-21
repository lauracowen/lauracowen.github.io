---
id: 1511
title: The Ambient Kettle
date: 2013-03-16T15:06:21+00:00
author: Laura
layout: post
guid: http://www.lauracowen.co.uk/blog/?p=1511
permalink: /blog/2013/03/16/the-ambient-kettle/
tweet_this_url:
  - http://is.gd/SwOATZ
  - http://is.gd/SwOATZ
tmac_last_id:
  - "465491775193231360"
  - "465491775193231360"
categories:
  - Blogging, Twittering, etc
  - 'HCI &amp; Usability'
  - Making Things
  - Technology
tags:
  - eightbar
  - Making Things
  - Twitter
---
<p style="text-align: left;">
  Back in 2007, <a title="My new friend blog post" href="/blog/2007/05/24/my-new-friend/">my Mum and I got a pair of Internet-connected Nabaztag bunnies</a>. Aside from all the online content we could subscribe to using the bunnies, the most fun thing for me was that we could &#8216;pair&#8217; our bunnies so that they would talk to each other. If I moved the ears on my bunny, the ears on my Mum&#8217;s bunny would move to match, and vice versa. The 250 physical miles disappear for a few seconds when you see the ears move and know that it&#8217;s because Mum is physically moving the ears of her bunny. I know exactly what she&#8217;s doing at that particular pointing in time, as if we&#8217;re briefly in the same room. The technical term for this is, apparently, <a title="Ambient awareness on Wikipedia" href="http://en.wikipedia.org/wiki/Ambient_awareness" target="_blank"><em>ambient awareness</em></a>.
</p>

![My Nabaztag bunny](/assets/uploads/2013/03/bunny.jpg)

<p style="text-align: left;">
  The bunny ears experience of ambient awareness inspired my first (and, so far, only) Arduino project: <a title="Electricity monitoring with Christmas lights and Arduino" href="/blog/2010/02/09/electricity-monitoring-with-christmas-lights-and-arduino/">Monitoring electricity using Christmas lights</a>. The red/orange lights indicated the current electricity usage of my house and the blue/green lights indicated the current electricity usage of Mum and Dad&#8217;s house. The more electricity currently being used, the faster the lights flashed. Again, it was just that tiny tiny insight into what was happening 250 miles away. Just the mundanity of everyday life shared.
</p>

<p style="text-align: left;">
  So I was curious about the <a title="Kickstarter project for Good Night Lamp" href="http://www.kickstarter.com/projects/designswarm/good-night-lamp/" target="_blank">Kickstarter project</a> for the <a title="Good Night Lamp website" href="http://goodnightlamp.com/" target="_blank">Good Night Lamp</a>. The Good Night Lamp is a really nice and simple concept. One person has a Big Lamp (shaped like a  house) and they give Little Lamps, associated with the Big Lamp, to friends and/or family anywhere in the world. When the owner switches off the Big Lamp (when they go out or go to bed), the associated Little Lamps also switch off. An appealing part of it is that you can collect a Little Lamp from each of your family or group of friends and arrange them on a shelf so that before you go to bed at night, you can see each of them &#8216;say goodnight&#8217; as their respective lights go out.
</p>

![Good-Night-Lamp](/assets/uploads/2013/03/Good-Night-Lamp-9.jpg)

<p style="text-align: left;">
  The problem I see with the Good Night Lamp is similar to the one with the Nabaztag. While I think it&#8217;s great having simple devices that do just one thing well, it doesn&#8217;t half clutter up the place. These kinds of devices need shelf-space. And it has to be shelf-space you can see easily in a place you&#8217;ll often be or they don&#8217;t work. Maybe as people replace all their books with the more easily stored ebooks, living-room bookcases will become filled with ambient devices instead. I got to chatting with <a title="Ambient Orb website" href="http://www.ambientdevices.com/about/consumer-devices" target="_blank">Ambient Orb</a> fan <a title="@andysc on Twitter" href="https://twitter.com/andysc" target="_blank">Andy Stanford-Clark</a> about it.
</p>

<p style="text-align: left;">
  While my and my Mum&#8217;s&#8217; Nabaztags have now died or gone into hibernation and the Christmas lights never made it as far as the tree, our more lasting providers of ambient awareness don&#8217;t even have their own physical forms. Instead, they&#8217;re software on our smartphones and tablets, devices that we have around anyway, wherever we are. In particular, SMS updates of my Mum and Dad&#8217;s Tweets.
</p>

<p style="text-align: left;">
  Every morning, my Mum wakes up, has a coffee with my Dad, and reads interesting articles on her iPad. I know this from when I&#8217;ve visited them and because when she reads an interesting article, she tweets or retweets it and I receive about half-a-dozen txts in quick succession. Later in the afternoon, after they&#8217;ve got home from wherever they&#8217;ve been that day (or have found free wifi somewhere while they&#8217;re out) and are drinking another cup of coffee or tea, I receive another half-a-dozen txts pointing to interesting articles online. Just receiving the txts gives me an awareness of them waking up or sitting down to read the paper. Clicking the links to the articles gives me an insight into what they&#8217;re reading and how they&#8217;re probably feeling about the topics of the articles. The fairly mundane, everyday things that we wouldn&#8217;t remember, or bother, to talk about on the phone a week or so later.
</p>

<p style="text-align: left;">
  As drinking coffee or tea seems to play a regular, if side, part in the activities I&#8217;m notified about, Andy and I came up with the idea of the Ambient Kettle. In my house, we have a whole house <a title="Current Cost website" href="http://currentcost.co.uk/" target="_blank">Current Cost monitor</a> that is connected to a server out on the Internet. It was the feed from this server that we used in my Christmas Lights project. Since then, though, I&#8217;ve added individual appliance monitors (IAMs) to a few of the appliances around the house, including the kettle. The feeds from these IAMs also go to the server and so can be used by applications that know which data to request.
</p>

<p style="text-align: left;">
  So Andy hacked up a (private) Twitter account, @ambientkettle, which my Mum follows. Each time the kettle boils in my house, the @ambientkettle account tweets to my Mum:
</p>

![@ambientkettle tweets](/assets/uploads/2013/03/kettle-tweet.png)

<p style="text-align: left;">
  Without being physically present or explicitly letting her know that I am making a cup of tea, she can get a sense of what I&#8217;m doing. The messages in the tweets that @ambientkettle sends are pre-canned and chosen at random but made to be chatty enough that it seems a bit like the start of a conversation. Indeed, Mum sometimes tweets back to it to say that she and Dad are also having a cup of tea or are looking forward to one when they get home, or whatever. As I say, it&#8217;s mundane but it&#8217;s those kinds of mundane things that make everyday life.
</p>

<p style="text-align: left;">
  I&#8217;ll be interested to see how the Good Night Lamp gets taken up. It was featured in the very mainstream <a title="@GNLteam's tweet about Daily Mail article" href="https://twitter.com/GNLteam/status/312626544336064512" target="_blank">Daily Mail yesterday</a> and <a title="Good Night Lamp team" href="http://goodnightlamp.com/team/" target="_blank">its founding team</a> has a good record of startups, product design, interaction design, and Internet of Things creativeness. And there&#8217;s something very appealing about having ambient awareness of friends and family when we&#8217;re geographically spread apart.
</p>
