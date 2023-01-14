# Part 2 - Prerequisite Knowledge

Meadowlark's codebase is written almost exclusively in [Rust](https://www.rust-lang.org/). If you haven't already, I recommend at-least going through as much of the [Official Rust Book] as you can.

There are however a few notable places where we don't use Rust:
* The website is standard web dev stuff. If you are interested in helping with the website, here is a link to the [website repository](https://github.com/MeadowlarkDAW/MeadowlarkDAW.github.io).
* The [`meadowlark-clap-exts`](https://github.com/MeadowlarkDAW/meadowlark-clap-exts) repository is written in C. This is to allow third party plugins to use our custom CLAP extensions more easily.
* If you are planning to contribute pure DSP algorithms, you are allowed to use whatever programming language you are comfortable with as long as the DSP algorithm is self-contained with no external dependencies. Another team member can translate the algorithm to Rust once you are done.

### Some additional resources for learning Rust
- [How to learn modern Rust] - An extensive list of resources for learning Rust.
- [Rust By Practice] - A great unofficial online book that helps you learn Rust through excersises.
- [Learn Rust the Dangerous Way] - Tips on writing low-level Rust code from a C background.
- [The Rust Performance Book] - Tips on optimizing code in Rust.
- [How-to Optimize Rust Programs on Linux] - Guide on how to profile Rust code on Linux.

# GUI Prerequisites

Meadowlark uses the [Vizia](https://github.com/vizia/vizia) GUI library for its frontend, so if you are planning to contribute to the UI, I would at least learn the basics of how Vizia works first.

---

[Part 3 - Repository Overview](./Part_3_Repository_Overview.md)

[Official Rust Book]: https://doc.rust-lang.org/book/
[How to learn modern Rust]: https://github.com/joaocarvalhoopen/How_to_learn_modern_Rust
[Rust By Practice]: https://practice.rs/why-exercise.html
[Learn Rust the Dangerous Way]: http://cliffle.com/p/dangerust/
[The Rust Performance Book]: https://nnethercote.github.io/perf-book/title-page.html
[How-to Optimize Rust Programs on Linux]: http://www.codeofview.com/fix-rs/2017/01/24/how-to-optimize-rust-programs-on-linux/