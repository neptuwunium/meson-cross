<!--
SPDX-FileCopyrightText: 2026 Neptuwunium

SPDX-License-Identifier: CC0-1.0
-->

# meson-cross

cross and host files for meson

basically, i'm tired of copying the same text file everywhere.

## usage

refer to https://mesonbuild.com/Cross-compilation.html

i.e.

```sh
meson setup builddir --cross-file x86_64-w64-mingw32-clang.txt --native-file x86_64-pc-linux-clang.txt
```
