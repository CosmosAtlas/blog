---
title: "Nds Flash Card in 2021"
date: 2021-05-30T01:54:27+08:00
author: "Wenhan Zhu (Cosmos)"
cover: ""
tags: 
- "nds"
- "gaming"
keywords:
- ""
- ""
description: ""
showFullContent: false
draft: false
---

> TL;DR: Skip to "How to choose your flash card" section

## Why this post

This is a reflection of my past 2 months of research on NDS flash cards.
I wanted a new flash card to enjoy some NDS games, however, the journey wasn't
quite smooth as I thought. I'll document the stuffs I learn, so you don't need
to go through what I did.

Disclaimer: Every card mentioned below unless stated specifically, I own the
card at one point.


## What is a flash card

Flash cards for NDS are basically ways to run any `.nds` file you want. The
most common use is probably just pirating games. Duh... Due to the availability
currently on NDS titles, it's also probably your best bet to play many NDS
games.

## Brief background on NDS flash cards

NDS flash cards have long exists since the beginning of the NDS life cycle.
Noticeably it has gone through a few generation of advancements that still have
some impact today.

The most important information to know if the compatibility of the flash cards
with the different systems. The first two versions of the NDS (namely, the
original NDS, also nicknamed the NDS phat and NDS Lite) do not have firmware
updates. Which means that any half decent flash card will have no issues
running on this machine. On the other hand, the last revision of NDS system,
the NDSi (also its large version NDSiXL or NDSiLL in Japan) do have firmware
updates. So not every flash card is compatible with the console, and for some
flash cards, they are only compatible with previous system versions.

With the difference in NDS systems in mind, it is very important to make sure
that you get a flash card that your system supports. However, a good news here
is if you are willing to install custom firmware (CFW) on your system (which is
quite easy to do and have minimal risks), this is not a problem. With CFW on
your NDSi, you are able to run any flash card with it.

## How do flash cards differ

If you know about NDS flash cards, you probably know that there's many
different versions of the flash card. So how are they different? In the early
days of NDS flash cards, the major selling point of them lies in their
compatibility with games. However, now since no new games are released for the
system and users have created custom menu and anti-privacy patches, it's less
of a problem on game compatibility.

So, back to the problem again, how are they different?! So from a higher level,
these flash cards are different implementations on the same idea by different
teams that made flash cards. So in a way like how many different companies make
Android phones, but when you use an Android phone they are mostly the same
beside same small differences.

## Some detailed differences between flash cards

Currently on the market, whichever flash card you chose, on the surface, you'll
likely essentially end up with two different core/kernels.

* Wood Kernel
* YSMenu

Some flash cards (such as DSTT) can run both, so it provides them with extreme
compatibility with games.

However, two flash cards both running Wood Kernel may not be the exact same
despite they support the same wood version. Since there are limited information
online on why, here is my conjecture based on some readings. Wood kernel was
developed back in the days by one person, however, many flash card makers took
the kernel and further developed on the kernel to make some changes. This can
be reflected by the different flash card launch files even if they both run on
the wood kernel.

So for end users, are there any effects on you? The answer is actually yes. If
you intent to play modified ROMs, sometimes in the form of romhacks and
sometimes in the form of localization (like a fan translation version), you
might get different results on two flash cards with the same wood kernel.

## Buy new

There's currently like only 2 kind of NDS flash cards if you want to buy new.

* A *r4isdhc.com* card with a "bomb" logo in the system. (COM card)
* Some randomly labelled card with a "sword" logo that runs wood. (Wood card)

There is a *gimmik* with the COM card, where the developers implemented
a **time bomb** in the card where after a certain date, you will not be able to
use the card. The time bomb can be solved in two ways, use YSMenu on the card
or set your system date to a time before the time bomb activation date. For me
personally, because of the time bomb, I would avoid this card like if its
a plague.

On the other hand, the Wood card, there is probably a gazillion different
variants of this card, some times the 208-in-1 card sold on ebay, the Ace3DS+
card, or a very popular and often recommended *r4ids.cn* variant of the card.
However, due to the reason I talked about before on the "hidden" variants
between the wood cards, you can't tell before you tried the card on whether
a modified ROM will run. But if you only play with clean ROMs, any Wood card
with the newest kernel (version 1.62 for most and for some reason there's
a 1.64 version exclusive to the *r4ids.cn* wood card) will serve you well.

| Card Name                                                                 | Claimed wood version | modified ROM test |
|:--------------------------------------------------------------------------|---------------------:|------------------:|
| *woodr4isdhc.com* 2021 wood version                                       |                 1.62 |              FAIL |
| *r4isdhc.in* 2014 version                                                 |                 1.62 |           SUCCESS |
| *r4ids.cn* R4I GOLD 3DS (the card most recommended in the fast few years) |                 1.64 |              FAIL |
| All cards in next section with Wood kernel                                |                 1.62 |           SUCCESS |

Note that the year label for R4 cards do not mean anything most of the time
(since 2014).

So, clearly, you really have two sub-par choices here if you want a "perfect"
card, you either by a card knowing it have a time bomb, or you get a wood card
knowing that there's a probability that in the future it won't run on some
modified ROM.

## Buy old cards

So now let's turn our eyes on some old cards. Below are a selection of cards
that works well. However, they do have other issues which I'll go over.

| Card Name    | Compatible with newest NDSi/3DS firmware |                            Kernel | Note                                                                                                    |
|:-------------|-----------------------------------------:|----------------------------------:|:--------------------------------------------------------------------------------------------------------|
| Origin R4    |                                       No |                           YS+Wood | Only supports up to 2GB tf card                                                                         |
| DSTTi        |                                       No |                           YS+Wood |                                                                                                         |
| AceKard2i    |                                       No | AKAIO (what Wood is derived from) |                                                                                                         |
| DSOnei       |                                       No |                               EOS |                                                                                                         |
| DSTWO        |                                      Yes |                     EOS for DSTWO | Have special hardware to play GBA and SNES games. Reduced battery life also due to the special hardware |
| *r4isdhc.hk* |                                      Yes | R4iNP (custom version of YS+Wood) | The year on top left from 2014-2018 are just labels                                                     |

So, in short, DSTWO and a *r4isdhc.hk* card is your best bet for running on any
system and likely have no issues with game compatibility. However, as stated on
the background part, if you are willing to get CFW running on your NDSi/3DS
(which is really easy), the DSTTi, AceKard2i, and DSOnei are also good choices.
And if 2GB does not limit you (which really doesn't matter, the largest NDS
games is ~300Mb), it's also a great choice. On a side note, it is actually
uncommon to see a new branded 2GB tf card in 2021 (probably because even a 32GB
card is dirt cheap these days...).

## How to choose your flash card

I'll ask you two big questions, 

1. If you own an DSi/3DS, do you (want to) run a CFW?
2. Do you plan to play a modified ROM?

| CFW? (Only for DSi/3DS) | Modified ROM? | Recommendation                                        |
|------------------------:|--------------:|:------------------------------------------------------|
|                     Yes |           Yes | DSTTi, AceKard2i, DSOnei, DSTWO, *r4isdhc.hk*         |
|                     Yes |            No | Any card I've mentioned                               |
|                      No |           Yes | DSTWO, *r4isdhc.hk*                                   |
|                      No |            No | One of the wood cards that can run on newest firmware |

## Closing up

Note that until now I did not put prices for any flash card, since these will
change over time and just by some quick searches online you can easily find the
price. However, here I'll put some references on how much a card is compared to
other at the moment.

| Card Name      | Price |
|----------------|-------|
| Origin R4      | ~$10  |
| DSTWO          | ~$60  |
| Any other card | ~$20  |

## Summary

As any piece of information you read online, you should take my writing as
a grain of salt. Think and do your research before you make your decision, and
when you do, make it YOUR decision.

Anyway, for me, I find researching the NDS flash cards and getting the ROMs
organized on a SD card much more fun than playing the games.

Enjoy!
