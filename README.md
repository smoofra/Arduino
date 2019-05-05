64bit only build for Mac OS
================

This branch replaces three of the packages that go into Arduino with rebuilt
ones without any 32 bit binaries.

These rebuilt packages are downloaded to the following tarballs:

* `build/macosx/avr-gcc-5.4.0-atmel3.6.1-arduino2-x86_64-apple-darwin11.tar.bz2`
* `build/macosx/avrdude-6.3.0-arduino14-x86_64-apple-darwin11.tar.bz2`
* `build/arduino-builder-macosx-fixed-1.4.1.tar`

The changes for eac package are linked as submodules in `./packages/`

To build the the first two
-----------------
Just run `package-avr-gcc.bash`, and `package-avrdude.bash`, and move the files into `build`.

I've uploaded tarballs as "releases" in those fork repos on github, and linked
them in `build.xml`, so ant should actually download and install those
automatically without you needing to rebuild them.

For the last one
-----------------

It's called arduino-builder but what really needs rebuilt is ctags, which is
packaged along with it.

I couldn't find a package script, so I wrote my own goofy one that just patches
the official one, it's called `package.sh` in my ctags branch.  This patched
`arduino-builder` tarball is also "released" in my ctags fork.


Arduino
========

* Arduino is an open-source physical computing platform based on a simple I/O
board and a development environment that implements the Processing/Wiring
language. Arduino can be used to develop stand-alone interactive objects or
can be connected to software on your computer (e.g. Flash, Processing and MaxMSP).
The boards can be assembled by hand or purchased preassembled; the open-source
IDE can be downloaded for free at https://www.arduino.cc/en/Main/Software

* For more information, see the website at: https://www.arduino.cc/
or the forums at: https://forum.arduino.cc/  
You can also follow Arduino on Twitter at: https://twitter.com/arduino or
like Arduino on Facebook at: https://www.facebook.com/official.arduino

* To report a *bug* in the software or to request *a simple enhancement* go to:
https://github.com/arduino/Arduino/issues

* More complex requests and technical discussion should go on the Arduino Developers
mailing list:
https://groups.google.com/a/arduino.cc/forum/#!forum/developers

* If you're interested in modifying or extending the Arduino software, we strongly
suggest discussing your ideas on the Developers mailing list *before* starting
to work on them. That way you can coordinate with the Arduino Team and others,
giving your work a higher chance of being integrated into the official release
https://groups.google.com/a/arduino.cc/forum/#!forum/developers

Installation
------------
Detailed instructions for installation in popular operating systems.  
For Linux: https://www.arduino.cc/en/Guide/Linux (see also the Arduino playground page https://playground.arduino.cc/Learning/Linux)   
For macOS X: https://www.arduino.cc/en/Guide/MacOSX   
For Windows: https://www.arduino.cc/en/Guide/Windows

Credits
--------
Arduino is an open source project, supported by many.

The Arduino team is composed of Massimo Banzi, David Cuartielles, Tom Igoe
and David A. Mellis.

Arduino uses
[GNU avr-gcc toolchain](https://gcc.gnu.org/wiki/avr-gcc),
[GCC ARM Embedded toolchain](https://launchpad.net/gcc-arm-embedded),
[avr-libc](http://www.nongnu.org/avr-libc/),
[avrdude](http://www.nongnu.org/avrdude/),
[bossac](http://www.shumatech.com/web/products/bossa),
[openOCD](http://openocd.org/)
and code from [Processing](https://www.processing.org)
and [Wiring](http://wiring.org.co).

Icon and about image designed by [ToDo](https://www.todo.to.it/)

