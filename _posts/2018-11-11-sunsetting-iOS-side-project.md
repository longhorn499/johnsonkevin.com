---
layout: post
title: Shutting Down an iOS Side Project
---

My project I'm about to shutdown is a marketplace app for paintball players to buy/sell/trade gear. It never attracted a large amount of users by any means (~80 daily active users at the end), but when it felt time to shutdown the idea to pull it from the App Store without warning felt wrong. People could be in the middle of a deal and not have a way to wrap up. Also I wanted to have some closure with a project I'd spent over a year working on. 

How are you supposed to do this though? There are plenty of posts about how to build apps that others will (hopefully) use, but less on how to wind them down in a reasonable way. We are less likely to share what we may perceive as a failure. Though any difficult project (regardless of  outcome) delivers plenty of valuable lessons.

> "You are only entitled to the action, never to its fruits." 

### Diving in 

I hadn't looked at the code in roughly 3 months because I'd lost interest and started working on other projects. I also had gotten in a position  where I felt that an Android app would be more valuable than any additional work on the iOS side. On the Instagram page the #1 thing I heard was make it for Android. I ended up working on neither. Working on iOS felt like procrastinating working on something more impactful, and the idea of learning React Native to create an Android app (and potentially a cross-platform app) was appealing for a moment but ultimately I never did it.

![lolios](/img/lol_ios_only.jpg)


### Reasoning 🤔

I no longer had any interest working on the project and additional steps to grow users seemed not worthwhile. Server costs from AWS were insignificant, but felt like a waste when I'd get the bill and realize I hadn't worked on the project that month.

I never achieved a large amount of users by any means with this project, but thinking about trying to grow just made me think about potential issues rather any type of satisfaction.

![firebase](/img/firebase_dashboard.png)

An online marketplace is something I would not recommend as a solo project (pretty obvious). It can be fun at first, but as it grows in size the amount of customer support you'll have to provide is untenable. When people get ripped off it does not feel great at all (no active marketplace is 100% scammer free - no exceptions). Even though I received only 1-2 emails over roughly a year where someone had gotten scammed, that still felt bad. Thinking about potential user growth made me think about scammer growth instead. I had established rules, could direct people to PayPal for claims, and discourage/warn against trading on the platform, but bad things could still happen in a marketplace I had built and encouraged people to use.

I think there can be a tendency to shirk responsibility when it comes to addressing people behaving poorly that are enabled by something you created. I felt this way sometimes, but  mostly felt guilty about anything that had happened or could happen that I wouldn't be able to fix. No wonder people like to build RSS readers on the weekend and not eBay clones.

### Steps

* Release a version to the App Store with an alert that lets active users know the shutdown date. This gives people using the app roughly 1 month notice which seems fair for a small project

![lolios](/img/shutdown_alert.png)

* Announcement on social media (in my case just Instagram)

* NO email message even though I do have access to most user emails in Firebase. I never sent emails to users and didn't want to do it now, especially considering that many of those people are not using the app anymore. Shoutout to Overcast's great policy when it comes to [email](https://overcast.fm/skeptics_faq)

* Respond to any messages/questions I receive via email or on Instagram 

#### Day of Shutdown

* Pull from App Store

* Shutdown Firebase: disable write access to database, storage, and ensure I have one last backup saved

* Shutdown EC2 instance I used for PayPal and sending Push Notifications (I think you can send Push Notifications with Cloud Functions in Firebase but never figured it out 🌝)

* Cancel GoDaddy auto-renew for website domain, associated email address, and hosting

Clearly this is not how you would shutdown something of a larger scale. I couldn't find any posts about ending a smaller iOS project so here we are.

### Shoutout

Shoutout to [Grailed](https://grailed.com), the idea came from thinking about what if there were a Grailed-like marketplace for paintball players (tailored marketplace for niche audience). 

### After	

TBD. Will fill this in later (if anything noteworthy occurs).

Any comments or have a similar experience? Tweet me [@dirtydan499](https://twitter.com/dirtydan499)

















