<!--
SPDX-FileCopyrightText: 2026 Neptuwunium

SPDX-License-Identifier: CC0-1.0
-->

# meson-cross

cross and host files for meson

basically, i'm tired of copying the same text file everywhere.

## note on cross/x86_64-w64-mingw32-clang.txt

due to https://github.com/mesonbuild/meson/issues/15923

meson will not compile with this cross file without first removing the offending `-Wl,--allow-shlib-undefined` from the ninja/make file.

consequently, if you have mingw compiled with pthreads (i.e. for wine) you will need to always include threads as a dependency.

## usage

refer to https://mesonbuild.com/Cross-compilation.html

i.e.

```sh
meson setup builddir --cross-file x86_64-w64-mingw32-clang.txt --native-file x86_64-pc-linux-clang.txt
```
