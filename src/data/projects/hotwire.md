---
title: Hotwire
description: Fast and convenient link between phone and computer
tags:
  - NFC
  - Automation
  - Tasker
featured: true
image: /hotwire.webp
---

Browsing on the phone is easy. Reading in the computer is more convenient.

This situation probably has happened to you more times than you realize:
* You have your laptop open, doing something
* You're reading an article on your phone

Maybe you're waiting for the video to buffer on the computer and you quickly open the news, or perhaps you're 
writing code when suddenly your friends share you a link to the restaurant you're going to later.

You click **open**. And suddenly, you find yourself navigating through a website poorly optimized for phones, or 
just going through the hassle of filling out forms in a mobile phone when you computer is right there.
Yes, you could open **Whatsapp web** in the laptop, and wait for an eternity for it load, then click the link.
You could go through your **history** and open the page again, or click **Share** and share the page with your computer.
If you are an Apple user, you can just use **Handoff**. But as an Android/Windows user, I can't do that. 
And any of the other methods are too inconvenient to justify switching to your computer.

But what if you could share the contents of your phone to your computer in less than a second? **Hotwire** makes it
as easy as just tapping.

The laptop has a tiny **NFC tag** called Hotwire, hidden under a sticker. Just get the phone close to the tag, and the website
you're reading is immediately on your computer. Maximum convenience.

I know what you're thinking. No one asked for this. It's solving a problem no one has. No one cares.

And yet, once you try it, it's impossible to go back. Just like using your phone to check your messages becomes
automatic, just like it feels unnatural to not have it with you, that same feeling is the one I've had when using
other computer that didn't have my Hotwire tag. It doesn't happen often, but when it does it's like Domino's pizza
not offering delivery. What do you mean I have to go physically and do it myself? Hotwire has become one of the
little invisible automations that make the day to day easier and save you time in the long run.

The program is made in Tasker, and it automatically runs on the background on my phone. When it reads the correspondent
NFC tag, it runs accessibility services to read the current url or app, and sends it to the computer using Join.
Chrome then immediately opens with the requested link. It even detects apps such as Netflix, Whatsapp or Outlook
and opens the corresponding webpage in the browser.

Overall, this is a deceptively useful project that I still use in my day to day life. I even put another Hotwire tag
near the screen of my home PC to use it there too.