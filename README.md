# whichlib
Which but for library.

## Requirements
- `awk`

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

- `whichlib [regex]` will print libraries from which the name matches the regex.

```
$ ./whichlib libc.so
/lib/libc.so.6
/lib64/libc.so.6

$ ./whichlib lib.*le\.so$
/lib/libpcprofile.so
/lib64/libpcprofile.so
```

# whichinclude
Which but for header file

## Requirements
- `g++`

## Usage

- `whichinclude [header.file]`

## Example
```
$ ./whichinclude omp.h
/usr/lib/gcc/x86_64-redhat-linux/4.8.5/include/omp.h
```
