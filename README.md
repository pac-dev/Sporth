# Sporth

Sporth (short for SoundPipe fORTH), is a small stack-based musical language, roughly
inspired by stack languages like Forth and PostScript.

## Features

- Stack oriented paradigm
- Written entirely in C
- 100+ unit generators to choose from
- Powered by the Soundpipe DSP library
- Unix-Friendly
- Small codebase
- Powerful C API
- Easily extendable
- Easily embeddable


## Installation

In order to compile Sporth, The development "dev" version of [SoundPipe](http://www.github.com/PaulBatchelor/soundpipe.git) 
needs to be installed. 
**When you clone soundpipe, be sure to use the 'dev' branch of soundpipe with 'git checkout dev'.**
*Note: The development branch of Soundpipe is used because on any given day, there are 
more modules there than in the master branch. More modules = more fun :)*

Then:

1. make
2. sudo make install

### Some notes on Windows
Windows users should be able to compile Sporth and libsporth using [msys2](http://www.msys2.org). 
Due to some interesting quirks an platform differences, some features will need to be disabled.

To get Sporth compiled:

1. run "make conifg.mk" to generate the configuration file. 
2. Inside config.mk, uncomment NO\_LIBSNDFILE, NO\_LIBDL, and NO\_SPA.
3. Inside config.mk, disable the live coding interface by commenting out the variable LIVE\_CODING.
4. make
5. make install


## Quick start

To see Sporth in action, run this command from the inside the project directory:

```
sporth -d 5s -o dialtone.wav examples/dialtone.sp 
```

This will generate a 5 second audio clip of sound.

More information on Sporth can be found 
[here](http://paulbatchelor.github.io/proj/sporth.html).

## Examples

Several examples demonstrating specific ugens can be found in 
the [examples](examples) folder of the repository. More musical
examples can be found on my 
[Sporthlings page](http://www.pbat.ch/sporthlings).
