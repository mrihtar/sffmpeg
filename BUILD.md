**Tested on:**
<table>
<tr><td><b>CentOS 7.5-1804</b>   </td><td>x86_64</td></tr>
<tr><td><b>Ubuntu 18.04.1 LTS</b></td><td>amd64</td></tr>
<tr><td><b>Debian 9.5</b>        </td><td>amd64</td></tr>
</table>

**Build as root with:**
<pre>
# ./build_all
</pre>
<b>build_all</b> scripts adapts to the OS, where it's running on, downloads all external
libraries, applies patches, builds binaries and creates final packages.

**Result:**
<pre>
package/ffmpeg-4.0.2-1-amd64.tar.bz2
</pre>
and additionally on Ubuntu/Debian:
<pre>
package/ffmpeg_4.0.2-1_amd64.deb
</pre>

**Built files:**
<pre>
build/bin/ffmpeg                                     --> /usr/bin/ffmpeg
build/bin/ffprobe                                    --> /usr/bin/ffprobe
build/bin/frmxtract                                  --> /usr/bin/frmxtract

build/lib/frei0r-1/*.so                              --> /usr/lib/frei0r-1/

build/ffmpeg-prefix/src/ffmpeg/doc/ffmpeg*.1         --> /usr/share/man/man1/
build/ffmpeg-prefix/src/ffmpeg/doc/ffprobe*.1        --> /usr/share/man/man1/
build/ffmpeg-prefix/src/ffmpeg/doc/lib*.3            --> /usr/share/man/man3/

build/ffmpeg-prefix/src/ffmpeg/doc/ffprobe.xsd       --> /usr/share/ffmpeg/
build/ffmpeg-prefix/src/ffmpeg/presets/*.ffpreset    --> /usr/share/ffmpeg/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/*.c      --> /usr/share/ffmpeg/examples/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/Makefile --> /usr/share/ffmpeg/examples/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/README   --> /usr/share/ffmpeg/examples/

build/ffmpeg-prefix/src/ffmpeg/Changelog             --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/COPYING*              --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/CREDITS               --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/INSTALL*              --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/LICENSE*              --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/MAINTAINERS           --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/README*               --> /usr/share/doc/ffmpeg-4.0.2/
build/ffmpeg-prefix/src/ffmpeg/RELEASE_NOTES         --> /usr/share/doc/ffmpeg-4.0.2/
</pre>
