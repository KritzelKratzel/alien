Alien - Pure Lua extensions
===========================

For more information, see http://mascarenhas.github.com/alien.


What is Alien?
--------------

Alien is a Foreign Function Interface (FFI) for Lua. An FFI lets you call functions in dynamic libraries (.so, .dylib, .dll, etc.) from Lua code without having to write, compile and link a C binding from the library to Lua. In other words, it lets you write extensions that call native code using just Lua.

Alien works on Unix-based systems and Windows. It has been tested on Linux/x86, Linux/x64, Linux/ARM, FreeBSD/x86, Windows/x86, OS X/x86, and OS X/PPC. The Windows binary uses MSVCR80.DLL for compatibility with LuaBinaries.

Installing Alien
----------------

The best way to install Alien is through [LuaRocks](http://luarocks.org): just do `luarocks install alien`.

Alien is based on libffi. On a GNU/Linux system you should be able to install it with your package manager; 
it is probably called something like `libffi-dev` (Debian, Ubuntu etc.) or `libffi-devel` (Fedora, CentOS etc.).  If your system's package manager does not have libffi, or you don't have a package manager,
you can get the source code from [the libffi project](http://sources.redhat.com/libffi/).

Alien uses the GNU build system. For detailed instructions, see INSTALL. For a quick start:

```bash
./bootstrap
./configure && make 
make install
```

You may need to supply non-default paths (e.g. if you are using a system that supports more than one version of Lua). For example, on Debian or Ubuntu:

```bash
LUA=lua5.1 CPPFLAGS='-I/usr/include/lua5.1' ./configure --libdir=/usr/local/lib/lua/5.1 --datadir=/usr/local/share/lua/5.1
```

To run some tests:

```bash
make check
```

Credits
-------

Alien is designed and implemented by Fabio Mascarenhas. It uses the great [libffi](http://sourceware.org/libffi) library by Anthony Green (and others) to do the heavy lifting of calling to and from C. The name was stolen from Common Lisp FFIs.

License
-------

Alien uses the MIT license (the same as Lua).

```The MIT License (MIT)
Copyright (c) 2008 - 2018 Fabio Mascarenhas

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
```

