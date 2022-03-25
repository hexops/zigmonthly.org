---
title: "Zig monthly, February 2022: Language interoperability keeps getting better"
date: 2022-03-12T23:51:50-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/158046724-d423ec00-db66-4346-be54-257a59082b52.png"]
---

<a align="center" href="https://user-images.githubusercontent.com/3173176/158046724-d423ec00-db66-4346-be54-257a59082b52.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/158046724-d423ec00-db66-4346-be54-257a59082b52.png"></img></a>

# Haskell ↔ Zig

[Calling Zig from Haskell](https://luctielen.com/posts/calling_zig_from_haskell/) by [@luctielen](https://twitter.com/luctielen) covers how to leverage Zig from Haskell.

# NodeJS ↔ Zig

[`@ziglang/cli`](https://github.com/pluvial/node-zig/tree/main/packages/cli) is a new NPM package by [@pluvial](https://github.com/pluvial) which makes it easy to integrate Zig into a NodeJS project.

They're also using it in conjunction with their other project, [vite-plugin-zig](https://github.com/pluvial/vite-plugin-zig) to do things like [WebAssembly math addition](https://pluvial.xyz/wasm). Pretty cool!

# Rust ↔ Zig

[cargo-zigbuild](https://github.com/messense/cargo-zigbuild) has just been released by [@messense](https://github.com/messense), allowing one to compile a Rust Cargo project with Zig as linker for [easier cross compilation](https://actually.fyi/posts/zig-makes-rust-cross-compilation-just-work/)!

# mruby ↔ Zig

[mruby-zig](https://github.com/dantecatalfamo/mruby-zig) by [@dantecatalfamo](https://github.com/dantecatalfamo) lets you leverage the embeddable Ruby implementation fully from Zig applications!

# Huffman coding visualization

[190n](https://github.com/190n) created a [visualization of the Huffman coding algorithm](https://190n.github.io/huffman-visualization/)

<a align="center" href="https://user-images.githubusercontent.com/3173176/158044546-01dc8086-076d-4daa-9207-f06e3780de34.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/158044546-01dc8086-076d-4daa-9207-f06e3780de34.png"></img></a>

# Using Zig comptime for conceptual dryness (Forth)

[@lucabol](https://www.lucabol.com) shared an interesting article on [Using Zig comptime for conceptual dryness](https://www.lucabol.com/posts/2022-03-09-using-zig-comptime-for-conceptual-dryness/) - describing an implementation of the Forth language in Zig.

# Telegram ↔ Zig

[@axgdev](https://github.com/axgdev) wrote a [telegram echo bot](https://github.com/axgdev/telegram_echobot_zig) in Zig, pretty cool and shows usage of the `requestz` HTTP library. They also [streamed development of it on Twitch](https://www.twitch.tv/videos/1298657556) and more recently even released a [Telegram library for Zig](https://github.com/axgdev/telezig).

# Gameboy Advance Emulator

Rekai has been working on [ZBA, a gameboy advance emulator](https://git.musuka.dev/paoda/zba):

> I've been working on a Gameboy Advance Emulator! With an initial (quite broken) implementation of Mode 0 Graphics I finally have something visual to show off. It's still very early so the CPU is the only thing that really passes the gauntlet of test ROMs out there.

<a align="center" href="https://user-images.githubusercontent.com/3173176/158044744-f8c33a08-4cf1-4b45-bccc-7a793f209a8b.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/158044744-f8c33a08-4cf1-4b45-bccc-7a793f209a8b.png"></img></a>

# Simple Linking Format

[@MasterQ32](https://github.com/MasterQ32) released a small project for learn the basics of linking, [SLF](https://github.com/MasterQ32/SLF), "a very simple object file format that can be used to link programs that don't require distinct sections for code and data."

# In-depth articles about the stage2 Zig compiler internals

Mitchell Hashimoto has been publishing [a series of in-depth articles](https://mitchellh.com/zig) about the internals of the stage2 Zig compiler, including:

* [Zig Tokenizer](https://mitchellh.com/zig/tokenizer)
* [Zig Parser](https://mitchellh.com/zig/parser)
* [Zig AstGen: AST => ZIR](https://mitchellh.com/zig/astgen)
* [Zig Sema: ZIR => AIR](https://mitchellh.com/zig/sema)
* [Zig Build System Internals](https://mitchellh.com/zig/build-internals)

Also relevant, I highly suggest checking out [Govind's](https://zig.news/gowind) 2-part series ["So where is my stuff stored ?"](https://zig.news/gowind/so-where-is-my-stuff-stored-part-1-38b7) which dives into some of the lower-level details when investigating how Zig creates structs on the stack.

# Brucelib 

Although early stages and very much a work-in-progress, [@hazeycode](https://github.com/hazeycode) announced they are working on [Brucelib](https://github.com/hazeycode/brucelib):

> A monorepo of modules for programming cross-platform games, simulations, engines and editors. Leveraging the Zig programming language and toolchain, brucelib intends to be highly hackable and suitable for rapid prototyping, jams or fully-fledged products. Each module is designed to be easy to configure, extend or modify to your own specific needs, and to replace with something else in future if your project demands it.

<a align="center" href="https://user-images.githubusercontent.com/3173176/158044639-d7815e33-fbd5-463f-a470-e4965381ee14.gif"><img width="650px" src="https://user-images.githubusercontent.com/3173176/158044639-d7815e33-fbd5-463f-a470-e4965381ee14.gif"></img></a>

# Cosmic

[@fubark](https://github.com/fubark) is working on [Cosmic](https://www.cosmic-js.com/):

> Cosmic is a general purpose runtime for Javascript and WASM. It aims to have broad applications by exposing native cross platform APIs: window management, 2D/3D graphics, UI widgets, filesystem, networking, and more. It also aims to streamline software tooling to provide the essentials to help you develop and maintain software.

<a align="center" href="https://user-images.githubusercontent.com/3173176/158045196-4836fb58-1039-4e66-b64e-19242bfa46f1.png"><img width="650px" src="https://user-images.githubusercontent.com/3173176/158045196-4836fb58-1039-4e66-b64e-19242bfa46f1.png"></img></a>

# regz: Zig code generator for microcontrollers

[@mattnite](https://github.com/mattnite) and the Zig embedded group published [regz](https://github.com/ZigEmbeddedGroup/regz), a Zig code generator for microcontrollers produced from SVD files.

# Zig kills it in the WASM4 game jam

Zig games were quite prominant in the WASM4 game jam, there's a great [overview video on the new Zig forum](https://forum.ziggit.dev/t/awesome-tiny-games-in-11-programming-languages-wasm-4-jam-2022-results/63)

[@freiguy1](https://gitlab.com/freiguy1) for example did a Zig implementation of the original Snake game which you can play here: https://freiguy1.itch.io/znake

<a align="center" href="https://user-images.githubusercontent.com/3173176/158045251-e959db9e-dd8d-4af4-b4af-c9667cad3e75.png"><img height="340px" src="https://user-images.githubusercontent.com/3173176/158045251-e959db9e-dd8d-4af4-b4af-c9667cad3e75.png"></img></a>

# Package indexes

Now seems like a good time to re-highlight [Aquila](https://aquila.red/) by [@nektro](https://github.com/nektro):

> A federated package index and CI system for the Zig programming language built around the Zigmod package manager.

Aquila recently got support for [statistics](https://aquila.red/stats) and README rendering.

As well you should check out [zig.pm](https://zig.pm/), the Zig package aggregator by [@MasterQ32](https://github.com/MasterQ32) which you can [read about here](https://zig.news/xq/zig-package-aggregator-58co).

# s2s: struct to stream | stream to struct

[@MasterQ32](https://github.com/MasterQ32) released an excellent binary serialization library, [ziglibs/s2s](https://github.com/ziglibs/s2s):

> * Convert (nearly) any Zig runtime datatype to binary data and back.
> * Computes a stream signature that prevents deserialization of invalid data.
> * No support for graph like structures. Everything is considered to be tree data.

<a align="center" href="https://user-images.githubusercontent.com/3173176/158045305-8ab0f991-51fc-4101-ba7e-15ddf9ec69bb.png"><img height="340px" src="https://user-images.githubusercontent.com/3173176/158045305-8ab0f991-51fc-4101-ba7e-15ddf9ec69bb.png"></img></a>

# Mustache logic-less template rendering

[@batiati](https://github.com/batiati) is implementing logic-less [Mustache template rendering](https://github.com/batiati/mustache-zig) so your Zig code can render template strings like `Hello {{name}} from Zig`.

# 2-day meetup in Milan, Italy. Apr 9-10

The first ever European Zig meetup is happening Apr 9-10 in Milan, Italy! If you'd like to attend, there's plenty of room - [you can find more information here](https://zig.news/kristoff/zig-milan-party-2022-final-info-schedule-1jc1)

# Thanks for reading!

If you like my work on zigmonthly, [Mach engine](https://devlog.hexops.com/categories/mach), etc. consider [sponsoring me on GitHub](https://github.com/sponsors/slimsag) so I can do even more of it!
