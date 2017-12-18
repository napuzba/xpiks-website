---
layout: post
title: "How to build xpiks for your platform"
date: 2014-12-28T09:54:01+02:00
---

# Build instructions:

### 1. Environment:

- download Qt 5.2 or higher for your platform from <a href="http://qt.io/">official website</a>
- while installing, add Qt bin directory to your PATH (Environmental variables)
- download latest Git client for your desktop
- make sure you also have Git bin directory in your PATH

### 2. Obtaining source code:

- check out Xpiks repository with Git `git clone https://github.com/Ribtoks/xpiks.git` (or use git path of your Fork)
- check out submodules `git submodules init` and `git submodules update --recursive`
- rename `src/tiny-AES/aes.c` to `src/tiny-AES/aes.cpp`

### 3. Building the dependencies:

- <span class="gray">[Windows]</span> if you're building for Windows, build Zlib first (<a href="#zlib">see instructions below</a>)
- build <a href="#hunspell">Hunspell</a> and <a href="#quazip">Quazip</a> libraries (instructions below)
- <span class="gray">[Windows]</span> if you're building for Windows, build mman32 library before ssdll and libface (<a href="#mman32">see instructions below</a>)     
- build <a href="#libface">cpp-libface</a> library (instructions below)
- build <a href="#ssdll">ssdll</a> library (instructions below)
- <span class="gray">[Windows]</span> build <a href="#libcurl">libcurl</a> library (instructions below)
- build <a href="#exiv2">Exiv2</a> library (instructions below)

### 4. Building main application:

- open `src/xpiks-qt/xpiks-qt.pro` file with Qt Creator installed with Qt
- select build target [Debug/Release], press "Run qmake" and then "Build"
- [Windows] you might need to create `translations\` and `ac_sources\` directories in the build directory
- now you can use xpiks-qt on your computer

&nbsp;

&nbsp;

&nbsp;

# Instructions to build dependencies:

***<span id="zlib">To build <u>zlib</u> under Windows for Xpiks, do the following:</span>***

- download zlib (1.2.11) source code and extract to `scr/zlib-1.2.11`
- open `src/zlib-project/zlib.pro` in Qt Creator, select `Release`, execute `Run qmake`, execute `Build`
- copy built library `.lib` (and z.pdb if you builded for Debug) to `src/libs` directory

***<span id="hunspell">To build <u>Hunspell</u> do the following:</span>***

- download **Hunspell 1.6.0** from http://hunspell.sourceforge.net/ and extract it in the `src/` directory
- open project `src/hunspell/hunspell.pro` in Qt Creator, select `Release`, execute `Run qmake`, execute `Build`
- copy built library (e.g. `libhunspell.a`, `hunspell.lib`) from the build directory to the `src/libs` directory

***<span id="quazip">To build <u>Quazip</u> do the following:</span>***

- open project `src/quazip/quazip/quazip.pro` in Qt Creator, select `Release`, execute `Run qmake`, execute `Build`
- copy built library (e.g. `libquazip.a`, `quazip.lib`) from the build directory to the `src/libs` directory

***<span id="mman32">To build <u>mman32</u> under Windows for Xpiks, do the following:</span>***

- locate `mman-win32` directory in one of the subdirectories either of `ssdll` or `cpp-libface` submodules of Xpiks
- open `src/mman-win32/mman-win32.pro` in Qt Creator, select `Release`, execute `Run qmake`, execute `Build`
- copy built library `.lib` and `.dll` (and mman.pdb if you builded for Debug) to `src/libs` directory

***<span id="libface">To build <u>libface</u> do the following:</span>***

- open file `src/cpp-libface/README.md` and follow instructions for your platform
- copy built library (e.g. `libface.a`, `face.dll`) from the build directory to the `src/libs` directory
- for Windows you will also need mman32 library (`mman.lib`) to be in the `src/libs` directory

***<span id="ssdll">To build <u>ssdll</u> do the following:</span>***

- open file `src/ssdll/README.md` and follow instructions for your platform
- copy built library (e.g. `ssdll.so`, `ssdll.dll`) from the build directory to the `src/libs` directory
- for Windows you will also need mman32 library (`mman.dll`) to be in the `src/libs` directory

***<span id="libcurl">To build <u>LibCurl</u> do the following:</span>***

- open git bash and type `git clone https://github.com/blackrosezy/build-libcurl-windows.git`
- execute `build.bat` and after if finishes, copy contents of `lib/dll-debug-x64` to the `src/libs/` directory

***<span id="exiv2">To build <u>Exiv2</u> do the following:</span>***

**Visual Studio 2015 Build:**

- download **exiv2 v0.25** library from <a href="http://www.exiv2.org/" target="_blanc">official website</a> and extract it somewhere
- download **expat-2.1.1** library from <a href="https://sourceforge.net/projects/expat/">official website</a> and extract it on same level as exiv2
- rename directory `expat-2.1.1/` to `expat/`
- open `msvc2005/exiv2.sln` and upgrade all projects
- from each project remove file `localtime.c`
- open file `include/exiv2/exv_msvs.h` and enable unicode support, disable png, curl and ssh (alternatively, you can overwrite this file with the one in the _Xpiks_ repository via path `src/exiv2-0.25/include/exiv2/exv_msvs.h`)
- in Visual Studio select `"Build" -> "Batch build"` and mark all _DebugDLL_ and _ReleaseDLL_ builds for your platform (x64 or x86)
- press "Build"
- copy build artifacts (`libexiv2.dll`, `libexiv2.lib`, `libexpat.dll`, `libexpat.lib`) to `src/libs` directory in _Xpiks_ repository

**OS X Build:**

- open Terminal in the directory of exiv2 sources and do the following
- `mkdir build-Debug && cd build-Debug`
- `/Applications/CMake.app/Contents/bin/cmake .. -DEXIV2_ENABLE_SHARED=off -DCMAKE_BUILD_TYPE=Debug -DCMAKE_OSX_DEPLOYMENT_TARGET=10.7 -DCMAKE_CXX_STANDARD=11`
- `make`

&nbsp;

&nbsp;

&nbsp;

# Redistribution

If you builded for Release and you wish to redistribute it for similar desktop platforms to yours, follow next steps:

- after build is successful, navigate to build directory, open it in terminal
- find macdeployqt, windeployqt or any similar tool in Qt bin directory
- read help of *deployqt tool and execute it with necessary parameters to include qt frameworks which are needed for build as well as QML directories

Sample macdeployqt command for OS X can be found below: (depends on your build-* directory path)

`macdeployqt xpiks-qt.app -verbose=2 -dmg -executable=xpiks-qt.app/Contents/MacOS/xpiks-qt -qmldir=../ -qmldir=../Components/ -qmldir=../Constants/ -qmldir=../Dialogs/ -qmldir=../StyledControls/ -qmldir=../StackViews/ -qmldir=../CollapserTabs/`

And for Windows as well:

`windeployqt.exe --qmldir=../../xpiks-qt/Components/ --qmldir=../../xpiks-qt/Constants/ --qmldir=../../xpiks-qt/Dialogs/ --qmldir=../../xpiks-qt/StyledControls/ --qmldir=../../xpiks-qt/CollapserTabs/ --qmldir=../../xpiks-qt/StackViews/ --release xpiks-qt.exe`

Xpiks uses English dictionaries from [Libreoffice collection](http://cgit.freedesktop.org/libreoffice/dictionaries/tree/). In Windows they are stored in the `dict/` subdirectory, in OS X they are in the `Resources/` directory of a bundle. As of Xpiks 1.1 these files are copied automatically.
