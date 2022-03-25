---
title: "Zig monthly, November 2021: Pixel art editor, meetup talks, Advent of Code & more"
date: 2021-12-07T18:56:50-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/145131946-c52acf12-5859-4210-a1c1-fa67af567129.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/145131946-c52acf12-5859-4210-a1c1-fa67af567129.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/145131946-c52acf12-5859-4210-a1c1-fa67af567129.png"></img></a>

# Mini Pixel: a tiny pixel art editor written entirely in Zig

[@captainhorst](https://twitter.com/captainhorst) just released [Mini Pixel](https://fabioarnold.itch.io/mini-pixel):

> It's a tiny pixel art editor for Windows (for now?) inspired by the likes of IDraw3 and Graphics Gale. I've written it entirely in Zig. The GUI is done from scratch and inspired by Windows 95 or more recently Serenity OS :^). All the graphics and especially the icons are vector based. So, if you have a nice high resolution screen everything stays sharp. [...]

<a align="center" href="https://user-images.githubusercontent.com/3173176/144981141-f4c157e0-1599-4855-a97c-7264b1c273f8.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144981141-f4c157e0-1599-4855-a97c-7264b1c273f8.png"></img></a>

[Get it for free on itch.io now to try it out](https://fabioarnold.itch.io/mini-pixel), or [check out the code on GitHub](https://github.com/fabioarnold/MiniPixel)!

# Handmade Seattle talks, demos & podcasts

[Handmade Seattle](https://www.handmade-seattle.com/), the Independent Systems Programming Conference was held with numerous Zig attendees from around the world meeting for the first time in person, with board games and discussions late into the night in the hotel lobby - truly a great time:

<a align="center" href="https://user-images.githubusercontent.com/3173176/144971958-3a3d867a-107c-4e59-8d81-55386be60f36.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144971958-3a3d867a-107c-4e59-8d81-55386be60f36.png"></img></a>

(image credit: [@croloris on Twitter](https://twitter.com/croloris/status/1460696987960025090))


Highly suggest checking out all of [the Handmade Seattle talks](https://media.handmade-seattle.com/) if you haven't already. Some Zig highlights:

_"A Practical Guide to Applying Data-Oriented Design" - Andrew Kelley (talk)_

<a align="center" href="https://media.handmade-seattle.com/practical-data-oriented-design/"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144972765-e16f80e5-3c64-49c2-a3e8-558138df2023.png"></img></a>

_"The ZLD Linker" - Jakub Konka (demo)_

<a align="center" href="https://media.handmade-seattle.com/zld/"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144973106-f5f7477b-aedc-4283-a18b-49c93e3f323a.png"></img></a>

_"The race to replace C and C++" - Andrew Kelley, Ginger Bill, and Mason Remaley debating the merits of Zig, Odin, and Rust respectively. (podcast)_

<a align="center" href="https://media.handmade-seattle.com/the-race-to-replace-c-and-cpp-2/"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144973530-b714129d-c9be-4256-b9a5-86ed6b0e6d50.png"></img></a>

# Rem: a full-blown HTML parser in Zig

[@chwayne](https://github.com/chwayne/rem) has made a ton of progress on [Rem](https://github.com/chwayne/rem) - now a full-blown HTML parser in Zig:

> A while ago I shared an HTML parser that I was making. Only the tokenizer worked at that time, but I've made a lot of progress in the last few months, and it's now a full-blown parser!

# zig-gamedev gains Bullet physics and more

[@MichalZiulek](https://twitter.com/MichalZiulek) continues his full-time work on [zig-gamedev](https://github.com/michal-z/zig-gamedev), an impressive project focused on gamedev using Zig, Windows 10+ APIs and DirectX 12. This month he released v0.2.0, bringing Bullet physics [among other goodies](https://github.com/michal-z/zig-gamedev/wiki/Progress-Reports)-check out the new [physics demo on YouTube](https://www.youtube.com/watch?v=9Ri6xS2-9k8):

<a align="center" href="https://www.youtube.com/watch?v=9Ri6xS2-9k8"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144975676-4ddcf784-d8d6-4263-89a7-330920c185b8.png"></img></a>

Michal works full-time on zig-gamedev, so keep an eye out for more from him and [consider sponsoring him on GitHub](https://github.com/sponsors/michal-z)!

# Using Zig with Cypress STM32 microcontrollers

Arwalk has written up an interesting tutorial on [how to use Zig with Cypress STM32 microcontrollers](https://blog.arwalk.net/posts/zig_for_cypress_stm32/).

# Avokadoen's Zig+Vulkan gamejam submission

[@Avokadoen](https://github.com/Avokadoen) participated in a ~1 day gamejam using [nothing more than Zig and Vulkan](https://github.com/Avokadoen/gamejam-zig-vulkan), producing this hilarious depiction of +2k sprites battling it out:

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/144976657-4b57f964-3040-4909-8a1a-99526dd53e85.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/144976657-4b57f964-3040-4909-8a1a-99526dd53e85.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/144976534-a71e3410-056b-46ff-8440-79af7bd3f8c3.png"></img>
    </a>
</video>

# Zig compiler progress

Austin Rude has enhanced the https://ziglang.org/perf performance dashboard:

<a align="center" href="https://user-images.githubusercontent.com/3173176/144986700-4eb53892-a26c-4d57-968a-db04d93a02f5.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144986700-4eb53892-a26c-4d57-968a-db04d93a02f5.png"></img></a>

Meanwhile, Andrew Kelley continues regular progress reports for the development of the self-hosted Zig compiler [on Twitter](https://twitter.com/andy_kelley/status/1467652028159561728?s=20):

> Thanks to great work from Luuk de Gram, WASM joins the progress bar!
>
> Zig self-hosted compiler progress report:
> * 153,862 lines of code
> * Behavior Tests Passing:
>   - LLVM backend: 467/1072 (44%)
>   - C backend: 234/1072 (22%)
>   - WASM: 135/1072 (13%)
>   - ARM, x86: 0/1072 (0%)

Additionally, the Zig v0.9 release is rapidly approaching-it will include numerous bug fixes and improvements-so [keep an eye out for that coming soon](https://twitter.com/ziglang)!

# Zig on the Oculus Quest (proof of concept)

[@SpexGuy](https://github.com/SpexGuy) has created a repository with an example of how to create a minimal Oculus Quest app in Zig. Although just a proof of concept and not suitable for production use, it's a very compelling idea-[check it out on GitHub and consider contributing to the project yourself!](https://github.com/SpexGuy/Zig-Oculus-Quest)

<a align="center" href="https://user-images.githubusercontent.com/3173176/144982632-4574fd93-766c-4619-90f6-9b0e11e3dfc4.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/144982632-4574fd93-766c-4619-90f6-9b0e11e3dfc4.png"></img></a>

# Learn Zig by joining the Advent of Code

If you've been waiting for the perfect time to try and learn Zig, I highly encourage joining the several people who are doing the [Advent of Code](https://adventofcode.com/2021) in Zig

> Advent of Code is an Advent calendar of small programming puzzles for a variety of skill sets and skill levels that can be solved in any programming language

Here are a few ways you can join in:

* [Join the Zig Programming Language Discord](https://discord.gg/gxsFFjE) #advent-of-code and #zig-help channels.
* Follow [@nektro](https://twitter.com/nektro) on Twitter and Twitch, who is [streaming her answers in Zig on most days.](https://twitter.com/nektro/status/1466016831483756545)
* Join a Zig leaderboard and discuss [on Reddit](https://www.reddit.com/r/Zig/comments/r2yedk/advent_of_code_2021/)

And don't forget to add yourself to the [Zig user community world map](https://github.com/zig-community/user-map) if you decide to stick around in the community :)

# A brief note from me

The November issue of zigmonthly was delayed due to me getting ~~COVID?~~ superflu?, I'm much better now, but sorry for the delay!

When I started zigmonthly just a few months ago, my only goal was to bring more attention to the really awesome work that I kept seeing people post in Discord, on Twitter, etc. and aggregate it for people like myself who, when looking at Zig for the first time, may not be able to get a super clear picture of just how many people really are using Zig today.

Today, zigmonthly goes out to over 400+ subscribers and has had [16,000+ viewers](https://opendata.hexops.com/zigmonthly.org?period=12mo). It absolutely means the world to me that this has been able to draw more attention to the awesome work everyone is doing in Zig-so thank you for reading!

---

If you like my work on zigmonthly, Mach engine, etc. consider [sponsoring me on GitHub](https://github.com/sponsors/slimsag) so I can do even more of it!
