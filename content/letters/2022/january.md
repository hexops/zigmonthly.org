---
title: "Zig monthly, January 2022: Lua bindings, stage2 work, gamedev, and tons of new libraries"
date: 2022-01-30T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/153108292-db1f0981-af4d-4537-8032-f18e51a58d1e.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/153108292-db1f0981-af4d-4537-8032-f18e51a58d1e.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/153108292-db1f0981-af4d-4537-8032-f18e51a58d1e.png"></img></a>

# zoltan: a minimalist Lua binding 

This month's showcase mention is [@ranciere](https://github.com/ranciere)'s [zoltan project](https://github.com/ranciere/zoltan), a minimalist Lua binding. Use cases:

* Dynamic configuration of the application (you can handle complex configuration cases which involve logic)
* To support user-defined extensions
* To automate repetitive user tasks (Neovim)
* To develop UI business logic (a lot of games do this)

What struck me [about their blog post](https://zig.news/ranciere/zoltan-a-minimalist-lua-binding-4mp4) was the simplicity of the API:

<a align="center" href="https://user-images.githubusercontent.com/3173176/153103890-323d0dd6-dd45-4f97-8569-f4567a564b1f.png"><img width="400px" src="https://user-images.githubusercontent.com/3173176/153103890-323d0dd6-dd45-4f97-8569-f4567a564b1f.png"></img></a>

<a align="center" href="https://user-images.githubusercontent.com/3173176/153104227-de406a69-1218-4059-931e-20fb12828fb5.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/153104227-de406a69-1218-4059-931e-20fb12828fb5.png"></img></a>

# buztd: Super lightweight process killer

[@vrmiguel](https://github.com/vrmiguel) released [buztd](https://github.com/vrmiguel/buztd), a super lightweight process killer for Linux.

# ZT: ImGui+OpenGL+stb_image+GLFW

Runner up for this month's showcase mention, [@JonSnowbd](https://github.com/JonSnowbd)'s project called [ZT](https://github.com/JonSnowbd/ZT), "A zig-contained library for Windows and Ubuntu that automatically compiles and links ImGui, OpenGL, stb_image, and GLFW into typed packages." which has been in development for over 9 months:

<a align="center" href="https://user-images.githubusercontent.com/3173176/153103202-c428b674-c16c-46b4-9ca6-25a661079b0b.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/153103202-c428b674-c16c-46b4-9ca6-25a661079b0b.png"></img></a>

# minz: Minimal string compression

[@judofyr](https://github.com/judofyr) released [minz](https://github.com/judofyr/minz), a minimal string compressor based on the paper [FSST: Fast Random Access String Compression.](http://www.vldb.org/pvldb/vol13/p2649-boncz.pdf)

Highly suggest checking out [the Reddit discussion](https://www.reddit.com/r/Zig/comments/sa1pnf/minz_minimal_string_compression/) if this interests you.

# Zig compiling and running a program faster than Python can interpret it

[Andrew Kelley shared](https://twitter.com/andy_kelley/status/1483677253682675713) how the upcoming stage2 Zig compiler can compile an executable from scratch and run it faster than Python can interpret the file on the right:

<a align="center" href="https://user-images.githubusercontent.com/3173176/153105034-68134cdc-f206-42ad-91c4-1e7cfcdf887a.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/153105034-68134cdc-f206-42ad-91c4-1e7cfcdf887a.png"></img></a>

We're also starting to get the first hints of how Zig's [hot code swapping](https://github.com/ziglang/zig/issues/68) feature will work, with the first successful hot code swap [shown on one of Andrew's recent Twitch streams](https://www.reddit.com/r/Zig/comments/s9toy1/we_have_a_working_hot_code_swapping/)!

# Implementing the "Self" programming language in Zig

[@sin-ack](https://github.com/sin-ack) shared [on Discord](https://discord.com/channels/605571803288698900/605572611539206171/939317499139330111) how they're working on an implementation of the Self programming language:

> For about the past 2 months or so, I have been working on an implementation of the Self programming language (https://selflanguage.org/) in Zig. It's been coming along pretty well so far; the language parser, AST, interpreter and VM runtime is now done. For the past couple of weeks I have been working on getting garbage collection (generational scavenging GC) right and for the past couple of days I've been doing performance work. Feel free to ask me anything :^)
>
> The project is available at: https://github.com/sin-ack/zigself
> 
> I've been recording some of the things I've worked on and uploading them here: https://www.youtube.com/channel/UC7XQtFrGLTuJpIMTg3oiZ5Q/videos (just published a second video, actually :^)

# Visualizing how rasterization works on modern GPUs

[@MichalZiulek](https://twitter.com/MichalZiulek) is back again with more incredible DirectX graphics demos, [this time showing](https://www.reddit.com/r/gamedev/comments/sest9c/see_how_gpu_rasterizer_works_in_slow_motion_gtx/) how GPU reasterization of triangles works in slow motion ("This works by capturing render output to a transient buffer and then playing it back at human-discernable speed."):

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/153105961-29ee6e52-656f-41cf-bf33-1cc871c6bbce.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/153105961-29ee6e52-656f-41cf-bf33-1cc871c6bbce.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/153106005-21568eb5-6610-442f-a908-17fb1ae10068.png"></img>
    </a>
</video>

[Check it out on GitHub](https://github.com/michal-z/zig-gamedev/tree/main/samples/rasterization) and [consider sponsoring Michal's work](https://github.com/sponsors/michal-z)!

# zmath & introduction to zig-gamedev DirectX applications

The other two notable mentions from Michal are:

* [zmath 0.2](https://github.com/michal-z/zig-gamedev/blob/main/libs/common/zmath.zig): fast, multi-platform, SIMD math library ("This release brings matrix operations, quaternion operations and much improved API. I wrote short [article about it here](https://zig.news/michalz/fast-multi-platform-simd-math-library-in-zig-2adn)")
* [6 zig-gamedev samples / intro applications](https://github.com/michal-z/zig-gamedev/tree/main/samples/intro), "Learn low-level graphics programming, game programming and zig-gamedev framework. Intro applications have been designed for learning purposes, I try to keep code as simple as possible and comment new functionality added in each subsequent program." - some very cool screenshots in here!

# Minecraft-inspired arcade game

Ino#7587 is working on a Minecraft-inspired arcade game, built using [their Zig SFML wrapper](https://github.com/Guigui220D/zig-sfml-wrapper):

<a href="https://user-images.githubusercontent.com/3173176/153094991-4ddc48be-4684-48f9-b2a2-225c9f5f6e87.png"><img width="240px" src="https://user-images.githubusercontent.com/3173176/153094991-4ddc48be-4684-48f9-b2a2-225c9f5f6e87.png"></img></a> <a href="https://user-images.githubusercontent.com/3173176/153094998-8fba9b0f-f573-4f71-86fb-9b671f9b13c4.png"><img width="240px" src="https://user-images.githubusercontent.com/3173176/153094998-8fba9b0f-f573-4f71-86fb-9b671f9b13c4.png"></img></a>

# Zig Minecraft server implementation

[@regenerativep](https://github.com/regenerativep) is building a Minecraft server:

> to feel my way around zig and networking and the minecraft protocol. not a lot of functionality, but the server can be joined and you can see other players move around https://github.com/regenerativep/zig-mc-server

# Learning material

* [Zig JSON in 5 minutes](https://www.reddit.com/r/Zig/comments/s2g07j/zig_json_in_5_minutes/)
* [Zig hashmaps explained](https://devlog.hexops.com/2022/zig-hashmaps-explained)
* [Zig adventures on iOS (multi-part series)](https://zig.news/kristoff/zig-adventures-on-ios-getting-started-3n8f)
* [Let's build an Entity Component System from scratch (part 1)](https://www.reddit.com/r/Zig/comments/s5tafo/lets_build_an_entity_component_system_from/)
* [Zig by example](https://zig-by-example.com/) (new resource)
* ["Want to create a TUI application? - The Basics of "Uncooked" Terminal IO"](https://zig.news/lhp/want-to-create-a-tui-application-the-basics-of-uncooked-terminal-io-17gm)
* ["Analysis of the overhead of a minimal Zig program"](https://zig.news/aransentin/analysis-of-the-overhead-of-a-minimal-zig-program-4lg0)

# Major new library developments

* Tiny and fast node-api bindings: [evanwashere/napi.zig](https://github.com/evanwashere/napi.zig)
* libxml2 Built with Zig: [mitchellh/zig-libxml2](https://github.com/mitchellh/zig-libxml2)
* Objective-C Runtime bindings: [hazeycode/zig-objcrt](https://github.com/hazeycode/zig-objcrt)
* [Finite state machine](https://en.wikipedia.org/wiki/Finite-state_machine) library: [cryptocode/zigfsm](https://github.com/cryptocode/zigfsm)
* Text diffing (Myers' diff algorithm): [tomhoule/zig-diff](https://github.com/tomhoule/zig-diff)
* BTreeMap implementation: [pmkap/zig-btreemap](https://github.com/pmkap/zig-btreemap)
* Dynamic circular buffer allocator: [hmusgrave/zcirc](https://github.com/hmusgrave/zcirc)
* Compile-time validation of type constraints: [ibokuri/concepts](https://github.com/ibokuri/concepts) ("concepts is a library that provides compile-time validation of type constraints. It sort of aggregates the different ways you can validate a type in Zig into a more organized and consistent interface.")
* Bindings for the GEOS C library (libgeos): [guidorice/libgeos.zig](https://github.com/guidorice/libgeos.zig)
* Serialization and deserialization framework: [getty-zig/getty](https://github.com/getty-zig/getty)

# Thanks for reading!

If you like my work on zigmonthly, [Mach engine](https://devlog.hexops.com/categories/mach), etc. consider [sponsoring me on GitHub](https://github.com/sponsors/slimsag) so I can do even more of it!
