---
layout: post
title: "The Fair Games"
date: 2016-11-01 21:13:00 +0000
author: HeadCrash
categories: thinks hacking windows raspberry-pi
---

# The Fair Games

> Hacking yourself for jollies

![Tonight we're going to party like it's 1999](http://i.giphy.com/edl5t7nDVPtC.gif)

[Carolyn Meinel](https://en.wikipedia.org/wiki/Carolyn_Meinel) became infamous for her books Überhacker in 2000 and its follow-up Überhacker II in 2003 which laid bare the tools that turn-of-the Century black-hat hackers had been utilising for years to break into Windows machines. She became a target for the whole hacking community because of her books but of course eventually the community moved on to new tools, new methods, and eventually forgot their enemy. I have both of those books on my shelf and have often wondered what it was like to hack in the 90s. To find out I'll need a pair of machines to hack.

With the opensource hypervisor [QEMU](http://wiki.qemu.org/Main_Page), some clever folks over at the Raspberry Pi forums [1](https://www.raspberrypi.org/forums/viewtopic.php?p=123023#p123023),[2](https://www.raspberrypi.org/forums/viewtopic.php?p=123049#p123049), and the Windows 9x Project I plan to spin up a pair of images.

There's very little sense in exposing my internal network to a pair of old, untouched, unpatched OSs, virtualised or not so I plan to sandbox them on the same network that doesn't have an Internet exit node. This will be provided by an old DSL router I was left with after changing providers. I may even packet sniff my way onto that network to give it the full flavour.
