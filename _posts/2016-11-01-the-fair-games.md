---
layout: post
title: "The Fair Games"
date: 2016-11-01 21:13:00 +0000
author: HeadCrash
categories: thinks hacking windows raspberry-pi
---

# The Fair Games

> Hacking yourself for jollies

![Tonight we're going to party like it's 1999](http://i.giphy.com/MoZ0bsrAgsJAQ.gif)

[Carolyn Meinel](https://en.wikipedia.org/wiki/Carolyn_Meinel) became infamous for her books [Überhacker](https://openlibrary.org/books/OL8610895M/Uberhacker) in 2000 and its follow-up [Überhacker](https://openlibrary.org/books/OL8610904M/Uberhacker_II) II in 2003 which laid bare the tools that turn-of-the Century black-hat hackers had been utilising for years to break into Windows machines.

She became a target for the whole hacking community because of these books. She even used her notoriety to advertise the services of a company who hosted her website who in turn challenged the hackers to deface her site, hosted on their Brickserver system. Of course eventually the community moved on to new tools, new methods, and eventually forgot their enemy.

I have both of those books on my shelf and have often wondered what it was like to actually hack in the 90s. I was into the stories and the culture but was a graphic designer at the time so you can imagine my core technical skills were somewhat lacking.

To actually find out what's possible I'll need a pair of machines to hack.

With the opensource hypervisor [QEMU](http://wiki.qemu.org/Main_Page) and some reading of old VM forums I managed to fairly easily spin up a pair of machines on a stock RPi 3 running Raspbian for Windows 95 with something like:

```
qemu-img create W95 $(( 1024 * 512 ))
qemu-system-i386 -fda FDos.img -cdrom W95_PLUS.iso -hda W95 -m $(( 1024 * 64 )) -boot a
``` 

Bear in mind that it's necessary to format the hda with fdisk from the FreeDos bootdisk as I couldn't make it work using the Windows95b.img file that's available from [AllBootdisks](http://www.allbootdisks.com/download/95.html). You'll have to have physical access to the machine or a combination of SSH and VNC to complete the operation as you can't script the install proccess. Yet.

There's very little sense in exposing my internal network to a pair of old, untouched, unpatched OSs, virtualised or not so I plan to sandbox them on the same network that doesn't have an Internet exit node. This will be provided by an old DSL router I was left with after changing providers. Which was very nice of them. I may even packet sniff my way onto that network to give it the full flavour.
