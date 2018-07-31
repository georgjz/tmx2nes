# tmx2nes
This is a simple quick-and-dirty commandline tool for converting maps created with [Tiled](https://github.com/bjorn/tiled) level editor for use in NES ROMs.

It will create a background map that can be loaded into a name table in VRAM without further modification(e.g., with DMA).

This is a tool I wrote quickly out of laziness for loading background maps in homebrew NES ROM. It is unoptimized and there are no sanity checks. *Please be careful and use at own discretion.*

I admit that I shamelessly stole the code for the parser somewhere long time ago. I will attribute the original creator if I find out where I got it.

## Building
Use `make` in combination with `clang++`. The makefile(at least on my system) only works with `clang++` at the moment. You will also need the [cimg library](http://cimg.eu).

It's inconvenient but again, this was written out of laziness.

## Usage
`tmx2nes -f input.tmx -c palettenumber -o output.map`
All three flags are needed, else tmx2snes will not execute.
