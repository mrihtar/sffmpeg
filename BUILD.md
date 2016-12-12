**Tested on:**
<table>
<tr><td><b>CentOS 6.8</b>        </td><td>i386 and x86_64</td></tr>
<tr><td><b>Ubuntu 14.04.5 LTS</b></td><td>i386 and x86_64</td></tr>
<tr><td><b>Debian 7.11</b>       </td><td>i386 and x86_64</td></tr>
</table>

**Build with:**
<pre>
# ./build_all
</pre>

**Result:**
<pre>
package/ffmpeg-&lt;ver&gt;-&lt;rev&gt;-&lt;arch&gt;.tar.bz2
</pre>
and additionally on Ubuntu/Debian:
<pre>
package/ffmpeg_&lt;ver&gt;-&lt;rev&gt;_&lt;arch&gt;.deb
</pre>

**Built files:**
<pre>
build/bin/ffmpeg                                     --> /usr/bin/ffmpeg
build/bin/ffprobe                                    --> /usr/bin/ffprobe
build/bin/frmxtract                                  --> /usr/bin/frmxtract

build/lib/frei0r-1/*.so                              --> /usr/lib/frei0r-1/

build/ffmpeg-prefix/src/ffmpeg/doc/ffmpeg.1*         --> /usr/share/man/man1/
build/ffmpeg-prefix/src/ffmpeg/doc/ffprobe.1*        --> /usr/share/man/man1/

build/ffmpeg-prefix/src/ffmpeg/doc/ffprobe.xsd       --> /usr/share/ffmpeg/
build/ffmpeg-prefix/src/ffmpeg/presets/*.ffpreset    --> /usr/share/ffmpeg/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/*.c      --> /usr/share/ffmpeg/examples/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/Makefile --> /usr/share/ffmpeg/examples/
build/ffmpeg-prefix/src/ffmpeg/doc/examples/README   --> /usr/share/ffmpeg/examples/

build/ffmpeg-prefix/src/ffmpeg/Changelog             --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/COPYING*              --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/CREDITS               --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/INSTALL*              --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/LICENSE*              --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/MAINTAINERS           --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/README*               --> /usr/share/doc/ffmpeg-3.2.2/
build/ffmpeg-prefix/src/ffmpeg/RELEASE_NOTES         --> /usr/share/doc/ffmpeg-3.2.2/
</pre>
