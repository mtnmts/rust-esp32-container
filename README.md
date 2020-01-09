# Rust build environment for ESP32

This image builds the rust compiler toolchain for the Xtensa ISA
using [llvm-xtensa](https://github.com/espressif/llvm-xtensa) and
[rust-xtensa](https://github.com/MabezDev).

Most of the steps in this image are based on a 
(blog post)[http://quickhack.net/nom/blog/2019-05-14-build-rust-environment-for-esp32.html] 
by Yoshinari Nomura.

# Usage

To build your project, run this in the same directory as your `Cargo.toml`.
Your project needs to be mounted in `/code` to build out of the box.

```bash
docker run -v $PWD:/code mtnmts/rust-esp32
```

If you want an interactive session to use anything inside the machine
(esptool.py is installed and in the path for example, if you want to
use elf2image).

```bash
docker run -v $PWD:/code -ti mtnmts/rust-esp32 bash
```
