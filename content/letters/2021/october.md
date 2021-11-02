---
title: "Zig monthly, October 2021: Games, gamedev, Elixir, tools & more"
date: 2021-11-2T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/139949770-9002e36d-3c00-447c-a9ab-b9f52c251b28.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/139949770-9002e36d-3c00-447c-a9ab-b9f52c251b28.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/139949770-9002e36d-3c00-447c-a9ab-b9f52c251b28.png"></img></a>

Wow! So much has happened over the last month in Zig that it's been downright overwhelming, let's dive right in!

# Digital Scavenger (game)

[Felix "xq" Queißner](https://github.com/sponsors/MasterQ32) - you may recall his [Android support](https://zigmonthly.org/letters/2021/september#android-support) in the last zigmonthly. He's back, and this time sharing an early gameplay video of his Digital Scavenger game prototype:

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/139792411-55d711fe-3504-44bd-9f04-79f944cf4c83.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/139792411-55d711fe-3504-44bd-9f04-79f944cf4c83.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/139793155-c6ef5256-be38-421f-847e-4909369fd30c.png"></img>
    </a>
</video>

As he [writes on Twitter](https://twitter.com/ikskuh/status/1455225369804562434):

> Full feature showcase of my current gamedev project. Most of the stuff started to come into reality in the last week and everything is still just a prototype.
>
> It's built with Zig, OpenGL ES 2.0 and a lot of love, also uses Box2D.

I highly encourage [checking out his other work.](https://github.com/sponsors/MasterQ32)

# Cross-platform Elixir applications using Zig

[Quinn Wilton shared](https://twitter.com/wilton_quinn/status/1453152473112145928) Burrito, a project by [@doawoo](https://twitter.com/doawoo) which uses Zig to enable building cross-platform Elixir applications

> I'm thrilled to open source work we've done to support building cross-platform Elixir applications!
>
> We're using this code in production to distribute command-line applications to on-premise customer environments, without an installed Erlang runtime.

It is accompanied by an excellent talk at ElixirConf 2021 [which you can watch here](https://www.youtube.com/watch?v=lDfjdGva3NE&list=PLqj39LCvnOWZna91xJ_i44g3rx4Brbpnv).

_**EDIT:** Updated to clarify the project is by [@doawoo](https://twitter.com/doawoo) (Quinn: ["I just want to make sure to credit @doawoo
 for Burrito. I was involved, but it's really their project."](https://twitter.com/wilton_quinn/status/1455653326129807362?s=20))_

# zig-gamedev project

[@michal-z](https://github.com/michal-z), independent graphics programmer & ex-AMD/Frostbite/EA DICE/Intel engineer shares the [zig-gamedev project](https://github.com/michal-z/zig-gamedev):

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/139600261-8c424980-afeb-4774-8ec9-aa8e5eca3662.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/139600261-8c424980-afeb-4774-8ec9-aa8e5eca3662.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/139793223-f3a68592-7d05-4355-a2ee-867e12b9d077.png"></img>
    </a>
</video>

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/139600273-f2fbd11c-dfa3-4f6a-b1c0-fab486332e82.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/139600273-f2fbd11c-dfa3-4f6a-b1c0-fab486332e82.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/139793304-13e225c5-6a8b-4ff7-b59b-e7707b88d841.png"></img>
    </a>
</video>

He recently [left a highly paid position at AMD](https://twitter.com/MichalZiulek/status/1447830542330826752) to work on his own indie game written in Zig. As a first step to build a full game he has created an open-source project called [zig-gamedev](https://github.com/michal-z/zig-gamedev). This project contains growing collection of sample applications, libraries and other tools for game developers using Zig. The goal of the project is to build necessary technology, share knowledge, help others and promote the language. He works on it full-time, so [please consider supporting Michal on GitHub](https://github.com/sponsors/michal-z).

> I build game development stuff in Zig full-time. If you like my work and my mission to promote the language, please consider supporting me.  I will create more sample applications, libraries and complete mini-games. I have game development knowledge and experience and I want to share it with others by writing open-source software in Zig.

# Fuzz testing

Ryan Liptak shared an [excellent article](https://www.ryanliptak.com/blog/improving-fuzz-testing-with-zig-allocators/) on improving fuzz testing using the AFL fuzzer with Zig allocators. 

# Zig snapshots debugger

[@kubkon](https://github.com/kubkon), the Zig core team member working on the Zig linker, announced [zig-snapshots](https://github.com/kubkon/zig-snapshots) - an interactive debugging tool allowing you to preview snapshots of Zig's incremental linker progression between subsequent incremental updates:

<a align="center" href="https://user-images.githubusercontent.com/3173176/139801303-7fc75638-61ab-4401-a285-68d9ca380052.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/139801303-7fc75638-61ab-4401-a285-68d9ca380052.png"></img></a>

# Zig self-hosted compiler progress

Andrew Kelley is [sharing regular progress updates](https://twitter.com/andy_kelley/status/1448869273431011330) on the Zig self-hosted compiler, which is a major milestone for Zig:

> Zig self-hosted compiler progress report:
> * 140,331 lines of code
> * Behavior Test Suite:
>   - LLVM backend: 365/1057 (35%) passing
>   - C backend: 42/1057 (4%) passing
>   - arm and x86 backends: work in progress towards the first passing test case

Zig self-hosted https://twitter.com/andy_kelley/status/1448869273431011330

# GLFW bindings

This one from yours truly. I've announced [mach-glfw](https://github.com/hexops/mach-glfw): Ziggified GLFW bindings with 100% API coverage, zero-fuss installation, cross compilation, and more as well as a [Vulkan example](https://github.com/hexops/mach-glfw-vulkan-example) to go along with it. This one small step towards [my vision for Mach engine](https://devlog.hexops.com/2021/mach-engine-the-future-of-graphics-with-zig).

Learn more: [Perfecting GLFW for Zig, and finding lurking undefined behavior that went unnoticed for 6+ years](https://devlog.hexops.com/2021/perfecting-glfw-for-zig-and-finding-undefined-behavior)

<a align="center" href="https://user-images.githubusercontent.com/3173176/139573985-d862f35a-e78e-40c2-bc0c-9c4fb68d6ecd.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/139573985-d862f35a-e78e-40c2-bc0c-9c4fb68d6ecd.png"></img></a>

# Using Zig and translate-c to understand weird C code

Over on zig.news, [Sobeston](https://zig.news/sobeston) has published [a very interesting article](https://zig.news/sobeston/using-zig-and-translate-c-to-understand-weird-c-code-4f8) walking through how they use Zig's translate-c functionality (which converts C code to Zig code) to understand what a strange C code snippet is doing. Very much worth the read.

# Andrew Kelley on the Sourcegraph podcast

Recently I got the opportunity to join Andrew Kelley on the Sourcegraph podcast through my dayjob (I work at Sourcegraph), it's a high-level chat around why Andrew built Zig, the challenges in doing so, how programmers can get funding for their side projects and hobbies, the differences between Zig and C, and why and how Zig can be faster than both C and Rust. Check it out on YouTube below or [read it here](https://about.sourcegraph.com/podcast/andrew-kelley/).

<a align="center" href="https://www.youtube.com/watch?v=gn3YsZ6HUHw"><img width="650px" src="https://user-images.githubusercontent.com/3173176/139802947-59c266c7-8caf-4fe2-b6a0-2d8dd7dc909c.png"></img></a>

# Sat November 6th: Zig SHOWTIME!

We're just a few days away from the next Zig SHOWTIME episode. Join live by going to https://zig.show for more info, or [subscribe to the Zig SHOWTIME calendar](https://calendar.google.com/calendar/embed?src=8a028atr03arr440lsqp4a5tls%40group.calendar.google.com&ctz=Europe%2FRome&utm_source=ZigSHOWTIME&utm_medium=email&utm_campaign=zig-rush-zig-showtime-30) ([iCal](https://calendar.google.com/calendar/ical/8a028atr03arr440lsqp4a5tls%40group.calendar.google.com/public/basic.ics?utm_source=ZigSHOWTIME&utm_medium=email&utm_campaign=zig-rush-zig-showtime-30)) to have all episodes automatically added to your calendar.

# Nov 11-12th: Handmade Seattle conference!

Whether you join remotely or in-person, [Handmade Seattle](https://www.handmade-seattle.com/), the Independent Systems Programming Conference is here!

Several members of the Zig community are joining both online, and in person (myself included). The conference will also feature talks by Andrew Kelley, 

Andrew Kelley and others in the Zig community will also be giving talks and demos, so you won't want to miss it!

---

Zigmonthly recently surpassed 300+ subscribers and 7k+ viewers, and this is just the third article! Thanks so much for reading and being a part of this!

If you like my work, you can [sponsor me on GitHub](https://github.com/sponsors/slimsag)

