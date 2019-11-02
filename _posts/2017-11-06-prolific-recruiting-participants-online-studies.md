---
id: 2451
title: 'Prolific: Recruiting participants for online Psychology studies'
date: 2017-11-06T14:27:28+00:00
author: Laura
layout: post
guid: http://lauracowen.co.uk/blog/?p=2451
permalink: /blog/2017/11/06/prolific-recruiting-participants-online-studies/
image: /wp-content//assets/uploads/2017/11/Prolific-create-study-75pc-604x270.png
categories:
  - PhD
  - Technology
---
I&#8217;ve just run a research study in which I paid to recruit participants for the first time. I used the online [Prolific](https://www.prolific.ac/r?ref=H24R8XPS) recruitment website and it went really well. So I thought I&#8217;d share my experience.

## Using Prolific for recruiting participants to my PhD studies

Prolific is a website for recruiting human participants to research studies. People (participants) sign up to do studies, get notified when studies for which they are eligible are available, and get small amounts of money in return if they participate in a study.

According to [Prolific&#8217;s About page](https://www.prolific.ac/about), the company was set up in the last 2-3 years by a former PhD student, Katia (and her friend Phelim), who had struggled to recruit human participants for her research. So the focus is very much on recruitment for research studies with a personal appreciation of what&#8217;s involved in such activities. As I write this, the participant pool seems to include about 37,400 people and they have recently been upgrading their website so it seems to be going well.

## How does it work?

Prolific does not host the studies themselves. You can set up your actual study using all kinds of software; for example, a survey on [Qualtrics](https://www.qualtrics.com) or [Survey Monkey](http://www.surveymonkey.com/), or an experiment on [Gorilla](https://gorilla.sc/). Prolific just helps you recruit participants to it.

You can register for Prolific with a researcher account or a participant account (or both). As a researcher, you can set up studies and add credit to your account to run them. As a participant, you provide some personal information so that Prolific can offer you only studies for which you are eligible. If you participate in a study, you get paid for your time and you can receive that money yourself or donate it to charity.

## How do you use Prolific as a researcher?

When you&#8217;ve set up your online study outside of Prolific, you create a new study in Prolific and give it details of your study, including the URL to the study itself:

![](/assets/uploads/2017/11/Prolific-create-study-75pc.png)

I set up my study in Gorilla. Gorilla integrates nicely with Prolific in that it generates a URL that collects participants&#8217; Prolific IDs automatically (so the participant doesn&#8217;t have to manually enter it). As a researcher, you can also enter the Prolific &#8216;completion URL&#8217; into your Gorilla experiment so that participants don&#8217;t need to manually enter a completion code into Prolific before they can receive payment. This mostly worked seamlessly for me, though I messed up the set up at one point because I accidentally limited my Gorilla study to one fewer participant than on Prolific; don&#8217;t do that, it means that Prolific sends the last participant to Gorilla which then rejects them and Prolific sends another participant, and so on&#8230;

As you can see in the screenshot, Prolific calculates up-front the cost of your study. The cost depends on the number of participants you want to recruit and how much you want to pay them, plus Prolific&#8217;s commission. Prolific enforces a minimum payment to participants of the equivalent of £5 per hour (I paid participants £1.25 for a 15-minute study; some took longer than 15 minutes, most took much less but all received the same amount).

You then provide a textual description of your study so that potential participants can decide whether they&#8217;re interested in taking part. After that, you can optionally select to &#8216;prescreen&#8217; participants according to their basic demographics or other more specific features of their lives:

![](/assets/uploads/2017/11/Prolific-prescreeners-75.png)

I selected that participants should be UK residents which, Prolific helpfully informed me, restricted me to about 18,000 people in the participant pool. Aside from basic demographic details, most of the prescreener questions are optional for participants to complete (though not completing them restricts how many studies they&#8217;re eligible to participate in). The fewer prescreeners you include in your study, the more potential participants are eligible to do your study.

Prolific are quite firm that you must not include screening questions in your actual study (e.g. asking participants if they are a certain age and ending the study if they are not). Instead, you must use the prescreeners so that ineligible participants don&#8217;t even get offered your study. This is because it gets really annoying, as a participant, to be offered a study and then start it, only to then be told you&#8217;re not eligible.

Finally, you have to confirm that you&#8217;ve tested your study and various other things. I specified not to include the page in an iframe. When, as a participant, you start a study, Prolific displays a panel above the study that contains your Prolific details. For studies where the participant has to manually enter their Prolific ID etc for tracking their participation, that&#8217;s maybe useful. For my study, though, Gorilla handled all that automatically and an extra panel on the page just unnecessarily used up screen space.

You can now publish your study, as long as you&#8217;ve credited your account with enough money to cover the calculated cost (you can request a refund for any credit you don&#8217;t spend). At this point Prolific displays your study to eligible participants and email subsets of eligible participants to notify them that there&#8217;s a new study they can take part in. It&#8217;s quite good fun watching the live dashboard update as participants start your study:

![](/assets/uploads/2017/11/Prolific-live-screen-75pc.png)

Prolific keeps recruiting until it reaches your target recruitment number (21 in the screenshot above). You then have 21 days to &#8216;approve&#8217; participants so that they get paid. Prolific has [a few criteria you can legitimately use to approve or reject participants](http://help.prolific.ac/managing-and-reviewing-submissions/reviewing-submissions/reviewing-submissions-how-do-i-decide-who-to-acceptreject). I included some &#8216;attention questions&#8217; in my study and only participants who got a certain number correct were paid (in practice, all of them were fine). I also did some other checks but ultimately accepted all the complete sets of data.

One participant, for some reason, was not presented with all the questions but otherwise completed the study. This appeared to have been a weird technical blip in the study itself so I approved the participant even though I couldn&#8217;t use their data because it wasn&#8217;t their fault. I also, separately, gave a bonus payment of 25p to one participant who had tried to take part but had been bounced out of my study because of my mistake in setting it up (see above) and they contacted me to let me know.

I ended up running the study in Prolific three times. The first time had participants whitelisted to just my participant ID (I&#8217;m registered with a participant account as well as a researcher account) so that I could test it (the recommended way to test that Prolific integrates properly with your study software). The second time, I collected 20 data from participants and then checked that everything was going okay. I then approved their payments but that automatically &#8216;completed&#8217; the study so I couldn&#8217;t just add 21 more participants to the recruitment target. Instead, I had to create the study again by just duplicating it in Prolific (which retained all the same details to integrate with Gorilla) and then screening out anyone who had taken part previously. This worked fine but was a bit unnecessary and annoying. The workaround is to &#8216;pause&#8217; your study before approving and adding additional participants, then unpausing the study to continue running it with the new recruitment target.

All in all, it&#8217;s all pretty easy to use, though it&#8217;s worth reading relevant parts of the [Prolific documentation](http://help.prolific.ac/) to understand how it works and what it can do for you, especially with prescreening and with integrating Prolific with your online study software. I was a bit slow setting up my first study but in future it will be quicker.

## Isn&#8217;t the sample biased by recruiting through a website like Prolific?

All samples are biased unless they&#8217;re completely random and, even then, randomly-selected participants will drop out (or just refuse to take part) so you get some bias of self-selection. This happens in all research that involves human participants. What&#8217;s important is that you try to get as representative and suitable sample as possible for the population that you are studying.

My research is on people&#8217;s perceptions of household energy. Because experiences of household energy vary according to the country you live in (e.g. in the US, aircon is far more prevalent than in the UK), I decided to design my studies for people with experience of living in UK households. A large proportion of Prolific&#8217;s participant pool is UK-based, which suits my studies well.

The [demographics of Prolific&#8217;s participant pool](https://app.prolific.ac/open-demographics) are biased towards Caucasian participants (though [about representative of the UK](https://en.wikipedia.org/wiki/Demography_of_the_United_Kingdom)) and towards younger and middle-aged people. I think it can be assumed that it is also implicitly biased towards people who are willing, comfortable, and able to use websites to participate. Interestingly, despite the large proportion of students in Prolific&#8217;s participant pool, the majority of participants in my study were not students (which was perfect for my studies). If you&#8217;re interested, Prolific have [a collection of links to resources about online versus lab-based studies](http://help.prolific.ac/general/is-online-crowdsourcing-a-legitimate-alternative-to-lab-based-research).

For my study, Prolific was great. I&#8217;m getting close to the end of my PhD and I just need to run some small, exploratory, online studies quickly on people who live in UK households. To check the findings of these studies with other sub-demographics (eg older people in the UK, greater ethnic diversity of people in the UK, people in the UK who are less comfortable with using websites and computers, people not in the UK), in future studies, I would need to find another method of recruitment to complement this one.

## How is Prolific different from Amazon&#8217;s Mechanical Turk?

I did look into using [Amazon&#8217;s Mechanical Turk](https://en.wikipedia.org/wiki/Amazon_Mechanical_Turk) (MTurk) after a friend&#8217;s positive experience of using it for her own PhD study. MTurk is a similar kind of service but for any type of work that can be done online (not just research studies), though researchers have taken to using it quite a lot. The problem for me was that MTurk&#8217;s participant pool is mostly in the US and India and I needed to recruit UK residents. Prolific describe that and other [differences between them and MTurk](http://help.prolific.ac/general/how-is-prolific-different-from-mturk-co). They also provide a link to an independent study that found Prolific was generally better than MTurk for research studies (at least along criteria that I cared about).

## Isn&#8217;t there a danger of recruiting only professional study participants?

Prolific claims to avoid this problem (which has been observed on MTurk) by notifying different subsets of eligible participants so that it isn&#8217;t just the fastest people in the participant pool who get to participate in all the studies all the time.

## Any problems?

I was initially uncertain about how well my study would go because I&#8217;d also registered as a participant to get a feel for the experience from that perspective (I recommend doing this) and experienced a couple of problems. These were partly technical problems caused by the site upgrades. I&#8217;d also wondered how reliably participants got offered the studies because, as a participant, I&#8217;d had to complete many, many prescreener questions before being offered a very small number of studies (though I think this was maybe because of Prolific&#8217;s policy of not encouraging the same few participants to do all the studies).

Ultimately, my study was fine and I recruited my initial 20 participants in about 18 minutes, which was amazing! And they seemed to be fairly representative of the participant pool with a greater range of ages than I&#8217;d expected.

The other main problem was that I discovered that, as a researcher, I could download a lot more information about my participants than I&#8217;d expected or was ethically cleared to obtain. As both a researcher and a participant, this made me uncomfortable. However, I emailed the team and they quickly investigated and addressed the problem, prioritising it to get fixed within a few days. Researchers now have access only to [a limited set of non-identifying data](http://help.prolific.ac/general/researcher-faqs/is-some-basic-prescreening-data-available-via-prolific-or-do-i-have-to-collect-it-during-my-study) about participants plus the participants&#8217; responses to any prescreeners that were selected for the study.

The Prolific support team has been brilliant. You can contact them by email or there&#8217;s an in-site messaging system; if there&#8217;s no one available, they&#8217;ll email you later. They&#8217;ve responded helpfully to every contact I&#8217;ve made and they regularly update their [help/FAQ system](http://help.prolific.ac/).

## Is it worth using Prolific?

I will definitely use Prolific again for another study in the next few weeks so I, obviously, encourage you to sign up as a participant. 🙂 Based on my overall positive experience as a researcher, I recommend it to other researchers and students as an option to consider for their own studies. If you want to give it a go, it&#8217;d be great if you could use [my Prolific referral link](https://www.prolific.ac/r?ref=H24R8XPS) which gives me credit towards future studies I run.