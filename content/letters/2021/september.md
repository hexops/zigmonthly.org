---
title: "Zig monthly, September 2021: TODO"
date: 2021-10-29T00:00:00-07:00
draft: false
images: ["https://user-images.githubusercontent.com/3173176/128805441-9f809577-7182-475a-9916-f26b93ed1635.png"]
---

TODO: main article image

# TODO - for consideration
* Highlights:
  * test C code with Zig https://twitter.com/TommiSinivuo/status/1432393016761856003
  * android support https://twitter.com/ikskuh/status/1432717320732954624
  * worth mentioning or nah? self-project https://twitter.com/lemire/status/1429466213537751045
  * Aetherwind on Discord https://discord.com/channels/605571803288698900/634812978994085888/885689223691264011
  * xq grid-based editor https://discord.com/channels/605571803288698900/634812978994085888/885276121300611123
  * robinhood hash table: https://discord.com/channels/605571803288698900/605572611539206171/875057467904630835
    > A robin hood hash table that keeps entries lexicographically sorted. Assumes that keys are 256-bit cryptographic hashes. Able to insert 25.8 million entries per second, query 30.83 million entries per second, and delete 24.21 million entries per second. Using it as one of the core main-memory data structures for a blockchain I'm writing in Zig called Rheia. Wrote and improved upon the data structure based on Twitter comments and articles made by Per Vognsen and Paul Khuong. Beats any other sorted data structure I've benchmarked so far in terms of insertion/query/deletion throughput by 3-4x order of magnitudes. https://github.com/lithdew/rheia/blob/master/hash_map.zig
  * LRU cache https://discord.com/channels/605571803288698900/605572611539206171/875832055865442396
  * real-time pathtracer https://discord.com/channels/605571803288698900/605572611539206171/875207278188462080
    * screenshot: https://discord.com/channels/605571803288698900/605572611539206171/882107088824844318
  * webassembly constellation map https://discord.com/channels/605571803288698900/605572611539206171/878813863234125835
  * curl clone https://discord.com/channels/605571803288698900/605572611539206171/879967495396655104
  * boids animation https://discord.com/channels/605571803288698900/605572611539206171/880161701943734323
  * ray-tracing-in-a-weekend https://discord.com/channels/605571803288698900/605572611539206171/881273187042738258
    * https://discord.com/channels/605571803288698900/605572611539206171/881578121697058827
  * HTML parsing https://discord.com/channels/605571803288698900/605572611539206171/883020251900567622
  * xxhash https://discord.com/channels/605571803288698900/605572611539206171/884981979848773672
  * 
* Tutorials:
  * reminder about past tutorials - maybe aggregate them somewhere?
  * https://twitter.com/rhamorim/status/1426224138016989185
  * Experienced
    * Series of articles on C/C++/Zig https://zig.news/kristoff/series/3:
      * [Extend a C/C++ Project with Zig - Loris Cro](https://zig.news/kristoff/extend-a-c-c-project-with-zig-55di)
      * [Make Zig Your C/C++ Build System - Loris Cro](https://zig.news/kristoff/make-zig-your-c-c-build-system-28g5)
      * [Cross-compile a C/C++ Project with Zig - Loris Cro](https://zig.news/kristoff/cross-compile-a-c-c-project-with-zig-3599)
      * [Compile a C/C++ Project with Zig - Loris Cro](https://zig.news/kristoff/compile-a-c-c-project-with-zig-368j)
    * [Struct of Arrays (SoA) in Zig? Easy & in Userland! - Loris Cro](https://zig.news/kristoff/struct-of-arrays-soa-in-zig-easy-in-userland-40m0)
    * [How to use hash map contexts to save memory when doing a string table - Andrew Kelley](https://zig.news/andrewrk/how-to-use-hash-map-contexts-to-save-memory-when-doing-a-string-table-3l33)
    * [Crafting an Interpreter in Zig - 2 part series - Andres](https://zig.news/andres/crafting-an-interpreter-in-zig-part-1-jdh)
  * Beginner
    * [Interfaces in Zig - David Vanderson](https://zig.news/david_vanderson/interfaces-in-zig-o1c)
    * [zig build explained - 2 part series - Felix "xq" Queißner](https://zig.news/xq/zig-build-explained-part-1-59lf)
    * [What's undefined in Zig? - Loris Cro](https://zig.news/kristoff/what-s-undefined-in-zig-9h)
    * [What's a String Literal in Zig? - Loris Cro](https://zig.news/kristoff/what-s-a-string-literal-in-zig-31e9)
    * [How to Add Buffering to a Reader / Writer in Zig - Loris Cro](https://zig.news/kristoff/how-to-add-buffering-to-a-writer-reader-in-zig-7jd)
* Podcasts/videos:
  * reminder about past podcasts & videos - maybe aggregate them somewhere?
  * https://www.youtube.com/channel/UCpaTqf90rm1jmJI49BtVMRw
  * https://www.youtube.com/watch?v=_Jlikdtm4OA https://www.tigerbeetle.com/20k-challenge

# New Zig tutorials

[Loris Cro, VP of community at the Zig Software Foundation](https://kristoff.it) has been putting together multiple beginner tutorials over on https://zig.news:

- [Where is print() in Zig?](https://zig.news/kristoff/where-is-print-in-zig-57e9)
- [How to Add Buffering to a Reader / Writer in Zig](https://zig.news/kristoff/how-to-add-buffering-to-a-writer-reader-in-zig-7jd)
- [What's a String Literal in Zig?](https://zig.news/kristoff/what-s-a-string-literal-in-zig-31e9)
- [What's undefined in Zig?](https://zig.news/kristoff/what-s-undefined-in-zig-9h)

# New podcasts & videos

# Upcoming events

---

Enjoying Zig monthly? Please consider [supporting my work](https://github.com/sponsors/slimsag)
