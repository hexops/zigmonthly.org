---
title: "Zig monthly, December 2021: GUI, NodeJS modules, optional GC & more"
date: 2021-12-31T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/148187357-381b3b33-bc2b-4243-a704-6c21a65f5b26.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/148187357-381b3b33-bc2b-4243-a704-6c21a65f5b26.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/148187357-381b3b33-bc2b-4243-a704-6c21a65f5b26.png"></img></a>

# Vulkan GPU path tracing

[@ashpil](https://github.com/ashpil) has been working on a GPU accelerated path tracer using vulkan-zig, GLFW, and the Vulkan ray tracing extensions:

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/148028145-f231a70d-45de-467d-8b4e-70a5cc0eae85.mov" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/148028145-f231a70d-45de-467d-8b4e-70a5cc0eae85.mov">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/148177248-0d46e710-f8cc-49c6-928a-7193a413d215.png"></img>
    </a>
</video>

> It's about 6K lines of code, I thought a realistic chess game would be a good way to learn some advanced graphics techniques, as the gameplay is so well established I could just focus on the visuals.
> 
> Plans for the near future include performance optimizations (it probably lags less on an RTX series card but I'm on a 1080) and more interesting materials that take full advantage of path tracing.

They're planning to publish the code on GitHub after polishing some more, you can keep an eye on their [GitHub profile](https://github.com/ashpil) or reach out to them on Discord (Brunch#9226) in the meantime!

# Async generator library

[Yurii Rashkovskii](https://twitter.com/yrashk) published [zig-generator](https://github.com/yrashk/zig-generator)-a library for writing async generator functions, which I found best described by [this commit message](https://github.com/yrashk/zig-generator/commit/bda35aa8c9691319b8ddb37b3294befe61a5014e) (but be sure to check out the code examples in the README):

> Problem: what's the point of generators?
>
> Generators look nice, but they are still slower than callbacks (as they naturally have more harness code).
>
> Solution: provide Map and Join generators
>
> The beauty of generators is that they are async and this allows us to build higher-level primitives.
>
> Of a particular interest is Join that will allow to consume values from two generators, as they come.

# zgt: a Zig GUI toolkit

[@zenith391](https://github.com/zenith391) released v0.1 of [zgt (Zig GUI Toolkit)](https://www.reddit.com/r/Zig/comments/ru7cp0/zgt_zig_gui_toolkit_01_has_been_released):

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/148033333-8a7ab325-ebd5-48bc-87e4-f057820e0e82.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/148033333-8a7ab325-ebd5-48bc-87e4-f057820e0e82.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/148310446-60cac05f-839f-4b7b-ab11-0827a50f2bdd.png"></img>
    </a>
</video>

> zgt is a pure Zig (in fact, the only backend that needs libc is the GTK+ one) library for making cross-platform GUIs. It has first class support for animations and data binding. One notable thing is that its main aim is to use native widgets when available, but it (will) be able to draw widgets manually which will be used for the OpenGL ES backend. [...] Only thing missing is a Cocoa / Mac OS backend.

# Low level terminal manipulation

[@xyaman](https://github.com/xyaman) [released mibu](https://github.com/xyaman/mibu), a library for low-level terminal manipulation, "[...] It’s far from complete, but the basics work":

> Features:
> - Allocation free.
> - Raw mode.
> - 8-16 colors.
> - True Color (24-bit RGB).
> - Cursor controls.
> - Clear(Erase) functions.
> - Colors.
> - Key events.

# TinyVG

[Felix "xq" Queißner](https://github.com/sponsors/MasterQ32) released [TinyVG](https://zig.news/xq/a-challenger-to-the-throne-of-vector-graphics-svg-is-dead-long-live-tinyvg-4on8): "A challenger to the throne of vector graphics. SVG is dead, long live TinyVG!" - definitely worth checking out!

<a align="center" href="https://user-images.githubusercontent.com/3173176/148180065-4b621b42-92c5-43ef-a573-661908fdf708.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/148180065-4b621b42-92c5-43ef-a573-661908fdf708.png"></img></a>

# Use Zig to build native NodeJS modules

[Zig 0.9 was released](https://ziglang.org/download/0.9.0/release-notes.html) - which has enabled zig ld to be used to create native NodeJS modules without node-gyp. You can find some exampls [from the Tigerbeetle team here](https://twitter.com/jorandirkgreef/status/1473259997563961345)!

# Self hosted compiler progress

Development of the self-hosted Zig compiler continues, with [the most recent numbers](https://twitter.com/andy_kelley/status/1477385526625792000) (Jan 1st, 2022) showing over 50% of behavior tests passing with the LLVM backend(!):

> Zig self-hosted compiler progress report:
> * 159,096 lines of code
> * Behavior Tests Passing:
>   - LLVM backend: 575/1078 (53%)
>   - C backend: 298/1078 (28%)
>   - WASM: 157/1078 (15%)
>   - ARM: 7/1078 (1%)
>   - x86: 0/1078 (0%)

The 0.9 release notes included this awesome diagram:

<a align="center" href="https://user-images.githubusercontent.com/3173176/148181147-46e59b0b-b10a-453c-b357-4b7538a74ffd.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/148181147-46e59b0b-b10a-453c-b357-4b7538a74ffd.png"></img></a>

# Gamedev progress

Progress continues in the area of gamedev, too, attempting to summarize:

* [@omaraaa](https://github.com/omaraaa) published [a vector math library](https://github.com/omaraaa/VecFns) which extends your own `Vec2f`, etc. struct declarations with methods - an interesting approach.
* [@MichalZiulek](https://twitter.com/MichalZiulek) has been hard at work on a SIMD-accelerated vector math package for zig-gamedev: [zmath](https://github.com/michal-z/zig-gamedev/blob/main/libs/common/zmath.zig)
* [@MichalZiulek](https://twitter.com/MichalZiulek) published a [zig-gamedev December 2020 progress report](https://github.com/michal-z/zig-gamedev/wiki/Progress-Reports#december-2021), including audio, mesh shaders, and more!
* I published [a website and roadmap for the upcoming Mach game engine](https://hexops.com/mach/).

# Optional garbage collection

[Mitchell Hashimoto](https://twitter.com/mitchellh) (founder of Hashicorp) [wrote a wrapper for libgc in Zig](https://twitter.com/mitchellh/status/1472652373319241731) in order to learn how Zig interoperates with C ("turns out: exceptionally good")

The library implements the standard Zig `Allocator` interface, and should allow one to mix and match garbage collection and manual memory management, very cool!

# Other notable mentions

* Libraries
    * [zig-qoi](https://github.com/MasterQ32/zig-qoi): a Zig implementation of the QOI image format
    * [zig-v8](https://github.com/fubark/zig-v8): Zig and C bindings for V8 useful for embedding V8 into projects.
    * [zlib](https://github.com/mattnite/zig-zlib), [libcurl](https://github.com/mattnite/zig-libcurl), and more C library bindings from [@mattnite](https://github.com/mattnite)
* News
  * Coil (the company behind Tigerbeetle DB) [recently began sponsoring Zig](https://twitter.com/uchiuchibeke/status/1473717044331880450) and the Tigerbeetle team shared some [interesting insights into how they use leverage comptime for their database](https://twitter.com/jorandirkgreef/status/1474697395028045824).
  * [@sheredom](https://twitter.com/sheredom/status/1475441606207676419) and [@postgoodism](https://twitter.com/postgoodism/status/1476999481228881921) both shared Advent of Code postmortems after having completed it in Zig!
  * [Jens Goldberg](https://twitter.com/aransentin) shared an ["Analysis of the overhead of a minimal Zig program"](https://zig.news/aransentin/analysis-of-the-overhead-of-a-minimal-zig-program-4lg0)

# Thanks for reading!

If you like my work on zigmonthly, Mach engine, etc. consider [sponsoring me on GitHub](https://github.com/sponsors/slimsag) so I can do even more of it!
