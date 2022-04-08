---
title: "Zig monthly, March 2022: io_uring, physics, chess, gamedev & scripting languages"
date: 2022-04-01T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/162355131-07d263f8-bb28-4946-adca-ad1444532eca.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/162355131-07d263f8-bb28-4946-adca-ad1444532eca.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/162355131-07d263f8-bb28-4946-adca-ad1444532eca.png"></img></a>

# AsyncIOUring

[@saltzm](https://github.com/saltzm) released [AsyncIOUring](https://github.com/saltzm/async_io_uring) - an event loop that wraps the `IO_Uring` library with coroutines support.

For context: `io_uring` is a new-ish Linux kernel feature which allows for **much more efficient network/file IO**. Zig has an `IO_Uring` library that is a convenient interface to the Linux API.

Where `AsyncIOUring` comes in (and why this is so cool): it's an _even more convenient interface_ to this API, adding an async event loop that handles submission and completion via the kernel APIs. It leverages Zig's async functionality to suspend execution, letting you write serial/blocking code naturally while behind the scenes it actually leverages IO concurrency (even within a single thread!)

# phyz 2D physics

[@silversquirl](https://github.com/silversquirl) is working on [phyz](https://github.com/silversquirl/phyz), a work-in-progress physics engine for 2D games

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/162350926-164fef0f-e70b-466d-a15a-ab8e855aaa1e.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/162350926-164fef0f-e70b-466d-a15a-ab8e855aaa1e.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/162351061-114cadaf-9cab-44bf-9d43-19aa9bfd9112.png"></img>
    </a>
</video>

# regz: ATDF file parsing for microcontrollers

[@mattnite](https://github.com/mattnite) as part of the Zig embedded group has added ATDF file parsing (used for AVR microcontrollers) to [regz](https://github.com/ZigEmbeddedGroup/regz) (a Zig code generator for microcontrollers)

# ZBA (Gameboy advance emulator) updates

Rekai is continuing to work on [ZBA, a gameboy advance emulator](https://git.musuka.dev/paoda/zba), recently implementing normal sprites and squashing enough bugs that some titles like Kirby: Nightmare in Dream Land are playable!

<a align="center" href="https://user-images.githubusercontent.com/3173176/162351220-710f2b29-1b76-4a64-a5e1-92d3f75584c5.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/162351220-710f2b29-1b76-4a64-a5e1-92d3f75584c5.png"></img></a>

# Avalanche - UCI Chess Engine using Neural Networks

[@SnowballSH](https://github.com/SnowballSH) has released [Avalanche](https://github.com/SnowballSH/Avalanche):

> (Probably the first) UCI Chess Engine written in Zig :D It uses Neural Networks too.
> 
> It is written 99% in Zig, utilizing a lot of Zig's awesome features such as packed structs.
> 
> It plays at around 2300 ELO (a.k.a. **can beat most human professional players**) now :) You can view its games against other engines here https://lichess.org/@/IceBurnEngine/all

# zig-gamedev

<a align="center" href="https://user-images.githubusercontent.com/3173176/162349985-d6056fe4-76bb-46cf-97e1-c38b761515ce.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/162349985-d6056fe4-76bb-46cf-97e1-c38b761515ce.png"></img></a>

[@MichalZiulek](https://twitter.com/MichalZiulek) is back with many more updates to zig-gamedev!

* [`zbullet`](https://github.com/michal-z/zig-gamedev/tree/main/libs/zbullet) v0.1, bindings for the Bullet Physics SDK complete with 6 [intro applications](https://github.com/michal-z/zig-gamedev/tree/main/samples/intro#intro-6)!
* [`znoise`](https://github.com/michal-z/zig-gamedev/tree/main/libs/znoise) - bindings for FastNoiseLite
* [`zmesh`](https://github.com/michal-z/zig-gamedev/tree/main/libs/zmesh) - bindings for `par_shapes.h` complete with a [demo](https://github.com/michal-z/zig-gamedev/tree/main/samples/procedural_mesh)
* [`zmath`](https://github.com/michal-z/zig-gamedev/tree/main/libs/zmath) v0.3 - SIMD math library for game developers, now with Fast Fourier Transforms, color management functions, and better docs

# Mini Pixel v0.2

[@captainhorst](https://twitter.com/captainhorst) has [released Mini Pixel v0.2](https://twitter.com/captainhorst/status/1503468961094066176), a pixel image editor which you can get [for free on Itch.io](https://fabioarnold.itch.io/mini-pixel) 

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/162352146-5a0b5f8e-5d93-4441-9d2c-8d86d3c86321.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/162352146-5a0b5f8e-5d93-4441-9d2c-8d86d3c86321.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/162352265-a078adb5-466d-4d5e-a2b7-549046ebe603.png"></img>
    </a>
</video>

# Marble - an experimental metamorphic testing library

<a align="center" href="https://user-images.githubusercontent.com/3173176/162352504-947c419e-5ee9-4a99-85a1-769cc961de51.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/162352504-947c419e-5ee9-4a99-85a1-769cc961de51.png"></img></a>

[@cryptocode](https://github.com/cryptocode) released Marble, a metamorphic testing library:

> Metamorphic testing is a powerful technique that provides additional test coverage by applying a number of transformations to test input, and then checking if certain relations still hold between the outputs. Marble will automatically run through all possible combinations of these transformations.

# Mach engine v0.1 - cross platform Zig graphics in 60 seconds

<a align="center" href="https://user-images.githubusercontent.com/3173176/160258304-3335a609-6177-4c1a-9008-d9525bd72c85.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/160258304-3335a609-6177-4c1a-9008-d9525bd72c85.png"></img></a>

I released [Mach engine v0.1](https://devlog.hexops.com/2022/mach-v0.1-zig-graphics-in-60s) after some ~9 months of work and 1,100+ commits, giving you cross-platform graphics in 60s:

```
git clone https://github.com/hexops/mach
cd mach/
zig build run-example
```

# Buzz - small/lightweight typed scripting language

<a align="center" href="https://user-images.githubusercontent.com/3173176/162352945-d93c1675-f937-4a08-a2f4-a6c22b56470c.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/162352945-d93c1675-f937-4a08-a2f4-a6c22b56470c.png"></img></a>

[@giann](https://github.com/giann) is creating [Buzz](https://github.com/giann/buzz), a small/lightweight typed scripting language written in Zig:

> * Small in size and complexity (just a bit more than Lua though)
> * Strict typing
> * Unambiguous
> * No nonsense coercion

# Thanks for reading!

If you like my work on zigmonthly, [Mach engine](https://devlog.hexops.com/categories/mach), etc. consider [sponsoring me on GitHub](https://github.com/sponsors/slimsag) so I can do even more of it!
