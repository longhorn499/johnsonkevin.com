---
layout: post
title: Sunsetting an iOS Side Project
---

My project I'm about to shutdown is a marketplace app for paintball players to buy/sell/trade gear. It never attracted a large amount of users by any means (~80 daily active users), but when it felt time to shutdown the idea to pull it from the App Store without warning felt wrong. People could be in the middle of a deal and not have a way to wrap up. Also I wanted to have some closure with a project I'd spent over a year working on. 

How are you supposed to do this though? There are plenty of posts about how to build apps and other things others will use, but less on how to take them apart in a reasonable way. We are less likely to share what we or others may perceive as a failure. Though any difficult project (regardless of  outcome) delivers plenty of lessons.

> "You are only entitled to the action, never to its fruits." 

### Diving in 

I hadn't looked at the code in roughly 3 months because I'd lost interest and started working on other projects. I also had gotten in a position  where I felt that an Android app would be more valuable than any additional work on the iOS app. On the Instagram page the #1 thing I heard was make it for Android. I ended up working on neither. Working on iOS felt like procrastinating working on something more valuable, and the idea of learning React Native to create an Android app (and potentially a cross-platform app) was appealing for a moment but ultimately I never did it. I was more interested in a new iOS project that made more sense for a solo dev.

![lolios](/img/lol_ios_only.jpg)


### Reasoning 🤔

I no longer had any interest working on the project and additional steps to grow users seemed not worthwhile. Server costs from AWS were insignificant, but felt like a waste when I'd get the bill and realize I hadn't worked on the project that month.

I never achieved a large amount of users by any means with this project, but near the end thinking about trying to grow made me be think about potential issues rather than how satisfying the growth would have been.

![firebase](/img/firebase_dashboard.png)

An online marketplace is something I would not recommend as a solo project (totally obvious now). It can be fun at first, but as it grows in size the amount of customer support you'll have to provide is untenable. Also when people get ripped off it's ugly, real, and stressful (no active marketplace is 100% scammer free no exceptions). Even though I'd received only 1-2 emails over roughly a year period where someone had gotten scammed, that still felt bad. Thinking about potential user growth made me think about scammer growth. In my case I had established rules, could direct people to PayPal for claims, and discourage/warn against trading on the platform, but bad things could still happen and I'm the one who built these place where it could.

I think there can be a tendency to shirk responsibility when it comes to addressing people behaving poorly that are enabled by something you created. I felt this way sometimes, but  mostly felt guilty about anything that had happened or could happen that I wouldn't be able to provide support for. This is when something that started as a side project, to learn and maybe attract a few users, starts to feel not fun.

Even if you find meaningful ways to reduce the percentage of bad actors, a growing marketplace still sounds like a headache for someone who intends to run it as a side-project. Any project where you're enabling people to connect online can create problems that are difficult to deal with as a solo developer (let alone a large company). No wonder people like to build RSS readers on the weekend and not eBay clones.

### Steps

* Release a version to the App Store with an alert that lets active users know the shutdown date. This gives people using the app roughly 1 month notice which seems fair for a small project

![lolios](/img/shutdown_alert.png)

* Announcement on social media (in my case just Instagram)

* NO email message even though I do have access to most user emails in Firebase. I never sent any emails to users and didn't want to do it now, especially considering that many of those people are not using the app anymore. Shoutout to Overcast's great policy when it comes to [email](https://overcast.fm/skeptics_faq)

#### Day of Shutdown

* Pull from App Store

* Shutdown Firebase: disable write access to database, storage, and ensure I have one last backup saved

* Shutdown EC2 instance I used for PayPal and sending Push Notifications (I think you can do this with Cloud Functions in Firebase but never figured it out 🌝)

* Shutdown website, associated email address, and cancel auto-renewal for domain and hosting

Clearly this is not how you would shutdown something of a larger scale. I didn't see any posts about sunsetting a small project so here we are.

### Shoutout

Shoutout to [Grailed](https://www.grailed.com), the idea came from thinking about what if there was a Grailed-like marketplace for paintball players (tailored marketplace for niche audience). 

### Aftermath

TBD. Will fill this in later (if anything noteworthy occurs).

















