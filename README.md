# clang-fdev1
Dockerfile that sets up a basic gcc &amp; clang Debian environment with a number of libraries configured

The Docker Image is listed on Docker Hub:
https://hub.docker.com/r/tafthorne/clang-fdev1/

To pull the image:

 docker pull tafthorne/clang-fdev1

An overview of the included libraries is given below.

## Using This Image
The expected way to use this image is to navigate to the working directory
where your source code resides and start an interactive session.

  docker run -ti --volume="${PWD}:/shared" -w "/shared" tafthorne/clang-fdev1

Then within the running container you can call make, clang or gcc as if it were
a native tool.  The libraries added to this image will be in the global include
path.

## Clang

Clang is a C based language front-end for C, C++, Objective C/C++ and others
for the LLVM compiler.
* http://clang.llvm.org/
* http://www.llvm.org/

## GNU GCC

The GNU Compiler Collection is a compiling system that supports several
languages.  This project focuses more on the C and C++ usage.

## spdlog

spdlog is a fast, header only C++ logging library.  For further details please
see their project page.
* https://github.com/gabime/spdlog

## Contributing

Please see the notes in CONTRIBUTING.md.

