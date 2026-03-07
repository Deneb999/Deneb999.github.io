---
title: Incentive Machine
description: A specialized chocolate dispenser to reward hard work
tags:
  - Hardware
  - Productivity
featured: true
image: /incentive machine.webp
---

Writing is oftentimes a chore. It doesn't matter if you are trying to push 
through a deadline, code your homework before tomorrow, or write a 50 pages 
report explaining a design decision. In my case, it was setting myself the goal
of writing 500 words every day during my Erasmus in Scotland.

Do you know what makes a chore feel **less** daunting? For me, the answer was snacks.
A well-earned cookie every 100 words or so, to keep my motivation up. 
The problem, of course, is that few people have the iron will to be able
to resist a cookie waiting just in front of their noses. The solution that I came up with
was not developing better _impulse control_ or _concentration._ No. I set out to
build this project.

The **Incentive Machine** is a modified snack dispensing machine with accompanying
software. When you buy one of these machines, they are either completely manual,
or come with a button to dispense *the goods*. As my goal was to not let myself
have a reward until I had earned it, I bought one of the automatic ones and made
the button **logical** instead of **physical**. Instead, a Python script runs
in the background of your computer logging your keypresses. Once you have
reached your desired (configurable) threshold of words written, it does a happy sound and give you
your desired snack (snacks sold separately). The machine is connected to the computer
via USB-C.

The **design** of the machine was pretty straightforward. It was a matter of researching
how to activate a switch programmatically, connecting it to the internal motor
of the machine, and writing a simple keylogger.

The **assembly** was harder. As I mentioned, I was in Scotland during my Erasmus,
with no access to my typical tools, such as soldering iron, scissors or even a
screwdriver. But as my best MacGyver impression, here is a photo of the 
internal circuit, held together by adhesive tape, blu tack I found in the supermarket,
and using a knife to tighten the screws.
![Incentive machine build](/Incentive%20machine%20build.webp)