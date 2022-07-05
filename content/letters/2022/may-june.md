---
title: "Zig is becoming more production-worthy"
date: 2022-07-04T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/177217687-b47d897a-2516-4df8-b0df-de120552fc53.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/177217687-b47d897a-2516-4df8-b0df-de120552fc53.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/177217687-b47d897a-2516-4df8-b0df-de120552fc53.png"></img></a>

# How Zig is used at Uber

<a href="https://www.youtube.com/watch?v=SCj2J3HcEfc">
    <img width="650px" src="https://user-images.githubusercontent.com/3173176/177207028-843df8cd-4638-487d-9916-997ac888295b.png"></img>
</a>

At the start of the year the Zig Software Foundation [recieved](https://ziglang.org/news/financials-update/) a small ~$50k USD support contract from Uber.

In this talk, Uber engineer Motiejus Jakštys describes developing bazel-zig-cc, a drop-in C/C++ toolchain for Bazel using Zig, how he onboarded Uber to use it, as well as how Google and CloudFlare also appear to be using it.

If you liked that, be sure to check out these articles:

* [Building SQLite with CGo for (almost) every OS](https://zig.news/kristoff/building-sqlite-with-cgo-for-every-os-4cic) 
* [ZGo: Calling Zig from Go](https://www.reddit.com/r/Zig/comments/usm1ku/zgo_calling_zig_fnostage1_from_go/).
* [Testing and building C projects with Zig](https://renato.athaydes.com/posts/testing-building-c-with-zig.html)

# Stage2 compiler rapidly approaching

<a href="https://twitter.com/andy_kelley/status/1542667210602057728"><img width="594" alt="image" src="https://user-images.githubusercontent.com/3173176/177212829-f859c9e0-7390-4689-8283-ca62e00cd7bf.png"></a>

The multi-year effort to switch away from Zig's old stage1 C++ compiler to the new stage2 compiler written in Zig has really been progressing recently. ([tracking issue #89](https://github.com/ziglang/zig/issues/89))

Although it's not ready for prime time yet, and not advised to test with it yet as many bugs are already known, we're already seeing [it can compile parts of some major projects with a bit of finangling](https://github.com/hexops/mach/issues/180).

### Here's why stage2 is such an important milestone

* Once the compiler is written in Zig, a large portion of the community that wouldn't have been able/willing to dive into a C++ codebase before will now be able to help out.
* It will fix _numerous_ known issues, especially around comptime - enabling some new interesting ways of using Zig metaprogramming.
* The core team will then be able to begin thinking about:
  * Major language changes & what 1.0 might look like in the future
  * Exploring adding more safety to the language
  * Stabilizing the standard library
  * Exploring hot-code-swapping
  * Other performance wins

# "Porting my game to the web"

<a align="center" href="https://user-images.githubusercontent.com/3173176/177208004-6d81933c-004e-4643-a20f-60f9bfd6f065.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/177208804-dc723209-c957-44ec-bc4c-945b2885f779.png"></img></a>

Samarth Hattangady wrote [an excellent article of their experience](https://zig.news/samhattangady/porting-my-game-to-the-web-4194) porting their game to the web using Zig's WASM support and WebGL.

They're looking for playtesters, so be sure to download the game on [itch.io](https://chapliboy.itch.io/pirates) and give your feedback if it looks interesting to you!

# Major Zig conference in Milan, Italy

This is a conference you don't want to miss: [SYCL 22](https://sycl.it) (Oct 7-10):

> Software You Can Love, _a conference that celebrates the art of creating software for humans_

![image](https://user-images.githubusercontent.com/3173176/177196710-139bef76-3aa2-4148-a7c4-4758ecef8b85.png)

It's a new conference being ran by Loris Cro (VP of Community) and will be held in Milan, Italy, Oct 7-10, and features:

* Keynote speech from Andrew Kelley, a talk from Richard Feldman (remote)
* **Full day of Zig talks**
* Mi*LAN* PARTY day, where people behind popular community projects like the Zig Embedded Group, etc. will be chatting in a casual LAN-party-like setting
* SYCL Talks - The heart of the conference: Software You Can Love.
* Workshops

Full schedule will come out soon, and early bird pricing ends soon so [get your tickets now](https://sycl.it/tickets)!

# Article of the month: "How I built zig-sqlite"

["How I built zig-sqlite"](https://rischmann.fr/blog/how-i-built-zig-sqlite) is an excellent read for anyone looking to get a better understanding of Zig's C interoperability as well as its powerful meta-programming capabilities.

# Cosmic JS/WASM runtime developments

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/177211171-f3e875a8-d4be-45b4-b6ca-dde75dbd7f15.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/177211171-f3e875a8-d4be-45b4-b6ca-dde75dbd7f15.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/177210929-824f7ef5-6707-4623-8371-3fbd2eb1ba67.png"></img>
    </a>
</video>

What if you could develop native applications in JavaScript or WASM, with a runtime that is not Electron? [Cosmic](https://github.com/fubark/cosmic) is one answer to that, and a project to keep an eye on for sure:

> a general purpose runtime for Javascript and WASM.
> 
> It aims to have broad applications by exposing native cross platform APIs: window management, 2D/3D graphics, UI widgets, filesystem, networking, and more.

It recently gained [3D model rendering via Vulkan](https://www.reddit.com/r/Zig/comments/v9mf32/vulkan_and_3d_graphics_in_cosmic/), [Text and UI](https://www.reddit.com/r/Zig/comments/ux95c8/updates_to_cosmic_graphics_text_ui/), 3D animation, lighting, and PBR support (among other things):

# Ecosystem

[AllYourCodeBase.com](https://allyourcodebase.com/) was launched as a sort of "are we X yet" for Zig, I helped contribute an excellent overview of the [Zig gamedev ecosystem](https://allyourcodebase.com/gamedev/) - check it out and contribute information to it, as well!

## Project highlights

* [zigimg](https://github.com/zigimg/zigimg) continues to get improvements, with support for JPEG, PNG, QOI, TGA and more image formats.
* An IntelliJ and CLion Zig Support plugin, version 0.0.6, [was released.](https://zig.news/marioariasc/zig-support-plugin-for-intellij-and-clion-version-006-released-o68)
* [Easily create TUI programs with zig-spoon! (project demonstration)](https://zig.news/lhp/easily-create-tui-programs-with-zig-spoon-project-demonstration-4k33) by Leon Henrik Plickat showcases their new library for terminal UIs!
* [websocket.zig](https://twitter.com/karlseguin/status/1530558941758795776), a websocket server passing all (important) autobahn tests has been released!
* [ziglua](https://github.com/natecraddock/ziglua) was released, which "takes advantage of Zig's features to make it easier and safer to interact with the Lua API."

## Article highlights

* An excellent article on how to [build an IoT App with Zig and LoRaWAN](https://zig.news/lupyuen/build-an-iot-app-with-zig-and-lorawan-5c3m) was written by Lup Yuen Lee
* ["Testing Zig for embedded development"](https://www.reddit.com/r/Zig/comments/viuiup/the_missing_bit_testing_zig_for_embedded/), an excellent article contrasting Zig and Rust for embedded development.
* xq's ["Cool Zig Patterns" series](https://zig.news/xq/cool-zig-patterns-305o) has continued, covering generics over array length, stable main loops, configuration parameters, and type identifiers.
* ["Zig's var and const for JavaScript devs"](https://zig.news/guidorice/zigs-var-and-const-for-javascript-devs-3899) was published by Alex G Rice.
* ["An Intro to Zig's checkAllAllocationFailures"](https://www.reddit.com/r/Zig/comments/vll04j/an_intro_to_zigs_checkallallocationfailures/) detailing a strategy for testing OOM failures in Zig
* zig-gamedev [May 2022](https://github.com/michal-z/zig-gamedev/wiki/Progress-Reports#may-2022) and [June 2022](https://github.com/michal-z/zig-gamedev/wiki/Progress-Reports#june-2022) progress reports were released, featuring [a cross-platform physics demo/sandbox](https://www.reddit.com/r/Zig/comments/vc1q2g/crossplatform_physics_demosandbox/), [a cross-platform PBR & IBL sample](https://www.reddit.com/r/Zig/comments/utunok/ziggamedev_new_crossplatform_sample_application/), and new libraries for model loading, GUI, and audio - a great set of bindings for popular C libraries like imgui and mini-audio.
* Mach engine's [v0.2 roadmap](https://github.com/hexops/mach/issues/355) was published, and we began planning [the high-level application API](https://twitter.com/slimsag/status/1536189712821456897), ECS type safety, audio systems, WebAssebmly support & more.

# Changes to zigmonthly

As demands on my time and motivation shift over time, publishing zigmonthly on a regular cadence is.. challenging, to say the least.

* I work 40-60 hours a week [at a 200+ person startup](https://about.sourcegraph.com) directly reporting to the CTO, during tricky economic times.
* I do my best to get 40+ solid hours a week into a life-long passion project: the [Mach game engine](https://machengine.org/).
* I take care of what could be described as a small cat shelter.

I believe something like Zigmonthly should exist. It should be more than just a link aggregator, it should be a community update crafted with care and love. Behind the scenes, this involves a *lot* of work, and I haven't always been true to that statement: (a) it's not always clear when the best time to feature projects is, so I have to coordinate with project maintainers. Curating content and deciding if it's representative of the quality we all want of Zig, and making the tough call of when to exclude something, while trying to acknowledge my biases - is all very time consuming and challenging.

I do this work because nobody else is, and I want something like zigmonthly to exist for the community.

To make my life easier, and to improve the quality of zigmonthly, I'm adopting a bi-monthly schedule. Hopefully this gives me more time to focus on [Mach engine](https://machengine.org), more weekends where I can sit down and prepare these to publish on time, and give me a better selection of the highest quality content from the Zig community to go into these articles. The next one will go out *sometime* in September and cover July-Aug.

I'm also adopting a new format: orienting the articles more around _new and highly-notable developments that should be highlighted_, rather than speaking so much about _incremental developments to established projects_ (excluding the Zig project itself.) I want these to be things that get people excited about what is going on in Zig, not a dump of links.

The idea is that if you have a new project, if you wrote a new application in Zig, etc. and you'd like everyone to be aware of it - then you can use zigmonthly to 'launch' it to 600+ readers and build your own audience/community from that. Updates to established projects (like say Mach or zig-gamedev) will still be mentioned, they'll just be footnotes briefly summarizing (and linking to) their own status reports.

# Thanks for reading

If you like my work, you can be one of the 9 people needed to [help me reach my goal of 50 sponsors on GitHub](https://github.com/sponsors/slimsag) and I'll forever appreciate you.
