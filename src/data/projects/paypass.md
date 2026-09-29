---
title: Paypass study
description: An analysis of Mastercard's paypass system
tags:
  - NFC
  - Pen-testing
  - Cybersecurity
  - Android
featured: true
image: /paypass.webp
---

I've been in the hunt for a NFC ring that I can use for payments for a year. The premise is simple: we already use cards and Mobile Phones
to pay using NFC terminals, why not integrate that same technology in a easier to carry form factor? 
So when I came across Michael Roland and Josef Langer's paper: _Cloning Credit Cards: A combined pre-play and downgrade
attack on EMV Contactless_, I couldn't keep my eyes off it. 

Usually, contactless cards operate in EMV mode: a secure, modern method 
that uses cryptography to guarantee the card is authentic. Of course, MasterCard is old, and this method hasn't been around forever.

Before NFC, payment cards operated with a magnetic stripe: this is the black band that allows you to swipe your card to pay.
But this method is very insecure: anyone who reads the magnetic stripe can simply copy its static data, which is not even encrypted, and make a perfect copy of your card
(you heard me. Avoid getting cards with physical magnetic stripe).
Card companies knew this was a disaster waiting to happen. To fix it, they introduced the chips and convenient
tap to pay systems we use today: EMV mode. This method is basically bulletproof, using cryptography to prove 
your credit card is genuine and that the transaction untampered with.

But you can't just upgrade every cash terminal and register on the planet overnight.

To bridge the gap between old swipe registers and contactless tap to pay, 
we created a temporary solution called Magstripe mode. When you used an early contactless card in a reader without EMV capabilities,
they would both compromise and use Magstripe mode, and the card would wirelessly send the same data found on a magnetic stripe. 
And to stop people from just recording that signal and using it later, we added a safeguard: a dynamic security code. Completely random, completely secure

Except of course, it wasn't.

Here's how the trick works: use a compromised payment terminal (or in our case, and Android app) to communicate with the card. 
The app will play dumb, advertising that it doesn't have EMV capabilities and forcing the credit card to default to Magstripe mode.
This is the first part of the attack, the downgrade.

Afterwards, the app asks the card for a challenge to prove it's authentic. This is the dynamic security code, and it works like this:
the app sends a key, the card answers with a number that is a function of that key. This is what proves it's real. 
But our app doesn't stop there. It keeps sending keys and retrieving the answer numbers, which will later use to pass as the real card.
One would assume it takes hours to map all the keys to numbers this way, but in reality, cards are often limited to 10.000 keys, some of them less.
So this process is done in seconds.

Once the malicious app has mapped all the key - number combinations, it can again use its NFC capabilities to simulate being the original credit card, except
it doesn't advertise EMV capabilities. Once connected to a reader, they both default to MagStripe, and the app (or the theoretical ring where such an app could be loaded)
answers the challenge with its pre-cloned map of keys. This is the replay attack.