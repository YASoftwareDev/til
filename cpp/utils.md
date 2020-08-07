## strip - Discard symbols from object files.

## whereis - locate the binary, source, and manual page files for a command

## ldconfig - configure dynamic linker run-time bindings
  -p, --print-cache
         Print the lists of directories and candidate libraries stored in the current cache.
example:
```
/sbin/ldconfig -p | rg libnvinfer
```

## dpkg - package manager for Debian
  -l
    List packages matching given pattern

##
If you'd like to delete (purge) the package completely (with configuration files), you'll have to run:

dpkg -P urserver

https://unix.stackexchange.com/a/236843/223835

## strace - trace system calls and signals (ultimate tool!)

strace -e file app.elf - get 

## ldd - print shared object dependencies

## how to find out the dynamic libraries executables loads when run

this link is a good summary of possible methods :)

https://unix.stackexchange.com/questions/120015/how-to-find-out-the-dynamic-libraries-executables-loads-when-run

## google/bloaty

https://github.com/google/bloaty - Bloaty McBloatface: a size profiler for binaries

## oneliners

```
file a.out
a.out: ELF 64-bit LSB shared object, x86-64, version 1 (GNU/Linux), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=847c736367efd9cd353e8a0790a24ad58ce86d70, with debug_info, not stripped

strings a.out | rg GNU
GNU C++14 7.5.0 -mtune=generic -march=x86-64 -g -std=gnu++14 -fstack-protector-strong
GNU C++14 7.5.0 -mtune=generic -march=x86-64 -g -std=gnu++14 -fPIC -fstack-protector-strong
GNU C17 9.2.1 20191102 -mtune=generic -march=x86-64 -g -O2 -fvisibility=hidden -fno-common -fno-strict-aliasing -fasynchronous-unwind-tables -fstack-protector-strong
GNU C11 9.2.1 20191102 -msse -msse2 -mtune=generic -march=x86-64 -g -O3 -O3 -std=c11 -fomit-frame-pointer -fPIC -fno-math-errno -fno-signed-zeros -fno-tree-vectorize -fasynchronous-unwind-tables -fstack-protector-strong
GNU C++11 9.2.1 20191102 -mtune=generic -march=x86-64 -g -O2 -std=c++11 -fPIC -fasynchronous-unwind-tables -fstack-protector-strong
GNU C++11 9.2.1 20191102 -mtune=generic -march=x86-64 -g -O2 -std=c++11 -fPIC -fno-rtti -fno-exceptions -fasynchronous-unwind-tables -fstack-protector-strong
GNU C99 9.2.1 20191102 -mtune=generic -march=x86-64 -g -g -O2 -std=c99 -fPIC -fasynchronous-unwind-tables -fstack-protector-strong
GNU C99 9.2.1 20191102 -mtune=generic -march=x86-64 -g -g -g -O2 -std=c99 -fPIC -fvisibility=hidden -fasynchronous-unwind-tables -fstack-protector-strong
GNU C++11 9.2.1 20191102 -mtune=generic -march=x86-64 -g -g -O2 -O2 -std=c++11 -fPIC -fasynchronous-unwind-tables -fstack-protector-strong
__GNU_EH_FRAME_HDR
```
