# whichlib
Which but for library.


## Usage

`whichlib` will print all the library in your path (including the one  in`LD_LIBRARY_PATH`). 

```
$ ./whichlib | head
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libubsan.so.1
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libgcc_s.so.1
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/liblsan.so.0
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libatomic.so.1
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libmpxwrappers.so.2
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libssp.so.0
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libgomp.so.1
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libquadmath.so.0
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libstdc++.so.6
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libitm.so.1
```

`whichlib regex` will print the library from which the name matches the regex.

```
$ ./whichlib libc.so
/lib/libc.so.6
/lib64/libc.so.6
```
