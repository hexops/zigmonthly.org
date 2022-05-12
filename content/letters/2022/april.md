---
title: "Zig monthly, April 2022: OS interop, Graphics, WebAssembly, Talks, Wren language & more"
date: 2022-05-12T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/168130228-0b0e9736-97fa-44d2-a020-896bb4aa6105.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/168130228-0b0e9736-97fa-44d2-a020-896bb4aa6105.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/168130228-0b0e9736-97fa-44d2-a020-896bb4aa6105.png"></img></a>

# nanovg-zig

[@fabioarnold](https://github.com/fabioarnold) has released nanovg-zig:

> A hardware-accelerated vector graphics library. I use this library to build the user interface of my (free) [pixel art editor MiniPixel](https://fabioarnold.itch.io/mini-pixel). I've since rewritten it in Zig and ported it to Wasm/WebGL.
> 
> You can use it to draw (blurred) text, arbitrary bezier curved shapes (with holes) and of course gradients. You can try the [WebAssembly example here](https://fabioarnold.github.io/nanovg-zig/) and find [the source on GitHub here](https://github.com/fabioarnold/nanovg-zig)

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/167889348-9b8aa3aa-39f3-487f-914e-833995944146.mov" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/167889348-9b8aa3aa-39f3-487f-914e-833995944146.mov">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/168127948-d3f7ae2a-8425-4c1e-85ee-8415282331f4.png"></img>
    </a>
</video>

# wala: A language to simplify WebAssembly Text syntax

[wala](https://github.com/CalmSystem/wala) is a language trying to simplify WebAssembly Text syntax "while keeping the full expressiveness and retro-compatibility. Unwittingly becoming a Zig toolchain for WASM. - It aims to be for WASM what YAML is for JSON."

```wala
func $fib export()
  u64 $n -> ?
  if {$n <= 2}
    1
    +
      $fib{$n - 2}
      $fib{$n - 1}
```

[@CalmSystem](https://github.com/CalmSystem) cautions:

> This is my first zig project [...] FizzBuzz and others are already working, but some work is still needed before the first proper release.

# Tile-based, multithreaded 3D software renderer

[@danielabbott](https://github.com/danielabbott) created [a simple software renderer in Zig](https://github.com/danielabbott/Software-Renderer), a cool codebase to learn from if you're into that sort of thing:

<a align="center" href="https://user-images.githubusercontent.com/3173176/167912515-e7c0c8ea-68df-4929-860f-e34c1063e0de.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/167912515-e7c0c8ea-68df-4929-860f-e34c1063e0de.png"></img></a>

# Simple bin-packed texture atlas

[@mitchellh](https://github.com/mitchellh) dropped [a gist](https://gist.github.com/mitchellh/0c023dbd381c42e145b5da8d58b1487f) which provides a simple packed texture atlas in pure Zig, with no dependencies other than the stdlib.

# zlog: Zero-Allocation Logging

Inspired by Go's zerolog, [@candrewlee14](https://github.com/candrewlee14) has released [zlog](https://github.com/candrewlee14/zlog), a zero-allocation logging library.

<a align="center" href="https://user-images.githubusercontent.com/3173176/167915298-e1615354-f500-46c1-8e8f-fe5f2ec0c63b.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/167915298-e1615354-f500-46c1-8e8f-fe5f2ec0c63b.png"></img></a>

# Bindings for Wren ("a small, fast, class-based concurrent scripting language")

[@dantecatalfamo](https://github.com/dantecatalfamo) released [wren-zig](https://github.com/dantecatalfamo/wren-zig) which provides Zig bindings to [Wren](https://wren.io), a fast lua-sized scripting language with classes and concurrency.

```wren
System.print("Hello, world!")

class Wren {
  flyTo(city) {
    System.print("Flying to %(city)")
  }
}

var adjectives = Fiber.new {
  ["small", "clean", "fast"].each {|word| Fiber.yield(word) }
}

while (!adjectives.isDone) System.print(adjectives.call())
```

(If you like that, you may also be interested in [Buzz](https://github.com/giann/buzz), "a small/lightweight typed scripting language written in Zig", from last month's article.)

# snowflake simulator

![@Rekihyt](https://github.com/Rekihyt) has built a [simple snowflake simulator](https://github.com/Rekihyt/snow) using OpenGL:

<a align="center" href="https://user-images.githubusercontent.com/3173176/167920253-999344b2-3fdc-46d0-8525-cdb2f2be53e8.gif"><img width="650px" src="https://user-images.githubusercontent.com/3173176/167920253-999344b2-3fdc-46d0-8525-cdb2f2be53e8.gif"></img></a>

# zig-arg: CLI flags, subcommands & nested subcommands

[zig-arg](https://github.com/PrajwalCH/zig-arg) is a [clap-rs](https://github.com/clap-rs/clap) inspired Command Line Argument parser for Zig which support flags, subcommand and nested subcommands out of the box.

It looks quite slick, check out the [Reddit discussion](https://www.reddit.com/r/Zig/comments/u4bjrq/github_prajwalchzigarg_arg_parser_library_for_zig/) for some alternatives as well.

# Zig MiLAN Party 2023 talks

The first-ever European Zig meetup was held in Milan, Italy - the Zig MiLAN Party! Here were some of the talks presented/recorded:

- [⚡ Zig Roadmap 2023 - Andrew Kelley](https://www.reddit.com/r/Zig/comments/u4z46t/zig_milan_party_2023_zig_roadmap_2023_andrew/)
- [iOS DX With Zig - Jakub Konka](https://www.youtube.com/watch?v=bJNSPZTLMUU)
- [Mach game engine, what's next (2022) - Stephen Gutekanst](https://www.youtube.com/watch?v=m3gOX26LOeM)

# Windows explorer integration in Zig

Ever wondered how applications on Windows integrate with the right-click menu, and overlay their own pixels on files in the explorer? [@squeek502](https://github.com/squeek502)'s new [watchedoverlay](https://github.com/squeek502/watchedoverlay) project does just that, giving you the ability to right-click -> "Toggle watched" which renders a "Watched" green checkmark over files:

<a align="center" href="https://user-images.githubusercontent.com/3173176/167921403-a1347523-d419-48fd-9fff-d490c527fef1.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/167921403-a1347523-d419-48fd-9fff-d490c527fef1.png"></img></a>

# Jakub Konka's work on iOS developer experience

I'm ecstatic this work is ongoing, so I had to include this! This work isn't complete or very usable currently, as Jakub cautions below, but here are three repositories you may want to keep an eye on if you're interested in the future Zig developer experience for iOS app development:

* https://github.com/kubkon/ZigKit 'will hopefully become a goto lib for low-level Apple frameworks bindings in Zig'
* https://github.com/kubkon/zignature 'the goto solution for codesigning your Apple apps with Zig (hopefully without even requiring access to frameworks, but time will tell if that is even possible)'
* https://github.com/kubkon/zig-deploy 'the final piece of the puzzle [...] it uses ZigKit internally for low-level Apple bindings, including the undocumented and private framework MobileDevice which is used by Xcode (and oss tool ios-deploy) to speak to an Apple device such as an iPhone.'

> Early days, and I strongly advise against using zig-deploy - wouldn't want anyone to brick their phone! Having said that, any questions about any of this, you know where to find me!

# fast polygon tesselator

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/167927619-b6e67976-7cf5-4ea7-87ca-65ddefcd9418.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/167927619-b6e67976-7cf5-4ea7-87ca-65ddefcd9418.mp4">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/168122810-90dbeff6-6e41-41c1-b6da-df62d994f699.png"></img>
    </a>
</video>

> I wrote a fast polygon tessellator (triangulates in one pass) in pure zig which can be used for vector graphics.
> 
> It's able to handle complex cases and can draw the tiger head svg. This video shows what it's doing to fill a whisker of the tiger. The [demo app is here](https://github.com/fubark/cosmic/blob/master/tools/visual-tess.js) and the [zig implementation is here](https://github.com/fubark/cosmic/blob/master/graphics/src/tessellator.zig)

Be sure to check out the [discussion on Reddit](https://www.reddit.com/r/Zig/comments/u8bhto/polygon_tessellator_in_zig/), too, which goes into further detail about how it works:

> The vertices are chosen from a vertex queue similar to the y-monotone triangulation so most of the algorithm is making sure that each sub-polygon span is a y-monotone. And determining which regions to fill triangles depends on the winding rule. Currently, this tessellator does the evenodd fill rule but it shouldn't be too hard to add the nonzero fill rule. :)

# The Zig compiler can finally build itself

In case you missed it, the Zig self-hosted compiler has had a great deal of progress and [can finally build itself](https://news.ycombinator.com/item?id=31052029).

This is a huge milestone for Zig, and while [there's still much work to do](https://github.com/ziglang/zig/issues/89) before the new compiler can be shipped to everyone - it's looking like we'll be able to have Zig-implemented-in-Zig (rather than C++) very soon which should lead to an explosion of improvements and new contributors.

Exciting times!

# Mach engine updates

With Mach we've seen quite a burst of contributors! Thanks to @johanfforsberg, @d3m1gd, @zargio, @andoryuuta and more we've now got [a great WebGPU example showcase](https://machengine.org/gpu/) showing off low-level graphics and a great starting point for anyone interested in learning WebGPU with Zig:

<video align="center" width="650px" src="https://user-images.githubusercontent.com/3173176/167927458-819a6c65-42c5-497a-8b97-8f0ec7021560.mov" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/167927458-819a6c65-42c5-497a-8b97-8f0ec7021560.mov">
        <img width="650px" src="https://user-images.githubusercontent.com/3173176/168124468-ee9ade92-75eb-48ed-ab54-4b9890e4f9eb.png"></img>
    </a>
</video>

There's also major work underway by [@iddev5](https://github.com/iddev5) to add Browser WebAssembly support-making Mach even more cross-platform, as well as [@PiergiorgioZagaria](https://github.com/PiergiorgioZagaria)'s work to create a ShaderToy-esque application called [`shaderexp`](https://github.com/hexops/mach/tree/main/shaderexp) which live-reloads WGSL shaders as you save in your editor.

# glTF 2.0 in pure Zig

[@kooparse](https://github.com/kooparse) has been working on [a pure Zig parser for glTF 2.0](https://github.com/kooparse/gltf):

> Loading 3D models fully in Zig, without any parser/loader in other languages would be great, so I made a glTF 2.0 parser. I'm using it on my engine, and it works well enough for others' project usage (I guess). There are also some helpers to get local and global positions of each node and something to load data from binary. 'Hope it could help some! 🙂

# zig-gamedev updates

<a align="center" href="https://user-images.githubusercontent.com/3173176/168126644-1e60f480-3597-4278-82d4-964fd3d6bd78.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/168126644-1e60f480-3597-4278-82d4-964fd3d6bd78.png"></img></a>

[@michal-z](https://github.com/michal-z) is at it again, this time leveraging [mach/gpu](https://machengine.org/gpu) to bring his work to Windows/Linux/macOS:

* [triangle_wgpu](https://github.com/michal-z/zig-gamedev/tree/main/samples/triangle_wgpu) is a simple but fairly complete app showing the ins-and-outs of WebGPU, creating bind group layouts, render peipelines, managing vertex/index/uniform buffers, depth buffers, etc.
* [procedural_mesh_wgpu](https://github.com/michal-z/zig-gamedev/tree/main/samples/procedural_mesh_wgpu) leverages his zmesh library to efficiently draw several procedurally generated meshes, use simple physically-based shading, camera movement, and more.
* Speaking of [`zmesh`](https://github.com/michal-z/zig-gamedev/tree/main/libs/zmesh), v0.2 is out. It's a small library/bindings for loading, generating, processing and optimizing triangle meshes - using par_shapes, meshoptimizer, and cgltf behind the scenes.

# brucelib updates

You might also want to keep an eye on [@hazeycode](https://github.com/hazeycode)'s [brucelib](https://github.com/hazeycode/brucelib) - although early stages, work continues and it's recently gained [an audio module](https://github.com/hazeycode/brucelib/blob/main/modules/audio/README.md) which provides a basic mixer and wav file loader!

# Thanks for reading!

If you like my work on zigmonthly, [Mach engine](https://devlog.hexops.com/categories/mach), etc. consider [sponsoring me on GitHub](https://github.com/sponsors/slimsag) so I can do even more of it!
