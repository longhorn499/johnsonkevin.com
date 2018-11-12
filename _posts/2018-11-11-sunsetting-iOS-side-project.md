---
layout: post
title: Sunsetting an iOS Side Project
---

My project I'm planning to shutdown is a marketplace app for paintball players to buy/sell/trade gear. It never attracted a large amount of users by any means (~80 daily active users), but when it felt time to shutdown, the idea to pull it from the App Store without warning felt off. People could be in the middle of a deal and then not have a way to wrap up. Also I wanted to have some closure with a project I'd spent over a year working on.

### Diving in 

I hadn't looked at the code in awhile (~3 months) because I'd lost interest and started working on other projects. I also had gotten in a position  where I felt that an Android app would be more valuable than any additional work on the iOS app (on the app's Instagram page the #1 thing I heard was make it for Android). So I ended up not working on either. Working on iOS felt like procrastinating working on something more valuable. The idea of learning React Native to create an Android app and potentially a cross-platform app was appealing for a moment but ultimately I never did it. 

![lolios](/img/lol_ios_only.jpg)


### Reasoning 🤔

I no longer had any interest working on the project and additional steps to grow seemed not worthwhile. Server costs from AWS were insignificant, but felt like a waste when I'd get the bill and realize I hadn't worked on the project that month.

I never achieved a large amount of users by any means with this project, but if I had taken the steps to grow it further it may/would have meant more issues to deal with.

![firebase](/img/firebase_dashboard.png)

An online marketplace is something I would not recommend as a solo project. If it grows to a meaningful size the amount of customer support you'll have to supply is untenable. Also when people get ripped off it's very real and stressful (no active marketplace is 100% scammer free - no exceptions). Even though I received only 1-2 emails over roughly a year period where someone had gotten scammed, they still felt bad to get and were not something I wanted more of. In my case I could direct people to PayPal for claims and discourage/warn against trading on the platform, but bad things could still happen and I'm the one who built the place where that could go down.

Even if you find meaningful ways to reduce the percentage of bad actors, a rapidly growing marketplace still sounds like a headache for someone who intends to run the service as side-project. Enabling people to connect online can be stressful and create problems you don't have the capacity to deal with as a solo developer, let alone a large company in some circustmances. No wonder people like to build RSS readers on the weekend and not eBay clones.

### Steps

* Release a version to the App Store with an alert that lets active users know the shutdown date. This gives people using the app roughly 1 month notice which seems fair for a small project

![lolios](/img/shutdown_alert.png)

* Announcement on social media (in my case just Instagram)

* NO email message even though I do have access to most user emails in Firebase. I never sent any emails to users and didn't want to do it now, especially considering that many of those people are not using the app anymore. Shoutout to Overcast's great policy when it comes to [email](https://overcast.fm/skeptics_faq)

#### Day of Shutdown

* Pull from App Store

* Shutdown Firebase: disable write access to database, storage, and ensure I have one last backup saved

* Shutdown EC2 instance I used for PayPal and sending push notifications (I think you can do this with Cloud Functions in Firebase but never figured it out 🌝)

* Shutdown website, associated email address, and cancel auto-renewal for domain and hosting

Clearly this is not how you would shutdown something of a larger scale, but I didn't see any posts about sunsetting a small project so here we are. Just me walking through what I thought of for this situation.

### Shoutout

Shoutout to [Grailed](https://www.grailed.com), the idea came from thinking about if there were a Grailed equivalent for paintball players (tailored marketplace for niche audience). 

### Aftermath

TBD. Will fill this in later (if anything noteworthy occurs).

















