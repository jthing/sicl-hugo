---
title: "Improved GC"
tags: ["none"]
draft: false
---

## Improved GC {#improved-gc}

Hayley's algorithm in initiated by:

git clone <https://github.com/sbcl/sbcl>; cd sbcl;SBCL_MAKE_JOBS="-j" SBCL_MAKE_PARALLEL=42069
./make.sh --with-mark-region-gc

It's improvement of performance on my machine is pure magic.
