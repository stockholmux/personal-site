---
layout: post
title: "Use SemVer."
date: 2023-03-08 01:01:01
categories: versioning semver
image: /assets/usesemver.jpg
---

I'd be really curious to see how many projects that say they use SemVer actually follow the semantics. Unlike many specifications in the technology world, the spec is remarkably clear and short. If you haven't read it yet, go do it now. It'll take you 10 minutes.

From my perspective, it's all or nothing: either you follow SemVer or you don't. If you don't that's _totally_ fine too, but don't say you do. Do what you need to do where the spec is silent, but don't make alterations or exceptions to the spec for your project.

Why is this a big deal to me? Adhering to SemVer is a way of showing empathy to the people who use your software. Those three numbers communicate a whole lot of information. With that information and adhering to the spec, your allowing your users to not have to think (and waste their precious time) to understand your release. They can build automations and write policies on how to deal with updates. Installing a patch is a practical noop, there isn't anxiety on balancing having up-to-date software versus software that doesn't act the way you expect it.

I once had a conversation with a user in the financial services industry. He told me "I love that your project uses SemVer but I wish your project didn't release so many minor versions." This puzzled me and I responded "Minor versions add new features, don't you want new features?" He went on to explain to me that I was missing the point: his organization took security and stability very seriously and every new minor version required a review and sign-off. For him, rolling out a new patch version that contained a feature could have serious repercussions since that's not organizationally allowed to happen. 

Similarly, throwing someone a patch or minor version that has a breaking change is a day-ruining curve ball. Your users are busy and want to install the software that enables them to do more or be safer, but they have to trust what you communicate. Kicking off an update that is supposed to be benign but realizing after the fact that something is intentionally broken by the release is a great way to evaporate that trust.

Finally, users might be in a situation where they can't upgrade to a new major version (we've all been here). Taking the stance that your software has so many new features that you're going to rev the major even though it's not a breaking change also means that you're needlessly withholding those features from users. For what? Some sort of marginal marketing gain?

It's so easy to lose sight of the relationship that is silently forged between the teams making software and those using it. Sometimes we get rare chances to speak directly, but more often we're communicating through things like clear versioning, documentation, schemas, and API parameters. If we keep user empathy center, we're sure to build some great software.   