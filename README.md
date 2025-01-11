tiny_jpeg.h
===========

A header-only public domain implementation of Baseline JPEG compression.

Features:
---------

- stb-style header only library.
- Does not do dynamic allocations
- Simple API:
    - 2 API calls.
    - 3-value compression quality: 3 (best quality), 2 (Very good), 1 (Noticeable artifacts, best compression)
- Public domain

- On some systems, you may have an error:

``/usr/local/bin/ld: main.o: in function tjei_encode_and_write_MCU':
main.c:(.text+0xeb8): undefined reference to floorf'``

To fix it, you may have to link the math library

``gcc -o <OUTPUT_EXE> pipeline.o main.o -lm``

