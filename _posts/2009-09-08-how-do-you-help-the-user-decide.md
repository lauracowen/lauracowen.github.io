---
id: 228
title: How do you help the user decide?
date: 2009-09-08T21:20:59+00:00
author: Laura
layout: post
guid: http://www.lauracowen.co.uk/blog/?p=228
permalink: /blog/2009/09/08/how-do-you-help-the-user-decide/
tweet_this_url:
  - getnew
  - getnew
tmac_last_id:
  - "465491838359457792"
  - "465491838359457792"
dsq_thread_id:
  - "7699621593"
categories:
  - 'HCI &amp; Usability'
  - Open Source
tags:
  - Ubuntu
  - usability
---
One thing that I often debate with developers is why the error message  &#8220;An unexpected error has occurred.&#8221; isn&#8217;t a good message. Afterall, to the developer, the error \*is\* unexpected; otherwise, they&#8217;d have created a better error message for it.

From the user&#8217;s perspective (who the software is written for, after all), they don&#8217;t want to know that the error was not expected by the people who wrote the code. The user wants to know that the software (especially when it&#8217;s important to their job/finances/life) is in control and knows \*exactly\* what&#8217;s going to happen when you press a certain button. The user has to be able to trust the software and trust that the developer(s) of that software knew what they were doing when they wrote it.

So it gets difficult for the developer/designer when they have to make a call that potentially risks breaking that trust. For instance, supposing you (as a developer) were to provide a new feature that is really beneficial to the target user but there is a small risk that something will go wrong in a big way for that user if they try to use that feature. As developer, what do you do?

Typically, I&#8217;d predict, you would make the feature optional so that you aren&#8217;t forcing the user to use a feature that could potentially (however unlikely) cause them serious problems. If the user does try to use the feature, you provide scary warnings of what could occur in certain circumstances. Hopefully, that will put them off unless they really know what they&#8217;re doing.

Okay, that&#8217;s the developer&#8217;s perspective. And it&#8217;s entirely understandable and even laudable that the developer is doing what they can to keep the user safe.

So, switch now to the user&#8217;s perspective. The target user is computer literate but had no knowledge of the development of this feature or who developed it. This user could benefit greatly from this new feature but when they attempt to use it, they get a scary warning message which, as intended, makes them think twice about whether to use the feature or not.

Now what does the user decide? Granted, risk is all about weighing up the costs and benefits, and to one person the relative benefit will outweigh the possible cost. To make a decision, however, a person needs as much information as they can possibly get. In this case, the only (and therefore critical) information is provided by the developer; that is, how informative and/or scary the warning message is.

If the developer provides a lot of information that makes the feature look useful, the user might just choose to use it. But if the developer makes the warning message as scary as possible, the user will probably opt not to use it.

The developer wants users to use the new feature because they&#8217;ve made the effort to develop it and it really could benefit many users. The developer, however, doesn&#8217;t (understandably) want the responsibility of trashing someone else&#8217;s laptop in some way. So the result is that the developer pushes that responsibility off on to the user, when in fact the developer has far more information available to help them make that decision than the user has.

If you&#8217;re the user, though, how are you supposed to make that call?

For example&#8230;

Computer Janitor is a utility that was introduced in Ubuntu Intrepid (I think) so that you could run it to clean up old kernels that are no longer needed, and other bits and pieces of packages that are no longer used. When I first tried to use it, I raised <a title="Computer Janitor bug" href="https://bugs.launchpad.net/ubuntu/+source/computer-janitor/+bug/371918" target="_blank">this bug</a>, which, it turned out, had <a title="other Computer Janitor bug" href="https://bugs.launchpad.net/ubuntu/+source/computer-janitor/+bug/349336" target="_blank">this duplicate</a>.

Essentially, CJ could potentially remove packages that you might need. So when you try to use it tries to scare you into deciding whether you really really want to risk it. I raised the bug because the scary words don&#8217;t actually help you decide &#8211; in that, if you aren&#8217;t easily scared by such things, the scary message only determines how scared you are &#8211; not how well-informed you are to make a decision&#8230;and isn&#8217;t going to help when you break your computer.

What would maybe be more helpful is if CJ used a stricter set of criteria when selecting which files to remove. In this case, CJ might leave on your system  some files or packages that could be removed, instead of the reverse where it might incorrectly remove files or packages you need. The former is surely the preferably outcome for the majority of users (who would rather have a few unneeded files on their machine than a broken machine).

It would also be possible then, for the minority of users who really really know what they&#8217;re doing, to selectively delete the files that probably can be removed but CJ isn&#8217;t certain about. In this case, users are only presented with a decision to make if they actually seek it out but the majority of users are still able to benefit from the safer (if slightly less effective) behaviour. In fact, it would be better overall if CJ ran automatically during an Ubuntu upgrade so that the user really doesn&#8217;t have to care about it (unless they really really want to).

This is not intended as a dig at Computer Janitor as I think it&#8217;s a useful feature in general and I&#8217;m kindof surprised that this kind of clean-up wasn&#8217;t being done already whenever you do an upgrade of Ubuntu. Also, I think the bugs I&#8217;ve linked to above have caused a bit of a headache for the developers.

This issue of forcing users to make ill-informed decisions is a very common occurrence throughout software development and is certainly not specific to Ubuntu; it&#8217;s just that Ubuntu is a public development effort and provides examples that are relatively easy to explain. 🙂 So please don&#8217;t be offended if you are part of the development teams for either Computer Janitor or Ubuntu!

So, if you, as developer/designer, find that you&#8217;re having to give scary messages to make a user \*really\* decide if they want to continue, consider stepping back from it, thinking about the possible decisions the user could make and what the consequences of those decisions are. Even talk to some of your target users and find out what decisions they&#8217;d make. Just because you can successfully scare them off doesn&#8217;t make it a successful feature &#8211; if the feature is potentially useful to the user, they should be able to safely use it (no matter what level of fear you instill in them). Then look at the bigger picture, think about it in a different way, and see if the decision can be made for the user, or the decision can even be removed altogether.

I&#8217;m sure that it&#8217;s not as easy as it might sound. And it&#8217;s not always easy to recognise situations like this. I&#8217;m hoping, though, that, having thought this through while writing this post, I&#8217;ll actually remember it in future the next time a similar issue occurs for me.