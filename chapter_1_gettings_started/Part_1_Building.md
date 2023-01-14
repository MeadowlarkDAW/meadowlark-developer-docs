# Part 1 - Building Meadowlark

If you have not already, install the [Rust](https://www.rust-lang.org/) programming language on your system.

Next, choose a branch to fork/clone. The `main` branch is the latest stable branch, and the `dev` branch is the nighly development branch.

As of now, building Meadowlark should be very straightforward, and is the same for every platform (this may change in the future). Just run this command in the root of your cloned repository.
```
cargo run
```

Meadowlark has a lot of dependencies, so a cold build may take a while. Subsequent builds should be much faster.

You can run a more optimized build with this command. This will take longer to compile.
```
cargo run --release
```

And lastly, you can build an extra optimized build with this command (takes the longest to compile). This is the profile that will be used for official binary releases.
```
cargo run --profile release-lto
```

---

[Part 2 - Prerequisite Knowledge](./Part_2_Prerequisite_Knowledge.md)