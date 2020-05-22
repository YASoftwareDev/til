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

## how to find out the dynamic libraries executables loads when run

this link is a good summary of possible methods :)

https://unix.stackexchange.com/questions/120015/how-to-find-out-the-dynamic-libraries-executables-loads-when-run

## google/bloaty

https://github.com/google/bloaty - Bloaty McBloatface: a size profiler for binaries

