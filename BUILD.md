Tested on:
- CentOS 6.5		i686 and x86_64
- Ubuntu 14.04 LTS	i386 and x86_64
- Debian 7.6		i386 and x86_64

Build with:
$ ./build_all

Result:
package/ffmpeg-<ver>-<os>-<os_ver>-<arch>.tar.bz2

Built files:

build/bin/ffmpeg					--> /usr/bin/ffmpeg
build/bin/ffprobe					--> /usr/bin/ffprobe

build/lib/frei0r-1/*.so					--> /usr/lib/frei0r-1/

build/ffmpeg-prefix/src/ffmpeg/doc/ffmpeg.1*		--> /usr/share/man/man1/
build/ffmpeg-prefix/src/ffmpeg/doc/ffprobe.1*		--> /usr/share/man/man1/

build/ffmpeg-prefix/src/ffmpeg/doc/ffprobe.xsd		--> /usr/share/ffmpeg/
build/ffmpeg-prefix/src/ffmpeg/presets/*.ffpreset	--> /usr/share/ffmpeg/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/*.c		--> /usr/share/ffmpeg/examples/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/Makefile	--> /usr/share/ffmpeg/examples/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/README	--> /usr/share/ffmpeg/examples/

build/ffmpeg-prefix/src/ffmpeg/Changelog		--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/COPYING*			--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/CREDITS			--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/INSTALL*			--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/LICENSE*			--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/MAINTAINERS		--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/README*			--> /usr/share/doc/ffmpeg-2.4.2/
build/ffmpeg-prefix/src/ffmpeg/RELEASE_NOTES		--> /usr/share/doc/ffmpeg-2.4.2/