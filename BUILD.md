Build on CentOS 6.5 (vanilla install with all updates):

1. Install some prerequisites (hg, static libs, ...)
   $ ./centos-prereq

2. Compile latest version of CMake
   $ wget http://www.cmake.org/files/v3.0/cmake-3.0.2.tar.gz
   $ tar -zxvf cmake-3.0.2.tar.gz
   $ cd cmake-3.0.2
   $ ./bootstrap
   Edit CMakeCache.txt:
   CMAKE_USE_OPENSSL:BOOL=OFF --> ON
   ENABLE_OPENSSL:INTERNAL=OFF --> ON
   $ make install
   $ cd ..

3. Compile ffmpeg
   $ make

4. Package ffmpeg
