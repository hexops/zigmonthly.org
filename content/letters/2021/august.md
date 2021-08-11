---
title: "Zig monthly, August 2021: iOS support, tutorials, tree-sitter, a pathtracer, and more"
date: 2021-08-01T03:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/128805441-9f809577-7182-475a-9916-f26b93ed1635.png"]
---

# Announcing zigmonthly.org

Today, I am launching zigmonthly.org: a once-a-month publication where I curate all things Zig that I’ve seen since the past month from the Zig Discord channels, <a href="https://zig.news">zig.news</a>, Twitter, Reddit, etc. and do my best to come up with a nice showcase. <a href="/about">Learn more</a>

# Zig cross compiling to iOS? Yes please!

Nearly matching up with [Zig's 6th birthday](https://twitter.com/andy_kelley/status/1424163667306631168), [@kubkon](https://github.com/kubkon) (a core team member and author of Zig's MachO linker) has begun [adding minimal support for building iOS binaries with Zig, from any OS](https://github.com/ziglang/zig/pull/9532). Here's one running in the iOS emulator on a Mac:

<a href="https://user-images.githubusercontent.com/3173176/128664203-c9c0954d-fe74-43aa-964d-458f0fe74565.png"><img width="480px" src="https://user-images.githubusercontent.com/3173176/128664203-c9c0954d-fe74-43aa-964d-458f0fe74565.png"></img></a>

# Tree Sitter for Zig

[@maxxnino](https://github.com/maxxnino) has released a [tree sitter parser for Zig](https://github.com/maxxnino/tree-sitter-zig).

([Tree-sitter](https://tree-sitter.github.io/tree-sitter/) is a parsing framework from GitHub used for a variety of editors and IDEs, such as [NeoVim](https://neovim.io/doc/treesitter) and OniVim for code navigation and syntax highlighting. It's also used by static analysis tools like [Semgrep](https://semgrep.dev) and powers GitHub's code navigation features - so having an implementation for Zig could prove quite useful!)

# A twin stick shooter

@unvestigate [shared in the Zig discord](https://discord.com/channels/605571803288698900/605572611539206171/873274345160589392) a video of their twin stick shooter they began building four days ago, with all gameplay code in Zig:

<video width="480px" src="https://user-images.githubusercontent.com/3173176/128664622-b3f37ad2-56ba-47ba-bc53-4ee87893b009.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/128664622-b3f37ad2-56ba-47ba-bc53-4ee87893b009.mp4">
        <img width="480px" src="https://user-images.githubusercontent.com/3173176/128806787-a091b018-3881-46e2-804f-53ee8863cca2.png"></img>
    </a>
</video>

# Prometheus-style metrics for your Zig applications

[@vrischmann](https://github.com/vrischmann) released [a library](https://github.com/vrischmann/zig-prometheus) that enables one to add Prometheus-inspired counters, gauges, and histograms to their Zig applications - for use primarily with [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics), a Prometheus alternative.

# Positron - a web renderer frontend for Zig applications

[@MasterQ32](https://github.com/MasterQ32) has released [Positron](https://github.com/ziglibs/positron), a web renderer frontend for Zig applications. These Zig bindings to the popular [webview](https://github.com/webview/webview) library, enable one to write cross-platform HTML5 UI applications:

<a href="https://raw.githubusercontent.com/ziglibs/positron/04af916ddf4dbdf5ae44ef754e1a5ff3af1ddef9/screenshots/i3-login.png"><img width="240px" src="https://raw.githubusercontent.com/ziglibs/positron/04af916ddf4dbdf5ae44ef754e1a5ff3af1ddef9/screenshots/i3-login.png"></img></a> <a href="https://raw.githubusercontent.com/ziglibs/positron/04af916ddf4dbdf5ae44ef754e1a5ff3af1ddef9/screenshots/windows-chat.png"><img width="240px" src="https://raw.githubusercontent.com/ziglibs/positron/04af916ddf4dbdf5ae44ef754e1a5ff3af1ddef9/screenshots/windows-chat.png"></img></a>

# zigmod

[@nektro](https://github.com/nektro) continues her work on [zigmod](https://github.com/nektro/zigmod), a package manager for the Zig programming language - this month releasing v67 for various bug fixes. The project has now hit over 500 commits and 3.6k lines of code, when you add in the fact that zigmod uses a few handfuls of Zig dependencies - I think it's an interesting large Zig project.

I should also note an [official Zig package manager is planned](https://github.com/ziglang/zig/issues/943).

# A simple Karaoke player

@captainhorst [shared in the Zig Discord](https://discord.com/channels/605571803288698900/605572611539206171/873690060950761522) their recent project: a simple Karaoke player (note: video has no audio.)

[video](https://user-images.githubusercontent.com/3173176/128665375-276d55b5-3b46-4022-bf11-78043a498c04.mp4)

<video width="480px" src="https://user-images.githubusercontent.com/3173176/128665375-276d55b5-3b46-4022-bf11-78043a498c04.mp4" controls="controls" muted="muted">
    <a href="https://user-images.githubusercontent.com/3173176/128665375-276d55b5-3b46-4022-bf11-78043a498c04.mp4">
        <img width="480px" src="https://user-images.githubusercontent.com/3173176/128806923-49b0425e-b242-4230-87b5-08e0ffe14a53.png"></img>
    </a>
</video>

# A path tracer

[@msinilo](https://github.com/msinilo) shares [a detailed write-up](http://msinilo.pl/blog2/post/zig-pathtracer/) and their experience implementing a simple ray tracer in Zig - with no prior Zig experience!

> "I’ve to admit I went in completely ‘blind’, didn’t know much about the language other than some passing remarks posted on Twitter. I kinda expected another Rust, so initially was a bit put off by how “Spartan” Zig was. After I adjusted and started taking it for what it was – a modern “C+” alternative – it actually became a very fun experiment."

![](https://user-images.githubusercontent.com/3173176/128806390-0b93b3e1-9559-4a4a-85d1-440caec9bc96.png)

# Tutorials

[Loris Cro, VP of community at the Zig Software Foundation](https://kristoff.it) has been putting together multiple beginner tutorials over on https://zig.news:

- [Where is print() in Zig?](https://zig.news/kristoff/where-is-print-in-zig-57e9)
- [How to Add Buffering to a Reader / Writer in Zig](https://zig.news/kristoff/how-to-add-buffering-to-a-writer-reader-in-zig-7jd)
- [What's a String Literal in Zig?](https://zig.news/kristoff/what-s-a-string-literal-in-zig-31e9)
- [What's undefined in Zig?](https://zig.news/kristoff/what-s-undefined-in-zig-9h)

# See also

* [Full-Time Open Source With Andrew Kelley](https://corecursive.com/067-zig-with-andrew-kelley/) (podcast, transcribed)

---

Enjoying Zig monthly? Please consider [supporting my work](https://github.com/sponsors/slimsag)
