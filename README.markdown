# colorize-gimp 

An implementation of Colorization using Optimization, an algorithm created by Anat Levin, Dani Lischinski, and Yair Weiss.

Plugin for The Gimp. Stills only.

Examples of the algorithm: http://www.cs.huji.ac.il/~yweiss/Colorization/

Implemented by Christopher Lais https://github.com/zinx/
Optimizations by https://bitbucket.org/grimboy/colorize-gimp

## Installation

To install:

    $ make
    $ cp colorize ~/.gimp-2.6/plug-ins/

Needs libsuitesparse.

On Ubuntu 9.04:
`sudo apt-get install libsuitesparse-3.2.0 libsuitesparse-dev`

On OSX
Use e.g. Macports and `sudo port install suitesparse` in the terminal 

## Hints for compiling 

On Linux you need to install the gtk libraries first:
`sudo aptitude install libgtk2.0-dev`

Note that `apt-get` won't work as well as it won't resolve the dependency issues properly.

Also libsuitesparse-dev is required for compiling
`sudo aptitude install libsuitesparse-dev`

You also need the gimp development package
`sudo aptitude install libgimp2.0-dev`

Windows users will probably need something like CodeBlocks with the MingGW compiler
http://www.codeblocks.org/downloads/binaries

Then get the GTK dependencies from somewhere.
This [translated page](http://translate.google.com/translate?hl=en&sl=de&u=http://www.pronix.de/pronix-1212.html&prev=/search%3Fq%3Dbuild%2Ba%2BGIMP%2Bplug-in%2Bon%2Bwindows%2Bcodeblocks%26hl%3Den%26tbo%3Dd%26biw%3D1278%26bih%3D518&sa=X&ei=9WWhUKWtLOrQyAG8jIGIBQ&ved=0CDsQ7gEwAQ) has a bit of help.

On some systems there's a problem with lf77blas and people get an error like:

    /usr/lib/gcc/x86_64-pc-linux-gnu/4.6.3/../../../../x86_64-pc-linux-gnu/bin/ld: cannot find -lf77blas
    collect2: ld returned 1 exit status
    make: *** [colorize] Error 1

Try modifying 'lf77blas' in the Makefile to 'lblas'

The Makefile won't work on Windows either as it has unix paths in it.

Thanks to GitHub user [opticyclic](https://github.com/opticyclic) and [reverland](https://github.com/reverland) for help on Linux


## Other resources for compiling etc.

 * http://registry.gimp.org/node/24913
 * http://www.gimpchat.com/viewtopic.php?f=9&t=839&start=0&hilit=colorize
 * http://www.gimpchat.com/viewtopic.php?f=9&t=1625
 * http://my.opera.com/area42/blog/gimp-colorize
