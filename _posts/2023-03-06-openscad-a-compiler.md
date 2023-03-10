---
layout: post
title:  "Licensing and OpenSCAD projects"
date:   2023-03-06 00:00:00
categories: openscad oss
---

I use OpenSCAD weekly. I've solved a variety of problems with it and, over time, it's the quickest way for me to create a 3D object. It's also just fun for me in way that I don't get from point-and-click CAD. In my spare time, I've probably written thousands of lines of OpenSCAD.

I'm also an open source advocate. It's a great way to share and collaborate. I've released quite a few projects independently and it's part of my job to contribute to open source. 

So, why haven't I released a ton of OpenSCAD code? 

## You're free to use it, you're free to modify it, but…

Attribution is a big part of open source. In [many](https://opensource.org/license/mit/) [popular](https://opensource.org/license/apache-2-0/) [open](https://opensource.org/license/bsd-3-clause/) [source](https://creativecommons.org/licenses/by/4.0/) licenses you're required to give attribution directly or through a copyright line in the license file when you distribute the work in other forms (e.g. as a binary). And that's fair - it provides clarity on who originated it for the lawyers and prevents others from passing off something they didn't create as their own. Additionally, when you're name is in the license it also acts as a low-key advertisement of your abilities.

## So, why is OpenSCAD weird?

In the 3D printing world, models shared on Printables or Thingiverse are typically licensed with something from the Creative Commons family. If you take a look at the Creative Commons FAQ, you'll see [a curious line about where their licenses can be used](https://creativecommons.org/faq/#what-are-creative-commons-licenses):

> CC licenses may be applied to any type of work, including [educational resources](https://creativecommons.org/education/ "wikilink"), [music](https://wiki.creativecommons.org/wiki/Musician "wikilink"), [photographs](https://wiki.creativecommons.org/wiki/Photography "wikilink"), [databases](https://wiki.creativecommons.org/wiki/Data "wikilink"), [government and public sector information](https://wiki.creativecommons.org/wiki/Government_use_of_Creative_Commons "wikilink"), and [many other types of material](https://wiki.creativecommons.org/wiki/Case_Studies "wikilink"). The only categories of works for which CC does not recommend its licenses are [computer software](https://creativecommons.org/faq/#Can_I_apply_a_Creative_Commons_license_to_software) and hardware.

_Entering "I am not a lawyer" territory_

In my mind, OpenSCAD is unambiguously software: you provide it instructions in a specific grammar and it executes those instructions. Heck, with the customizer, it even has a GUI. 

Here is where it gets weird: you can certainly license your OpenSCAD code with something like MIT, Apache 2.0, or BSD 3 Clause and when someone redistributes the code they have to comply with those terms (and include attribution). It's unclear how that license applies to the _output_, and most interesting bit, the 3D model produced by the code.

If someone downloads your OpenSCAD code with an OSS license, makes a small modification, and uploads just the STL file to, say, Printables, do they need to attribute you? I think common sense would say "yep!" but I'm not sure that's how it works.

I was given an example which refuses to leave my head: You write a Python script that creates a PNG with four circles and a square when it's run file (for argument's sake, the PNG isn't part of the repo). You release the source code under an MIT license. Does the PNG file also have the MIT license? Most people would say no. What if someone takes the script, modifies it, and uses it to create beautiful work of art? Do they need to attribute you if they want to sell framed prints? Nahh, that doesn't make sense.

Admittedly, it seems pretty straightforward in the Python examples but I can't put my finger on what's different about OpenSCAD. 

## What's next?

First, I'd love for someone to tell me a nice, crisp solution to the problem. If there is something I've just missed or misunderstood about this problem, I would rapidly share a lot more OpenSCAD on GitHub. I'd love it if people used and enjoyed my projects. 

Without some license applying to the resulting models of the OpenSCAD code, I worry that malicious actors might pass off my designs as their own, which would irk me. Worse though could be someone claiming that _I _was the one who stole their work. I know it wouldn't be held up but copyright trolls do exist and they feed on content with unclear ownership. I don't need that in my hobby.

What I would love is some sort of license that fits this niche. But legal advice is expensive and the OpenSCAD community is tiny.

In the meantime, you may see me release some OpenSCAD in the form of libraries but probably not much that produces a copyrightable STL. 