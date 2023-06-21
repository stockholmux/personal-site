---
layout: post
title:  "3D Printing Needs Open Source More Than Ever"
date:   2023-06-20 08:00:00
categories: oss 3dprinting
excerpt: "Thomas Sanlander's recent video was a bad take. I don't think he proved his thesis (we should embrace closed source products?), but what I think he did do is underline how little the 3D printing industry understands open source and how they're super bad at using it"
---

[Thomas Sanladerer's recent video was a bad take. ](https://www.youtube.com/watch?v=68FkIwCc_eo)

I don't think he proved his thesis (we should embrace closed source products?), but what I think he did do is underline how little the 3D printing industry understands open source and how they're super bad at using it. 

## Free is not equivalent to open source.

In Thomas' video there was a lot of language about someone taking someone else's stuff: this is focusing the argument on the lack of cost ("gratis"). That isn't what makes something open source. The [OSI defines what is open source](https://opensource.org/osd/) and there is a lot more than just not costing anything, it really has to do with the license. 

It seems that companies aren't quite getting it right either. [Sovol SV06's GitHub repo](https://github.com/Sovol3d/SV06-Fully-Open-Source/tree/main) is "SV06-Fully-Open-Source" and, indeed, there is a comprehensive set of source files to it. However, as far as I can tell, this repo has no license, so it's not open source. Sovol's words here also relate some misunderstandings of open source:


> The SV06 was released 2 months ago (Oct.11, 2022) and has gained popularity from lots of customers. To express our thanks to your support, and pay tribute to the community, Sovol makes the fully open source available.



Even [Angus from Maker's Muse says "It's actually open source."](https://youtu.be/PMBmAqkB268?t=715)  I'm going to give Sovol the benefit of the doubt that it's a honest misunderstanding, but right now that IP is in a murky grey area: can you use it? They _say_ it's open source, but there is nothing to say what you can do with it. Open source, done properly, can do far more than focus on one taking something at zero cost, it's explicitly informing others what you, as the creator, allows.  

## Open source projects are not (usually) individual endeavours

This one bothers me a lot. If you take a look at big, important open source projects in other areas, they are mostly done by a coalition of people, often in a neutral foundation ([Linux Foundation](https://www.linuxfoundation.org), [Apache Software Foundation](https://www.apache.org), [Eclipse](https://www.eclipse.org/org/foundation/), [Free Software Conservancy](https://sfconservancy.org), etc). These neutral bodies make it easier to get everyone, even competitors, working towards a mutual good.

It is pretty hard to convince your boss to allow you to start making contributions directly to a competitor who, since they own and completely control the project, can take your hard work and throw it in the bin. However, if there is a neutral body made up of multiple organisations, you have a more clear path to get what _you_ need in the project in a way that benefits _you_. Additionally the neutral body breaks ties and sets up standards of practice to ensure people are treated fairly. 

In 3D printing, most software doesn't work this way. Cura is an Ultimaker project. Prusa Slicer comes from Prusa. Octoprint is Gina. So, of course, people just "take":  there isn't a clear path to contribute in a meaningful way as real peers from a project perspective. Sure, you (as an individual) can throw some code down, but it's quite different when your boss, and potentially your legal team, are dictating the rules.

## The moral argument is a bad justification for open source

Much of the 'pro' open source arguments you'll hear in 3D printing communities, and mirrored by Thomas, are what can be called the 'moral arguments' for open source. This is the idea that "Gosh darn it, open source is the _right thing to do._" I think when he talked about people just not caring in comparison to a new shiny 3D printer, he was referring to people caring about the moral argument. **This is probably the weakest argument for open source both from a personal and organizational perspective**. Sure, it can give a company a little bit of a marketing push to say "Look how nice we are," but the  problem is that companies aren't human and consequently lack capacity for morals. On the personal end, it's a _feeling_ and hard to quantify when compared to cheaper or faster.

What _are_ good arguments for open source revolve around the quality, transparency, and accountability. [More eye-balls on code makes it better](https://www.zdnet.com/article/coverity-finds-open-source-software-quality-better-than-proprietary-code/): transparency and accountability are [extremely effective sanitizers](https://www.mend.io/resources/blog/3-reasons-why-open-source-is-safer-than-commercial-software/). If your GitHub ID is next to a chunk of code, it zaps the opportunity to pull a fast one and sneak in a backdoor or to lay down lower quality code. Additionally, if there are issues with the code, anyone can point it out rather than being obscured in binary form.

We've seen it first hand in the 3D printing world: BambuLab's (proprietary) software was transmitting data in clear (non-encrypted) text, from the [BambuLab Blog](https://blog.bambulab.com/answering-network-security-concerns/):


> The LAN mode was developed in a rush to meet the request of customers who do not wish to connect to the cloud due to seurity concerns. These services are not applied to public network communications. To accelerate the development of LAN mode, we made the erroneous assumption that "the LAN on the user's side is secured", which is not always the case and could lead to potential security risks for the printers within that unsecured network.


and

> File transfers, such as sending 3MF files to the machines, which are indeed being sent through HTTP. 

This was [discovered by a community member](https://web.archive.org/web/20230126200804/https://blogg.karlsbakk.net/2022/11/23/bambu-lab-x1-carbon-the-flipside/) who ran some relatively simple port discovery routines. It came out in November of 2022, after the printer was already on the [market for many months](https://blog.bambulab.com/update-on-the-shipping/). If this had been open source, the community would have discovered it much more quickly. The unanswerable question of closed source software still remains: what else do we not know? 

## The missing boogie man

One thing that is totally missing from the conversation seems to be what happens in the (undefined) future? If you have a closed/proprietary system your future with that device is tied to that company. If they go out of business? Well, I guess you won't get any more updates or support. If they decide to switch to a new line of products and leave that one behind? Too bad. 

Of course there is always the planned obsolescence route: wearing parts that are made by exactly one company in the world, and guess what? They decide to stop making them, but you can get the new shiny printer for only double of what you paid for your last device (oh and they can use intellectual property leverage to stop _others_ from making spares). And there have been countless hobby devices that [required you to use their own consumables](https://youtu.be/Ju99EjfnGco?t=122) due to a [razor-and-blade business model](https://en.wikipedia.org/wiki/Razor_and_blades_model), that is really just a explicit exploitation of the whole proprietary direction.


## Why is it important _now_?

A 3D printer from 5-6 years ago had many of the same components as today: stepper motors, frames, heated beds, nozzles, etc. Sure they have evolved from the hardware perspective, but the mechanical bits are not what is changing rapidly. It's the computing power and software used by the printer.

Early printers had mainboards powered by 8-bit Arduinos with very limited computing power. This quickly evolved into 32-bit ARM based microcontrollers. Microcontroller have no real OS and are flashed to do very specific things. Now, we've evolved into using a microcontroller _and_ single board computers running full blown Linux with network connectivity (e.g. Klipper). This is a huge leap in computing power and complexity. This complexity worries me.

Keeping a Linux machine up-to-date is an ongoing task for the owner. It also requires the vendor of the software to continually be vigilant for things like CVEs and make smart choices about updating dependencies to balance maintaining compatibility and closing security holes. Now, you probably have Linux devices all around you, but most of these consumer devices are tightly locked down and/or maintained by a large company who continually feed updates to it. Or, you have the hobby route, where you have full control and it's your responsibility to maintain it.

3D printer manufacturers have become Linux OS and software vendors and are, let's say, not instilling confidence:

- VoidStarLab reports [FLSUN doesn't provide root and is running out-of-date software](https://youtu.be/KwI4XkB2uQg?t=1606)
- QidiTech has some[ _interesting_ ideas about maintenance and how to modify the software on your machine](https://ca.qidi3d.com/pages/software-firmware)
- Creality is reportedly [refusing to give the source to the K1](https://klipper.discourse.group/t/creality-violating-klipper-license/8990)

And these are all relatively new devices! What happens in 5 years when you try to update the Linux machine inside your 3D printer? There will be un-updated dependencies for the unusual hardware that will not work with the modern, secure bits you can update. Or, predictably, people will just keep on using insecure machines and some bad actors will catch on that they can be exploited, as [has happened with IP Cameras](https://www.securityweek.com/serious-vulnerabilities-found-firmware-used-many-ip-camera-vendors/). Printers are far worse though not only is there a camera but also motors and heaters - I really don't want those things being controlled by someone else.

Then, of course, we have the fully closed systems like BambuLab. It runs [Linux (of some sort)](https://forum.bambulab.com/t/does-bambu-use-any-open-source-software-in-their-firmware/9470/6) but the rest of the software is a bit of a mystery. Is it up-to-date? Anyone's guess. 

## What's the solution then?

There two different roles in this situation. First, you have the companies building printers and software for those printers, and then you have the consumers of those devices.

3D Printing companies need to get serious about open source instead of retreating into the closed world. Setup cross-organisation foundations, work together, let the rising tide lift all benchies. Instead of copy cats of say, the Ender 3, what would happen if there was an open source design born out of collaboration? I'm sure it would be better. Also build a model where neutral bodies can pool money and pay contributors to the foundational software for the whole community (instead of making [individuals developers appeal to the _users_ of the printers](https://fosstodon.org/@marlinfirmware/110574838077047976)).

As consumers, we should ask a lot of questions. Who is maintaining your software suppdevelopersly chain for your firmware? Do you disclose vulnerabilities? Are all these parts user serviceable? I think, as well, we should push the influencers in the space to really focus on these factors rather than the speed of the benchie or the menu layout on the touchscreen. I think we should also move away from the holy wars that push the community into corners: it doesn't matter if you've joined team bambu or will only ever touch a Voron, you have a lot more in common than actual difference.

_(Disclosure: My day job is working with an Linux distribution, but it's totally inappropriate for a 3D printer. These are only my opinions, not my employers.)_







