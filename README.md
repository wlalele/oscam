OSCam: Open Source Conditional Access Module
============================================


License
=======

OSCam: Open Source CAM
Copyright (C) 2009-2015 OSCam developers

OSCam is based on the Streamboard mp-cardserver 0.9d by dukat and
has been extended and worked on by many more since then.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.

For the full text of the licese, please read COPYING file in OSCam
top directory or visit http://www.gnu.org/licenses/gpl-3.0.html


Version history
===============

OSCam history is accessible through Trac timeline at:
   http://www.streamboard.tv/oscam/timeline/


Repositories
============

SVN repository:
   svn checkout http://www.streamboard.tv/svn/oscam/trunk oscam-svn


Building OSCam from source
==========================

 - Get the lastest sources from SVN
    svn checkout http://www.streamboard.tv/svn/oscam/trunk oscam-trunk

 - Go to oscam-trunk directory.

 - Run `make config` to choose the features you want.

 - Run `make` to compile OSCam.

For more information and examples on using the build system, please
see README.build and README.config files.


Building OScam for different CPUs (cross-compilation)
=====================================================

First you need to install the target CPU toolchain. Already built toolchains
for various architectures can be downloaded from:

    http://www.streamboard.tv/oscam/wiki/crosscompiling/

In order to cross compile OSCam you need to set CROSS variable when
running make. For example to compile for SH4 architecture you need
to run: `make CROSS=sh4-linux-` or if your cross compilers are not
in your PATH - `make CROSS=/opt/STM/STLinux-2.3/devkit/sh4/bin/sh4-linux-`.


Dependencies
============

OSCam by default do not depend on external libraries except when compilation
with SSL is requested. In that case openssl (libcrypto) library must be
installed.

OSCam supports building with the following external dependencies:
  - libcrypto (libssl) - 'make USE_LIBCRYPTO=1'
  - libusb             - 'make USE_LIBUSB=1'
  - PCSC               - 'make USE_PCSC=1'
  - SH4 STAPI support  - 'make USE_STAPI=1'
  - SH4 STAPI5 support - 'make USE_STAPI5=1'
  - Coolapi support    - 'make USE_COOLAPI=1'
  - AZBOX support      - 'make USE_AZBOX=1'

For STAPI support you need to download liboscam_stapi.a library and place
it in stapi directory under oscam/ root dir. liboscam_stapi.a can be downloaded
from: http://www.streamboard.tv/wbb2/thread.php?threadid=28854

For STAPI5 support you need to download liboscam_stapi5.a library and place
it in stapi directory under oscam/ root dir. liboscam_stapi5.a can be downloaded
from: http://www.streamboard.tv/wbb2/thread.php?postid=541107#post541107

For more information and examples on using the build system, run `make help`.


Help and Support
================

man pages and configuration examples are in Distribution/doc directory.

You may visit our Trac system for tracking and filling bug reports.
   http://www.streamboard.tv/oscam/

If you experience any problems with OSCam, feel free to post in our support
forum under (mainly German and English language) at:
   http://www.streamboard.tv/wbb2/portal.php

Configuration wiki:
   http://www.streamboard.tv/wiki/index.php/OSCam/
