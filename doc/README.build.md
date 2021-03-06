Obtaining the software
======================

Clone
---------------
The authoritative location of the software is the following git
repository:
   <http://mpegx.int-evry.fr/software/MPEG/PCC/mpeg-pcc-dmetric>

Each released version may be identified by a version control system tag in
the form `release-v0.13.3`.

An example:

```console
$ git clone http://mpegx.int-evry.fr/software/MPEG/PCC/mpeg-pcc-dmetric.git
$ cd mpeg-pcc-dmetric
```

> It is strongly advised to obtain the software using the version control
> system rather than to download a zip (or other archive) of a particular
> release.  The build system uses the version control system to accurately
> identify the version being built.

Building
------- 

The codec is supported on Linux, OSX and Windows platforms.  The build
configuration is managed using CMake.

> It is strongly advised to build the software in a separate build directory.

### Scripts

Bash scripts can be use to build mpeg-pcc-dmetric project: build.sh to build solutions and
clear.sh to clean.
 
### Linux

```console
  mkdir build
  cd build
  cmake ..
  make
  ../test/pc_error --help
```

### OSX

```console
  mkdir build
  cd build
  cmake .. -G Xcode
  xcodebuild
  ../test/pc_error --help
```

As an alternative, the generated XCode project may be opened and built from
XCode itself.

### Windows

```console
  md build
  cd build
  cmake .. -G "Visual Studio 15 2017 Win64"
```

Open the generated visual studio solution to build it.
