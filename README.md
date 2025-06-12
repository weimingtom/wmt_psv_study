# wmt_psv_study
My PSVita study

## vitasdk
* https://vitasdk.org  
https://github.com/vitasdk/autobuilds/releases/download/master-linux-v2.534/vitasdk-x86_64-linux-gnu-2025-06-10_18-45-54.tar.bz2  
https://github.com/vitasdk/autobuilds/releases/download/master-linux-v1109/vitasdk-x86_64-linux-gnu-2020-06-06_16-44-59.tar.bz2  
```
$ sudo apt install make git-core cmake python
$ gedit ~/.bashrc
export VITASDK=/home/wmt/vitasdk
export PATH=$VITASDK/bin:$PATH

$ git clone https://github.com/vitasdk/vdpm
$ cd vdpm
$ source ~/.bashrc
$ ./bootstrap-vitasdk.sh 
==> Installing vitasdk to /home/wmt/vitasdk
curl missing (install using: apt install curl)
$ sudo apt install curl
$ ./bootstrap-vitasdk.sh
https://github.com/vitasdk/autobuilds/releases/download/master-linux-v2.534/vitasdk-x86_64-linux-gnu-2025-06-10_18-45-54.tar.bz2
Please add the following to the bottom of your .bashrc:
export VITASDK=/home/wmt/vitasdk
export PATH=$VITASDK/bin:$PATH
and then restart your terminal
$ arm-vita-eabi-gcc -v
arm-vita-eabi-gcc: /lib/x86_64-linux-gnu/libc.so.6: version `GLIBC_2.32' not found (required by arm-vita-eabi-gcc)
arm-vita-eabi-gcc: /lib/x86_64-linux-gnu/libc.so.6: version `GLIBC_2.33' not found (required by arm-vita-eabi-gcc)
arm-vita-eabi-gcc: /lib/x86_64-linux-gnu/libc.so.6: version `GLIBC_2.34' not found (required by arm-vita-eabi-gcc)
(not support xubuntu 20.04)

(for xubuntu 20.04)
$ wget https://github.com/vitasdk/autobuilds/releases/download/master-linux-v1109/vitasdk-x86_64-linux-gnu-2020-06-06_16-44-59.tar.bz2
$ rm -rf vitasdk
$ tar xf vitasdk-x86_64-linux-gnu-2020-06-06_16-44-59.tar.bz2 
$ arm-vita-eabi-gcc -v
Using built-in specs.
COLLECT_GCC=arm-vita-eabi-gcc
COLLECT_LTO_WRAPPER=/home/wmt/vitasdk/bin/../lib/gcc/arm-vita-eabi/9.1.0/lto-wrapper
Target: arm-vita-eabi
Configured with: /home/travis/build/vitasdk/autobuilds/buildscripts/build/gcc-final-prefix/src/gcc-final/configure --build=x86_64-linux-gnu --host=x86_64-linux-gnu --target=arm-vita-eabi --prefix=/home/travis/build/vitasdk/autobuilds/buildscripts/build/vitasdk --libdir=/home/travis/build/vitasdk/autobuilds/buildscripts/build/vitasdk/lib --libexecdir=/home/travis/build/vitasdk/autobuilds/buildscripts/build/vitasdk/lib --with-sysroot=/home/travis/build/vitasdk/autobuilds/buildscripts/build/vitasdk/arm-vita-eabi --with-gmp=/home/travis/build/vitasdk/autobuilds/buildscripts/build/deps_build --with-mpfr=/home/travis/build/vitasdk/autobuilds/buildscripts/build/deps_build --with-mpc=/home/travis/build/vitasdk/autobuilds/buildscripts/build/deps_build --with-isl=/home/travis/build/vitasdk/autobuilds/buildscripts/build/deps_build --with-libelf=/home/travis/build/vitasdk/autobuilds/buildscripts/build/deps_build --with-python-dir=share/gcc-arm-vita-eabi --enable-languages=c,c++ --disable-decimal-float --disable-libffi --disable-libgomp --disable-libmudflap --disable-libquadmath --disable-libssp --disable-libstdcxx-pch --disable-nls --disable-shared --disable-tls --with-gnu-as --with-gnu-ld --with-newlib --disable-multilib --with-arch=armv7-a --with-tune=cortex-a9 --with-fpu=neon --with-float=hard --with-mode=thumb --with-pkgversion='GNU Tools for ARM Embedded Processors' --with-host-libstdcxx='-static-libgcc -Wl,-Bstatic,-lstdc++,-Bdynamic -lm' --with-headers=yes --enable-threads=posix CFLAGS=-DNO_IMPLICIT_EXTERN_C CXXFLAGS=-DNO_IMPLICIT_EXTERN_C
Thread model: posix
gcc version 9.1.0 (GNU Tools for ARM Embedded Processors) 

$ cd
$ git clone https://github.com/vitasdk/samples
$ cd samples
$ cd hello_world/
$ cmake .
(need to overwrite Makefile)
$ make
$ ls
build                CMakeLists.txt        hello_world.velf           Makefile
CMakeCache.txt       hello_world           hello_world.vpk            out
CMakeFiles           hello_world.self      hello_world.vpk.out        sce_sys
cmake_install.cmake  hello_world.self.out  hello_world.vpk_param.sfo  src
(install hello_world.vpk)
```
