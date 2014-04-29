MAA - Low Level Skeleton Library for Communication on Intel platforms
==============

Library in C/C++ to interface with Galileo & other Intel platforms over:

- I2C
- SPI
- GPIO
- PWM
- AIO

In a structured and sane API with port nanmes/numbering that match boards &
with bindings to javascript & python.

The intent is to make it easier for developers and sensor manufacturers to map
their sensors & actuators on top of supported hardware and to allow control of
low level communication protocol by high level languages & constructs.

=== ENV RECOMENDATIONS ===
--------------

node.js 0.10.26
python 3.3.x or 2.7.x
swig-v8 3.0.1 (if you want node.js to work you need to use swig-v8)
I'm using f31c1dce7a45c4b8ed7e6ff845f4c74539e056f1 from
http://github.com:oliver----/swig-v8

=== COMPILING ===
--------------

NOTE: The only supported cmake build configuration is to have the build/ dir
inside of the repo/tarball.

if swig-v8 is not in your default path you can try run cmake with
"-DCMAKE_PREFIX_PATH="/path/to/swig-v8"

mkdir build/
cmake ..
make

Install is currently unsuported. Javascript and python modules will be in
build/src/{javascript, python}

=== DEVELOPMENT ===
--------------

Unit tests for all features must be completed prior to implementations, please
run `ctest -V` from the build dir in order to see current implementation status

=== USING ===
--------------

see examples/

for node.js make sure that maajs.node is in the current dir and set export
NODE_PATH=.

python2/3 should both work, although testing is done on python3 exclusively.
Node.js bindings may be dodgy, I'm so far unclear of how good swig-v8 is.