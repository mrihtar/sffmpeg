PROJECT(sffmpeg)

CMAKE_MINIMUM_REQUIRED(VERSION 3.2) # needed for .xz support in ExternalProjects
INCLUDE(ExternalProject)
INCLUDE_DIRECTORIES(BEFORE ${CMAKE_BINARY_DIR}/include)
LINK_DIRECTORIES(${CMAKE_BINARY_DIR}/lib)
SET(ENV{PATH} ${CMAKE_BINARY_DIR}/bin:$ENV{PATH})
SET(ENV{PKG_CONFIG_PATH} ${CMAKE_BINARY_DIR}/lib/pkgconfig)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/etc)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/include)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/sbin)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/share/man)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/man/man1)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/man/man3)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/ssl)
file(MAKE_DIRECTORY ${CMAKE_BINARY_DIR}/var)
SET(CMAKE_VERBOSE_MAKEFILE ON)
SET(GIT_SHALOW ON)

EXTERNALPROJECT_ADD(
  yasm
  URL https://www.tortall.net/projects/yasm/releases/yasm-1.3.0.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR}
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  nasm
# URL https://fossies.org/linux/misc/nasm-2.15.05.tar.xz
  URL https://github.com/netwide-assembler/nasm/archive/nasm-2.15.05.tar.gz
  CONFIGURE_COMMAND ./autogen.sh COMMAND touch nasm.1 ndisasm.1 COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR}
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  z
  URL https://zlib.net/zlib-1.2.11.tar.gz
  CONFIGURE_COMMAND CFLAGS=-fPIC PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --static
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  bzip2
# URL https://fossies.org/linux/misc/bzip2-1.0.8.tar.gz
  URL https://sourceware.org/pub/bzip2/bzip2-1.0.8.tar.gz
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/bzip2-fpic.patch
  CONFIGURE_COMMAND ""
  INSTALL_COMMAND make install PREFIX=${CMAKE_BINARY_DIR}
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  xz
  URL https://tukaani.org/xz/xz-5.2.5.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  INSTALL_COMMAND make install PREFIX=${CMAKE_BINARY_DIR}
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  openssl
# Stay with older version for now (for rtmp)
  URL https://www.openssl.org/source/openssl-1.0.2u.tar.gz
# URL https://www.openssl.org/source/openssl-1.1.1h.tar.gz
  CONFIGURE_COMMAND ./config no-shared no-idea no-mdc2 no-rc5 --prefix=${CMAKE_BINARY_DIR}
  BUILD_COMMAND make depend COMMAND make
  INSTALL_COMMAND make install_sw
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  opencore-amr
  URL https://netcologne.dl.sourceforge.net/project/opencore-amr/opencore-amr/opencore-amr-0.1.5.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  fdkaac
# Stay with older version for now
# URL https://netcologne.dl.sourceforge.net/project/opencore-amr/fdk-aac/fdk-aac-0.1.6.tar.gz
  URL https://netcologne.dl.sourceforge.net/project/opencore-amr/fdk-aac/fdk-aac-2.0.1.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  mp3lame
  URL https://netcologne.dl.sourceforge.net/project/lame/lame/3.100/lame-3.100.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  ogg
  URL https://downloads.xiph.org/releases/ogg/libogg-1.3.4.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  speexdsp
  URL https://downloads.xiph.org/releases/speex/speexdsp-1.2rc3.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-sse
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  speex
  DEPENDS speexdsp ogg
  URL https://downloads.xiph.org/releases/speex/speex-1.2.0.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-sse
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  vorbis
  DEPENDS ogg
  URL https://downloads.xiph.org/releases/vorbis/libvorbis-1.3.7.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --disable-oggtest
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  theora
  DEPENDS ogg vorbis
# URL https://downloads.xiph.org/releases/theora/libtheora-1.1.1.tar.gz
  URL https://downloads.xiph.org/releases/theora/libtheora-1.2.0alpha1.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --disable-oggtest --disable-examples --with-ogg=${CMAKE_BINARY_DIR}
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  opus
  URL https://archive.mozilla.org/pub/opus/opus-1.3.1.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --disable-doc
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  xvidcore
  DEPENDS yasm
  URL https://downloads.xvid.com/downloads/xvidcore-1.3.7.tar.gz
  CONFIGURE_COMMAND cd build/generic && PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR}
  BUILD_COMMAND cd build/generic && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build/generic && make install COMMAND rm -f ${CMAKE_BINARY_DIR}/lib/libxvidcore.so ${CMAKE_BINARY_DIR}/lib/libxvidcore.so.4 ${CMAKE_BINARY_DIR}/lib/libxvidcore.so.4.3
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  x264
  DEPENDS nasm
# GIT_REPOSITORY git://git.videolan.org/x264.git
# UPDATE_COMMAND ""
# URL https://ftp.videolan.org/pub/x264/snapshots/last_stable_x264.tar.bz2
# URL https://ftp.videolan.org/pub/x264/snapshots/x264-snapshot-20190207-2245-stable.tar.bz2
  URL https://code.videolan.org/videolan/x264/-/archive/master/x264-master.tar.bz2
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --enable-static --enable-pic
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  x265
  DEPENDS yasm
# GIT_REPOSITORY https://bitbucket.org/multicoreware/x265_git
# UPDATE_COMMAND ""
# URL https://bitbucket.org/multicoreware/x265/downloads/x265_3.4.tar.gz
  URL http://anduin.linuxfromscratch.org/BLFS/x265/x265_3.4.tar.gz
  CONFIGURE_COMMAND cd build/linux && PATH=$ENV{PATH} cmake -G "Unix Makefiles" -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DENABLE_CLI:BOOL=OFF -DENABLE_SHARED:BOOL=OFF ../../source
  BUILD_COMMAND cd build/linux && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build/linux && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
ADD_CUSTOM_COMMAND(
  TARGET x265
  POST_BUILD
  WORKING_DIRECTORY ${CMAKE_BINARY_DIR}/lib/pkgconfig
  COMMAND ${CMAKE_CURRENT_SOURCE_DIR}/vendor/gcc_cleanup x265.pc
)
EXTERNALPROJECT_ADD(
  vpx
  DEPENDS yasm
  URL https://github.com/webmproject/libvpx/archive/v1.9.0.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  rtmp
  DEPENDS z openssl
# URL https://rtmpdump.mplayerhq.hu/download/rtmpdump-2.3.tgz
  GIT_REPOSITORY git://git.ffmpeg.org/rtmpdump
  UPDATE_COMMAND ""
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/rtmpdump-2.4-prefix.patch
  CONFIGURE_COMMAND ""
  BUILD_COMMAND make PREFIX=${CMAKE_BINARY_DIR} SHARED= XCFLAGS=-I${CMAKE_BINARY_DIR}/include XLDFLAGS=-L${CMAKE_BINARY_DIR}/lib XLIBS=-ldl
  INSTALL_COMMAND make PREFIX=${CMAKE_BINARY_DIR} SHARED= install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  freetype
  DEPENDS bzip2
  URL https://download.savannah.gnu.org/releases/freetype/freetype-2.10.4.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static CFLAGS=-fPIC\ -I${CMAKE_BINARY_DIR}/include LDFLAGS=-L${CMAKE_BINARY_DIR}/lib
  INSTALL_COMMAND PATH=$ENV{PATH} make install COMMAND ln -fs ${CMAKE_BINARY_DIR}/include/freetype2 ${CMAKE_BINARY_DIR}/include/freetype2/freetype
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  fribidi
# URL http://fribidi.org/download/fribidi-0.19.7.tar.bz2
  URL https://github.com/fribidi/fribidi/releases/download/v1.0.10/fribidi-1.0.10.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  expat
  URL https://github.com/libexpat/libexpat/releases/download/R_2_2_10/expat-2.2.10.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static --without-docbook CFLAGS=-fPIC
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  fontconfig
  DEPENDS freetype expat
  URL https://www.freedesktop.org/software/fontconfig/release/fontconfig-2.13.93.tar.xz
# PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/fontconfig-git.patch
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static --disable-docs CFLAGS=-fPIC
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  graphite
  DEPENDS freetype
  URL https://github.com/silnrsi/graphite/releases/download/1.3.14/graphite2-1.3.14.tgz
  CONFIGURE_COMMAND PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF .
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  brotli
# URL http://security.ubuntu.com/ubuntu/pool/main/b/brotli/brotli_1.0.9.orig.tar.gz
  URL https://github.com/google/brotli/archive/v1.0.9.tar.gz
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/brotli-link.patch
  CONFIGURE_COMMAND ./bootstrap COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR}
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  ass
  DEPENDS nasm freetype fribidi fontconfig graphite brotli
  URL https://github.com/libass/libass/releases/download/0.15.0/libass-0.15.0.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  gavl
  URL https://netcologne.dl.sourceforge.net/project/gmerlin/gavl/1.4.0/gavl-1.4.0.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static --without-doxygen CFLAGS=-fPIC
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  cairo
# GIT_REPOSITORY https://github.com/freedesktop/cairo
# URL https://www.cairographics.org/releases/cairo-1.14.12.tar.xz
# URL https://www.cairographics.org/snapshots/cairo-1.15.14.tar.xz
  URL https://www.cairographics.org/releases/cairo-1.16.0.tar.xz
# URL https://www.cairographics.org/snapshots/cairo-1.17.2.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static CFLAGS=-fPIC
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  opencv
# URL https://github.com/opencv/opencv/archive/2.4.13.6.tar.gz
  URL https://github.com/opencv/opencv/archive/3.4.12.tar.gz
# URL https://github.com/opencv/opencv/archive/4.5.0.tar.gz
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF -DBUILD_opencv_world:BOOL=OFF -DBUILD_opencv_java:BOOL=OFF -DBUILD_opencv_java_bindings_generator:BOOL=OFF -DBUILD_opencv_python2:BOOL=OFF -DBUILD_opencv_python3:BOOL=OFF -DBUILD_opencv_python_bindings_generator:BOOL=OFF -DBUILD_ITT:BOOL=OFF -DOPENCV_ENABLE_NONFREE:BOOL=ON ..
  BUILD_COMMAND cd build && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build && PATH=$ENV{PATH} make install && cp -p ${CMAKE_BINARY_DIR}/share/OpenCV/3rdparty/lib/libippiw.a ${CMAKE_BINARY_DIR}/lib/ && cp -p ${CMAKE_BINARY_DIR}/share/OpenCV/3rdparty/lib/libippicv.a ${CMAKE_BINARY_DIR}/lib/
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  frei0r
  DEPENDS gavl cairo opencv
# URL https://files.dyne.org/frei0r/releases/frei0r-plugins-1.7.0.tar.gz
  GIT_REPOSITORY https://github.com/dyne/frei0r.git
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --enable-static
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  bluray
# GIT_REPOSITORY git://git.videolan.org/libbluray.git
  URL https://download.videolan.org/pub/videolan/libbluray/1.2.1/libbluray-1.2.1.tar.bz2
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  flac
  DEPENDS ogg
  URL https://downloads.xiph.org/releases/flac/flac-1.3.3.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  sndfile
  DEPENDS vorbis flac
  URL http://www.mega-nerd.com/libsndfile/files/libsndfile-1.0.28.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static CFLAGS=-I${CMAKE_BINARY_DIR}/include
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  bs2b
  DEPENDS vorbis sndfile
  URL https://netcologne.dl.sourceforge.net/project/bs2b/libbs2b/3.1.0/libbs2b-3.1.0.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared CFLAGS=-I${CMAKE_BINARY_DIR}/include LDFLAGS=-L${CMAKE_BINARY_DIR}/lib LIBS=-lvorbis\ -lvorbisenc\ -logg\ -lFLAC\ -lm
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  caca
  GIT_REPOSITORY https://github.com/cacalabs/libcaca
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND ./bootstrap COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --disable-java --disable-x11 --disable-gl --disable-doc
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  cdio
# URL https://ftp.gnu.org/gnu/libcdio/libcdio-0.94.tar.gz
  URL https://ftp.gnu.org/gnu/libcdio/libcdio-2.1.0.tar.bz2
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  cdio-paranoia
  DEPENDS cdio
# URL https://ftp.gnu.org/gnu/libcdio/libcdio-paranoia-10.2+0.94+2.tar.gz
  URL https://ftp.gnu.org/gnu/libcdio/libcdio-paranoia-10.2+2.0.1.tar.bz2
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared CFLAGS=-I${CMAKE_BINARY_DIR}/include
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  raw1394
  URL https://www.kernel.org/pub/linux/libs/ieee1394/libraw1394-2.1.2.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  dc1394
  DEPENDS raw1394
  URL https://netcologne.dl.sourceforge.net/project/libdc1394/libdc1394-2/2.2.6/libdc1394-2.2.6.tar.gz
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/dc1394-inline.patch
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared CFLAGS=-I${CMAKE_BINARY_DIR}/include LDFLAGS=-L${CMAKE_BINARY_DIR}/lib LIBS=-lpthread\ -lraw1394
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  flite
  URL http://www.festvox.org/flite/packed/flite-2.1/flite-2.1-release.tar.bz2
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --with-audio=none
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  gsm
  URL https://deb.debian.org/debian/pool/main/libg/libgsm/libgsm_1.0.18.orig.tar.gz
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/gsm-install-root.patch
  CONFIGURE_COMMAND ""
  INSTALL_COMMAND PATH=$ENV{PATH} make INSTALL_ROOT=${CMAKE_BINARY_DIR} install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  avc1394
  DEPENDS raw1394
  URL https://netcologne.dl.sourceforge.net/project/libavc1394/libavc1394/libavc1394-0.5.4.tar.gz
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/avc1394-dupl-ref.patch
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  iec61883
  DEPENDS raw1394 avc1394
  URL https://www.kernel.org/pub/linux/libs/ieee1394/libiec61883-1.2.0.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  ilbc
# GIT_REPOSITORY https://github.com/TimothyGu/libilbc.git
  URL https://github.com/TimothyGu/libilbc/releases/download/v2.0.2/libilbc-2.0.2.tar.gz
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  modplug
  GIT_REPOSITORY https://github.com/Konstanty/libmodplug.git
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  openjpeg
  URL https://github.com/uclouvain/openjpeg/archive/v2.3.1.tar.gz
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF ..
  BUILD_COMMAND cd build && make
  INSTALL_COMMAND cd build && make install && cp bin/libopenjp2.a ${CMAKE_BINARY_DIR}/lib
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  shine
  GIT_REPOSITORY https://github.com/savonet/shine.git
# URL https://github.com/toots/shine/releases/download/3.1.1/shine-3.1.1.tar.gz
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND mkdir -p m4 COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  soxr
  URL https://netcologne.dl.sourceforge.net/project/soxr/soxr-0.1.3-Source.tar.xz
  CONFIGURE_COMMAND mkdir -p Release COMMAND cd Release && cmake -DCMAKE_BUILD_TYPE:STRING=Release -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF ..
  BUILD_COMMAND cd Release && make
  INSTALL_COMMAND cd Release && make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  twolame
  DEPENDS sndfile
  URL https://netcologne.dl.sourceforge.net/project/twolame/twolame/0.4.0/twolame-0.4.0.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  v4l2
# URL https://linuxtv.org/downloads/v4l-utils/v4l-utils-1.16.3.tar.bz2
  URL https://linuxtv.org/downloads/v4l-utils/v4l-utils-1.20.0.tar.bz2
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/v4l2-compile.patch
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared LDFLAGS=-static
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  vidstab
  GIT_REPOSITORY https://github.com/georgmartius/vid.stab.git
# URL https://github.com/georgmartius/vid.stab/archive/v1.1.0.tar.gz
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF .
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  vo-amrwbenc
  URL https://netcologne.dl.sourceforge.net/project/opencore-amr/vo-amrwbenc/vo-amrwbenc-0.1.3.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  wavpack
  URL http://www.wavpack.com/wavpack-5.3.0.tar.bz2
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  webp
  GIT_REPOSITORY https://chromium.googlesource.com/webm/libwebp
# URL https://github.com/webmproject/libwebp/archive/v1.0.2.tar.gz
  UPDATE_COMMAND ""
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/webp-tiff.patch
  CONFIGURE_COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-libwebpmux --enable-libwebpdecoder --enable-libwebpextras
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  xavs
  DEPENDS yasm
  SVN_REPOSITORY http://svn.code.sf.net/p/xavs/code/trunk
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR}
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  zmq
# URL https://github.com/zeromq/zeromq4-1/releases/download/v4.1.8/zeromq-4.1.8.tar.gz
  URL https://github.com/zeromq/libzmq/releases/download/v4.3.3/zeromq-4.3.3.tar.gz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared --enable-static LIBS=-lstdc++
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  zvbi
  URL https://netcologne.dl.sourceforge.net/project/zapping/zvbi/0.2.35/zvbi-0.2.35.tar.bz2
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  aom
  GIT_REPOSITORY https://aomedia.googlesource.com/aom
  GIT_TAG v2.0.1
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND mkdir -p aom_build COMMAND cd aom_build && PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF ..
  BUILD_COMMAND cd aom_build && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd aom_build && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  dav1d
  GIT_REPOSITORY https://code.videolan.org/videolan/dav1d
  UPDATE_COMMAND ""
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && PATH=$ENV{PATH} meson --prefix ${CMAKE_BINARY_DIR} --libdir ${CMAKE_BINARY_DIR}/lib --default-library static ..
  BUILD_COMMAND cd build && PATH=$ENV{PATH} ninja
  INSTALL_COMMAND cd build && PATH=$ENV{PATH} ninja install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  davs2
  URL https://github.com/pkuvcl/davs2/archive/1.6.tar.gz
  CONFIGURE_COMMAND cd build/linux && PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --enable-pic
  BUILD_COMMAND cd build/linux && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build/linux && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  xavs2
  URL https://github.com/pkuvcl/xavs2/archive/1.3.tar.gz
  CONFIGURE_COMMAND cd build/linux && PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --enable-pic
  BUILD_COMMAND cd build/linux && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build/linux && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  codec2
  URL https://codeload.github.com/drowe67/codec2/tar.gz/v0.9.2
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/codec2-lsp.patch
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF ..
  BUILD_COMMAND cd build && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  zimg
  URL https://github.com/sekrit-twc/zimg/archive/release-3.0.1.tar.gz
  CONFIGURE_COMMAND ./autogen.sh COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  avisynth
  URL https://github.com/AviSynth/AviSynthPlus/archive/v3.6.1.tar.gz
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF -DHEADERS_ONLY:BOOL=ON ..
  BUILD_COMMAND cd build && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  kvazaar
  URL https://github.com/ultravideo/kvazaar/releases/download/v2.0.0/kvazaar-2.0.0.tar.xz
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  vmaf
  URL https://github.com/Netflix/vmaf/archive/v1.5.3.tar.gz
  CONFIGURE_COMMAND mkdir -p libvmaf/build COMMAND cd libvmaf/build && PATH=$ENV{PATH} meson --prefix ${CMAKE_BINARY_DIR} --libdir ${CMAKE_BINARY_DIR}/lib --default-library static ..
  BUILD_COMMAND cd libvmaf/build && PATH=$ENV{PATH} ninja
  INSTALL_COMMAND cd libvmaf/build && PATH=$ENV{PATH} ninja install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  cunit
  URL https://netcologne.dl.sourceforge.net/project/cunit/CUnit/2.1-3/CUnit-2.1-3.tar.bz2
  CONFIGURE_COMMAND mv configure.in configure.ac COMMAND autoreconf -i COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --disable-shared
  BUILD_COMMAND PATH=$ENV{PATH} make
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  sofa
  DEPENDS cunit
  URL https://github.com/hoene/libmysofa/archive/v1.1.tar.gz
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_SHARED_LIBS:BOOL=OFF -DBUILD_TESTS:BOOL=OFF -DCODE_COVERAGE:BOOL=OFF ..
  BUILD_COMMAND cd build && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  lensfun
  URL https://github.com/lensfun/lensfun/archive/v0.3.95.tar.gz
  CONFIGURE_COMMAND mkdir -p build COMMAND cd build && PATH=$ENV{PATH} cmake -DCMAKE_INSTALL_PREFIX:PATH=${CMAKE_BINARY_DIR} -DBUILD_STATIC:BOOL=ON ..
  BUILD_COMMAND cd build && PATH=$ENV{PATH} make
  INSTALL_COMMAND cd build && PATH=$ENV{PATH} make install
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  ffmpeg
  DEPENDS bluray bzip2 caca cairo cdio expat fdkaac flite fribidi gavl gsm ilbc modplug mp3lame ogg opencore-amr openjpeg openssl opus raw1394 shine soxr twolame v4l2 vidstab vo-amrwbenc wavpack webp xz yasm z zmq zvbi vpx x264 x265 xavs xvidcore flac speex vorbis theora freetype cdio-paranoia avc1394 dc1394 rtmp fontconfig ass frei0r sndfile bs2b iec61883 aom dav1d davs2 xavs2 codec2 zimg avisynth kvazaar vmaf sofa lensfun opencv
  URL https://www.ffmpeg.org/releases/ffmpeg-4.3.1.tar.bz2
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/ffmpeg-ism-offset.patch && patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/ffmpeg-filename-size.patch
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} --datadir=/usr/share/ffmpeg --disable-shared --enable-static --pkg-config-flags=--static --enable-gpl --enable-version3 --enable-nonfree --disable-debug --disable-ffplay --enable-runtime-cpudetect --extra-cflags=-I${CMAKE_BINARY_DIR}/include\ --static --extra-ldflags=-L${CMAKE_BINARY_DIR}/lib\ -static --extra-libs=-lstdc++\ -lexpat\ -lpng\ -lxml2\ -lusb-1.0\ -lraw1394\ -lv4lconvert\ -ludev\ -ljpeg\ -lwebp\ -lwebpmux\ -lfreetype\ -lharfbuzz\ -lgraphite2\ -lncurses\ -lxcb\ -lXau\ -lXdmcp\ -ltinfo\ -lgpm\ -lbluray\ -lopencv_core\ -lzmq\ -lslang\ -licui18n\ -licuuc\ -lippiw\ -lippicv\ -luuid\ -lgomp\ -lrt\ -llzma\ -lpthread\ -lz\ -lm\ -ldl --enable-libxml2 --enable-libopencore-amrnb --enable-libopencore-amrwb --enable-libfdk-aac --enable-libmp3lame --enable-libspeex --enable-libtheora --enable-libvorbis --enable-libx264 --enable-libx265 --enable-libxvid --enable-libvpx --enable-libopus --enable-librtmp --enable-libfreetype --enable-libass --enable-fontconfig --enable-frei0r --enable-libbluray --enable-libbs2b --enable-libcaca --enable-libcdio --enable-libdc1394 --enable-libflite --enable-libgsm --enable-libiec61883 --enable-libilbc --enable-libmodplug --enable-libopenjpeg --enable-libshine --enable-libsoxr --enable-libtwolame --enable-libv4l2 --enable-libvidstab --enable-libvo-amrwbenc --enable-libwavpack --enable-libwebp --enable-libxavs --enable-libzmq --enable-libzvbi --enable-libaom --enable-libdav1d --enable-libdavs2 --enable-libxavs2 --enable-libcodec2 --enable-libzimg --enable-avisynth --enable-libkvazaar --enable-libvmaf --enable-libmysofa --enable-liblensfun --enable-openssl --enable-libopencv
  BUILD_COMMAND PATH=$ENV{PATH} make
  INSTALL_COMMAND PATH=$ENV{PATH} make install COMMAND PATH=$ENV{PATH} make install-data DATADIR=/usr/share/ffmpeg
  BUILD_IN_SOURCE 1
)
EXTERNALPROJECT_ADD(
  frmxtract
  DEPENDS ffmpeg
  URL ${CMAKE_SOURCE_DIR}/vendor/frmxtract-4.2.2.tar.gz
  PATCH_COMMAND patch -N -p1 < ${CMAKE_SOURCE_DIR}/vendor/frmxtract-configure.patch
  CONFIGURE_COMMAND PATH=$ENV{PATH} PKG_CONFIG_PATH=$ENV{PKG_CONFIG_PATH} ./configure --prefix=${CMAKE_BINARY_DIR} CFLAGS=-Wall\ -O2\ -I${CMAKE_BINARY_DIR}/include LDFLAGS=-static\ -L${CMAKE_BINARY_DIR}/lib\ -lavformat\ -lavcodec\ -lavutil\ -lswresample\ -lswscale\ -lvorbis\ -logg\ -lvorbisenc\ -ltheora\ -lvpx\ -lrtmp\ -lzvbi\ -lfdk-aac\ -lsndfile\ -lmp3lame\ -lmodplug\ -lsoxr\ -ltwolame\ -lwavpack\ -lxvidcore\ -lx264\ -lx265\ -lxavs\ -lwebpmux\ -lwebpdecoder\ -lwebp\ -lbluray\ -lopencv_core\ -lopencore-amrwb\ -lopencore-amrnb\ -lvo-amrwbenc\ -lfontconfig\ -lfreetype\ -lharfbuzz\ -lgraphite2\ -lshine\ -lspeex\ -lopus\ -lnuma\ -lbrotlidec\ -lbrotlicommon\ -laom\ -ldavs2\ -lxavs2\ -ldav1d\ -lcodec2\ -lkvazaar\ -lzmq\ -lgcc_eh\ -lunwind\ -lstdc++\ -lexpat\ -lilbc\ -lssl\ -lcrypto\ -lxml2\ -lopenjp2\ -lpng\ -lbz2\ -llzma\ -lslang\ -licui18n\ -licuuc\ -licudata\ -luuid\ -lgomp\ -lpthread\ -lrt\ -lz\ -lm\ -ldl\ -s
  BUILD_COMMAND PATH=$ENV{PATH} LDFLAGS=$ENV{} make
  BUILD_IN_SOURCE 1
)
