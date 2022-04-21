# Setup guide

> Gotta rustify your Nintendo Switch 🦀

## 1) Rust

- If not yet installed, [install Rust](https://www.rust-lang.org/learn/get-started):

  - We are currently forced to build using nightly toolchains due to `build-std` feature (which allows for our cross-compiling) currently being unstable.

  - You can customize the default toolchain to be `nightly` on the installation process.

  - You can also switch using using `rustup default nightly` if you installed a stable toolchain, or install and default a nightly toolchain of your choice like this:

  ```sh
  rustup install <toolchain>
  rustup default <toolchain>
  ```

  - TL;DR: make sure your default toolchain is `nightly`!

## 2) `cargo-nx`

> NOTE: this is technically an optional step, but it's highly recommended unless you really know what you're doing!

- [`cargo-nx`](https://github.com/aarch64-switch-rs/cargo-nx) is our custom cargo subcommand to create and/or build projects. It's usage is described on its repo.

- You can always build this organization's projects and examples manually (providing your own target and linker specs), but `cargo-nx` simplifies this process (by providing them manually).

- It can be installed by the following command:

```sh
cargo install cargo-nx --git https://github.com/aarch64-switch-rs/cargo-nx
```

## 3) `rust-src`

- This is a component required for cross-compiling in Rust.

- It's installed by the following command:

```sh
rustup component add rust-src
```

## 4) Profit!

- You're done installing/preparing your Rust environment for Nintendo Switch homebrew development!

- Now you can build existing projects (with `cargo nx build`) by cloning them (via `git clone`, for instance), create new projects of your own using `cargo nx new` (more info on its repo)... it's all up to you!