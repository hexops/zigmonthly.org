---
title: "Zig monthly, September 2021: Unicode, Android, cross-platform GUIs, learning resources & more"
date: 2021-09-25T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/134820515-8d672889-4deb-4b82-bec0-8497de9293f8.png"]
---

<a href="https://user-images.githubusercontent.com/3173176/134820515-8d672889-4deb-4b82-bec0-8497de9293f8.png"><img width="480px" src="https://user-images.githubusercontent.com/3173176/134820515-8d672889-4deb-4b82-bec0-8497de9293f8.png"></img></a>


# Slingworks & The Underburrow game

> _Underburrow is a speed running platformer game where you gather momentum with well timed button taps_

[@JonSnowbd shares _Slingworks 0.1_](https://github.com/JonSnowbd/slingworks): a simple and powerful Windows+Linux 'bring your content' engine built in Zig, as well as [Underburrow](https://github.com/JonSnowbd/underburrow): an all encompassing example for how Slingworks development works.

<video width="480px" src="https://user-images.githubusercontent.com/3173176/134818362-4736ee45-1aa0-407c-92b0-c4a5b301d4d4.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/134818362-4736ee45-1aa0-407c-92b0-c4a5b301d4d4.mp4">
        <img width="480px" src="https://user-images.githubusercontent.com/3173176/134818764-20d3f95c-090c-4000-8595-7e205247360e.png"></img>
    </a>
</video>

Both are still heavily under development, but it's already quite cool:

<a href="https://user-images.githubusercontent.com/3173176/134818377-5f4f40dc-9436-4aef-906e-7256d8f5c2a9.png"><img width="240px" src="https://user-images.githubusercontent.com/3173176/134818377-5f4f40dc-9436-4aef-906e-7256d8f5c2a9.png"></img></a> <a href="https://user-images.githubusercontent.com/3173176/134818383-1a2d2e23-0907-47cb-89be-b2b019e487b5.png"><img width="240px" src="https://user-images.githubusercontent.com/3173176/134818383-1a2d2e23-0907-47cb-89be-b2b019e487b5.png"></img></a>

<a href="https://user-images.githubusercontent.com/3173176/134818386-bcadf2f4-08c6-4b3b-8770-b06a8a7a1721.png"><img width="240px" src="https://user-images.githubusercontent.com/3173176/134818386-bcadf2f4-08c6-4b3b-8770-b06a8a7a1721.png"></img></a> <a href="https://user-images.githubusercontent.com/3173176/134818389-a8840e3c-cb5d-43d8-b71e-2a7e7a4c56f0.png"><img width="240px" src="https://user-images.githubusercontent.com/3173176/134818389-a8840e3c-cb5d-43d8-b71e-2a7e7a4c56f0.png"></img></a>

Check it out: [Slingworks](https://github.com/JonSnowbd/slingworks) | [Underburrow](https://github.com/JonSnowbd/underburrow)

# Unicode

Unicode is complex: even in languages with excellent support for it such as Go (by creators as UTF-8 itself) there is still regular confusion and subtle bugs [lurking behind incorrect assumptions about what runes/code-points and grapheme clusters are.](https://www.reddit.com/r/golang/comments/o1o5hr/fyi_a_single_go_rune_is_not_the_same_as_a_single/).

Zig has, thus far, taken a _lighter weight_ stance on Unicode: there are no native unicode types in the language, and the standard library is light weight in terms of Unicode support.

But many in the Zig community, myself included, care about Unicode support immensely - and [@jecolon](https://github.com/jecolon) has been working tirelessly on two libraries:

* [Ziglyph](https://github.com/jecolon/ziglyph): Unicode text processing for the Zig Programming Language.
* [Zigstr](https://github.com/jecolon/zigstr): A UTF-8 string type (which exposes Grapheme clusters instead of code points to avoid foot-guns.)

As well as a series of articles:

* [Unicode basics in Zig](https://zig.news/dude_the_builder/unicode-basics-in-zig-dj3)
* [Ziglyph Unicode wrangling](https://zig.news/dude_the_builder/ziglyph-unicode-wrangling-llj)
* [Unicode string operations](https://zig.news/dude_the_builder/unicode-string-operations-536e)

[@andrewrk](https://github.com/andrewrk) and [@jecolon](https://github.com/jecolon) are also [working together](https://github.com/ziglang/zig/issues/234#issuecomment-922065852) to ensure Zig's `std.unicode` library is a reasonable API in general before Zig 1.0.

# Android support

[@MasterQ32 has created a Zig android template repository](https://github.com/MasterQ32/ZigAndroidTemplate) - showing off how to create a minimal Android app in Zig.

Also see his earlier 2021 FOSDEM talk: [Create an Android Application with Zig](https://fosdem.org/2021/schedule/event/zig_android/) - I've included a short clip of the demo within for your enjoyment:

<video width="480px" src="https://user-images.githubusercontent.com/3173176/134788433-811ce689-ed38-40d3-8fda-09f5364e9734.mov" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/134788433-811ce689-ed38-40d3-8fda-09f5364e9734.mov">
        <img width="480px" src="https://user-images.githubusercontent.com/3173176/134788463-ee505626-01d0-435c-9f74-05b0483aee74.png"></img>
    </a>
</video>

Felix also has aspirations to do Zig-on-iOS work, so please [consider sponsoring him](https://github.com/sponsors/MasterQ32) for some Apple hardware if his work appeals to you!

# Test your C code with Zig

[@Pixeli](https://twitter.com/TommiSinivuo) on Twitter has shared an extremely cool topic: [how to easily test your existing C code using Zig](https://twitter.com/TommiSinivuo/status/1432393016761856003).

# IUP (cross platform GUI) for Zig

Rafael Batiati has shared a very interesting article: [IUP for Zig](https://zig.news/batiati/iup-for-zig-4ah):

> It's a cross-platform GUI toolkit developed by PUC-RIO, the same university behind the excellent Lua language.

<a href="https://user-images.githubusercontent.com/3173176/134789187-8e3eddef-30e2-4fd7-b296-eb4de0f911f1.png"><img width="480px" src="https://user-images.githubusercontent.com/3173176/134789187-8e3eddef-30e2-4fd7-b296-eb4de0f911f1.png"></img></a>

<a href="https://user-images.githubusercontent.com/3173176/134789196-25ead67b-3939-49a1-b065-1ba77762ceb1.png"><img width="480px" src="https://user-images.githubusercontent.com/3173176/134789196-25ead67b-3939-49a1-b065-1ba77762ceb1.png"></img></a>

# Robinhood hash tables

[Kenta Iwasaki](https://github.com/lithdew) shared their robin hash table implementation:

> A robin hood hash table that keeps entries lexicographically sorted. Assumes that keys are 256-bit cryptographic hashes. Able to insert 25.8 million entries per second, query 30.83 million entries per second, and delete 24.21 million entries per second.
> 
> Using it as one of the core main-memory data structures for a blockchain I'm writing in Zig called Rheia. Wrote and improved upon the data structure based on Twitter comments and articles made by Per Vognsen and Paul Khuong.
> 
> Beats any other sorted data structure I've benchmarked so far in terms of insertion/query/deletion throughput by 3-4x order of magnitudes.
> 
> https://github.com/lithdew/rheia/blob/master/hash_map.zig 

# Ray tracing in a weekend

[@Jack-Ji has implemented](https://github.com/Jack-Ji/ray-tracing-weekend.zig) the famous [ray-tracing-in-a-weekend](https://raytracing.github.io) in Zig:

<a href="https://user-images.githubusercontent.com/3173176/134789958-20a0d223-6510-42b5-8878-d7ad94f8c14c.png"><img width="480px" src="https://user-images.githubusercontent.com/3173176/134789958-20a0d223-6510-42b5-8878-d7ad94f8c14c.png"></img></a>

# Fast LRU cache

Also brought to us by [Kenta Iwasaki](https://github.com/lithdew):

> Wrote a really fast LRU cache that is an amalgamation of both a robin hood hash table and a doubly-linked deque.
> 
> On my laptop, with a max load factor of 50%, roughly:
> 
> - 19.81 million entries can be upserted per second.
> - 20.19 million entries can be queried per second.
> - 9.97 million entries can be queried and removed per second.
>
> The code is available here w/ unit tests and benchmarks: https://github.com/lithdew/rheia/blob/master/lru.zig

# Exceptional articles

* [Crafting an Interpreter in Zig](https://zig.news/andres/crafting-an-interpreter-in-zig-part-1-jdh) - Andres
* [Zig build explained](https://zig.news/xq/zig-build-explained-part-1-59lf) - Felix "xq" Queißner
* [Interfaces in Zig](https://zig.news/david_vanderson/interfaces-in-zig-o1c) - David Vanderson
* [Struct of Arrays (SoA) in Zig? Easy & in Userland!](https://zig.news/kristoff/struct-of-arrays-soa-in-zig-easy-in-userland-40m0) - Loris Cro
* [How to use hash map contexts to save memory when doing a string table](https://zig.news/andrewrk/how-to-use-hash-map-contexts-to-save-memory-when-doing-a-string-table-3l33) - Andrew Kelley
* [Code coverage for Zig](https://zig.news/squeek502/code-coverage-for-zig-1dk1) - Ryan Liptak
* [Resource efficient Thread Pools with Zig](https://zig.news/kprotty/resource-efficient-thread-pools-with-zig-3291) - Protty

# Learning Zig

![ziglings](https://user-images.githubusercontent.com/1458409/109398392-c1069500-790a-11eb-8ed4-7d7d74d32666.jpg)

Now seems like an excellent time to point out two resources for anyone considering learning Zig:

* [Ziglings](https://github.com/ratfactor/ziglings): a series of tiny broken programs. By fixing them, you'll learn how to read and write Zig code.
* [ziglang.org/documentation/master](https://ziglang.org/documentation/master)
* [ziglearn.org](https://ziglearn.org)

# New Zig tutorials

Since [last month's beginner tutorials](https://zigmonthly.org/letters/2021/august/#tutorials), https://zig.news has blown up with awesome tutorials all around:

* Intro to Zig - Sobeston:
  * [Fizz Buzz](https://zig.news/sobeston/fizz-buzz-3fao)
  * [Fahrenheit to Celsius](https://zig.news/sobeston/fahrenheit-to-celsius-akf)
  * [A guessing game](https://zig.news/sobeston/a-guessing-game-5fb1)
* [What's undefined in Zig?](https://zig.news/kristoff/what-s-undefined-in-zig-9h) - Loris Cro
* [What's a String Literal in Zig?](https://zig.news/kristoff/what-s-a-string-literal-in-zig-31e9) - Loris Cro
* [How to Add Buffering to a Reader / Writer in Zig](https://zig.news/kristoff/how-to-add-buffering-to-a-writer-reader-in-zig-7jd) - Loris Cro
* C/C++/Zig interoperability - Loris Cro
  * [Extend a C/C++ Project with Zig](https://zig.news/kristoff/extend-a-c-c-project-with-zig-55di)
  * [Make Zig Your C/C++ Build System](https://zig.news/kristoff/make-zig-your-c-c-build-system-28g5)
  * [Cross-compile a C/C++ Project with Zig](https://zig.news/kristoff/cross-compile-a-c-c-project-with-zig-3599)
  * [Compile a C/C++ Project with Zig](https://zig.news/kristoff/compile-a-c-c-project-with-zig-368j)

# New podcasts & videos

* [Zig ⚡ SHOWTIME #29: Don't Rewrite, Reinvent!](https://www.youtube.com/watch?v=tQHTvQqBhS8)
* [CoffeeTIME: The ZSF is 1 year old!](https://youtu.be/QFOxAUjXe0g)
* [CoffeeTIME: AWS ❤️ Rust](https://www.youtube.com/watch?v=1F5eprScpvA) - an insightful discussion about the relationship between AWS and Rust
* Launching the [TigerBeetle $20,000 consensus challenge](https://www.tigerbeetle.com/20k-challenge), there was a 2.5 hour [Zig ⚡ SHOWTIME #28: Viewstamped Replication Made Famous](https://www.youtube.com/watch?v=_Jlikdtm4OA).
* [Viewstamped Replication Made Famous - Joran Greef](https://www.youtube.com/watch?v=qeWyc8G-lq4)
* [Revisiting Viewstamped Replication with Brian Oki and James Cowling](https://www.youtube.com/watch?v=ps106zjmjhw)
* [Coderlyfe](https://www.youtube.com/channel/UCpaTqf90rm1jmJI49BtVMRw) has been steadily producing a series of Zig video tutorials if that's your cup of mocha:
  * [Optionals](https://www.youtube.com/watch?v=4XrsIOkS5sY)
  * [Blocks and closures](https://www.youtube.com/watch?v=hv71foOAPVk)
  * [Errors / exception handling](https://www.youtube.com/watch?v=t9EUoSojDUw)
  * [Allocators](https://www.youtube.com/watch?v=bS7jtl-CoEs)
  * [Unions/variants](https://www.youtube.com/watch?v=JEHZJHfiAfk)
  * [Structs and OOP](https://www.youtube.com/watch?v=NN1GC0E8J6I)

# Upcoming events

[Handmade Seattle](https://www.handmade-seattle.com) has several attendees from the Zig community, as well as talks and demos for Zig November 11-12, 2021.

P.S. In case you missed it, [Zig 0.8.1 has been released](https://ziglang.org/download/0.8.1/release-notes.html)!

---

If you're one of the 150+ subscribers or [3.5k+ viewers](https://zigmonthly.org/privacy), thanks for reading!

Please consider [supporting my work](https://github.com/sponsors/slimsag)
