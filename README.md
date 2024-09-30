# mimalloc-testing
## What is mimalloc?
This is code for testing mimalloc.  
A very small code, an allocator for memory management with excellent performance.  
  
it has also been implemented in Rust. i tested it io integrate it into the software.  
  
## install mimalloc
```
git clone https://github.com/microsoft/mimalloc
cd mimalloc/
mkdir -p build
cd build/
cmake ..
make
sudo make install
```
  
## Compile with GCC
Now, let's compile using GCC.
```
git clone https://github.com/haturatu/mimalloc-testing.git
cd mimalloc-testing
gcc main.c -o example -lmimalloc
./example
```
or static link
```
$ find /usr/local -name "libmimalloc.a"
/usr/local/lib/mimalloc-1.8/libmimalloc.a
```
Okay, i found it.
```
gcc main.c -o example -static -L/usr/local/lib/mimalloc-1.8/ -lmimalloc
./example
```
Done!
