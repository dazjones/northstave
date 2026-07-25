---
title: "ThinkPad X1 Carbon WWAN"
date: 2026-04-26
description: "Last week I discovered a port cover which turns out is a SIM slot. This got me excited."
tags: ["thinkpad","linux"]
---

Earlier this year, I finally [picked up a ThinkPad X1 Carbon Gen 7](https://northstave.com/posts/behold-the-thinkpad/) to replace my dying Macbook Pro. Last week I discovered a port cover which turns out is a SIM slot. This got me excited.

I immediately wondered if just inserting a nano-SIM would give 4G but I couldn't find any trace of the harware anywhere within Linux. It turns out Lenovo is a bit of a tease here. Every single chassis has the physical tray, but only a handful are actually wired for it. If your machine is pre-wired for it then its classed as WWAN-Ready otherwise its a bit of a faff trying to run and route antenna wires around the screen assembly. A quick google and I realised the only way to tell was to open her up.

Opening an X1 Carbon is actually a decent experience. It is not like some modern laptops held together with glue and proprietry screws. Once I was in, I was looking for two things. An empty M.2 slot and the antennas. If you find those tiny red and blue wires tucked away, you are WWAN-Ready and good-to-go. It means the machine is pre-wired and may or may not have the compatible module installed. If they are not there, you are looking at a total screen disassembly just to route the cables. That is a massive faff and I was not going to bother. Luckily, my antennas were in place, with plastic sleeves covering the loose end connector but no module. Next step was to find a compatible modem module.

Finding that modem can be a headache. You cannot just chuck any old M.2 LTE card in and call it a day. Lenovo uses a BIOS whitelist, which is incredibly annoying. If the part number does not match their approved list, the laptop just ignores it or refuses to boot. Fair enough, I suppose, but it meant digging through old hardware manuals and forums to find the exact Fibocom card with the right FRU. I have finally found one and it is in the post.

The plan is to drop in a prepaid SIM once the card arrives. I am fully prepared to spend a few hours wrestling with ModemManager and those stupid FCC lock scripts to get it working with Linux. But if it works, this thing becomes the ultimate tool for working anywhere.