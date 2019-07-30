# whichlib
Which but for library.

## Requirements
- `gawk`

## Usage

`whichlib [regex]`


- `whichlib` will print all the shared libraries in your path (including the one in`LD_LIBRARY_PATH`). 

```
$ echo $LD_LIBRARY_PATH
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64
$ ./whichlib
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libubsan.so.1
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/libgcc_s.so.1
/soft/compilers/gcc/8.2.0/linux-rhel7-x86_64/lib64/liblsan.so.0
[...]
/lib64/libstdc++.so.6
/lib64/libgcc_s.so.1
/lib64/libpcprofile.so
```

- `whichlib regex` will print libraries from which the name matches the regex.

```
$ ./whichlib libc.so
/lib/libc.so.6
/lib64/libc.so.6
```
