---
title: Build
category: info
tags: build
---

Table of Contents
=================

* [Installing ShapeworksStudio from source](#installing-shapeworks-studio-from-source)
* [Dependencies](#dependencies)
* [Qt](#qt)
* [Windows](#windows)
* [Max OS X](#mac-os-x)
* [Linux](#linux)
* [ITK](#itk)
* [VTK](#vtk)
* [Compiling Shapeworks Studio](#compiling-shapeworks-studio)
* [Mac OS X](#mac-os-x)
* [Linux](#linux)
* [Compiling ShapeworksStudio](#compiling-shapeworks-studio)
* [Compiling ITK](#compiling-itk)
* [Compiling VTK](#compiling-vtk)
* [Compiling ShapeworksStudio](#compiling-shapeworks-studio-1)
* [Unix and OSX](#unix-and-osx)
* [Windows](#windows-1)
* [All Platforms](#all-platforms)
* [ShapeworksStudio Support](#shapeworks-studio-support)

<!-- Created by [gh-md-toc](https://github.com/ekalinin/github-markdown-toc) -->

# Installing Shapeworks Studio from source

## Dependencies

### Qt

#### Windows

A Visual Studio binary build is available.
To our knowledge the Windows Visual Studio development libraries are only available in a 32-bit version.
A 64-bit version can be built from the source code download, configuring it as described on the Qt webpage.

#### Mac OS X

Qt binaries are available on the Qt website or can be built from source code.
Clang with C++11 support is required.

#### Linux

Qt is available from most package managers. Look for Qt 5+.

### CMake

[CMake](https://cmake.org/) versions 2.8 - 3.4 are supported.

### VTK

Visualization ToolKit (VTK 7. recommended) (http://www.vtk.org/)

### ITK

Insight Toolkit (ITK 4.7+ recommended) (http://www.itk.org/)


## Compiling Shapeworks Studio

Once you have obtained a compatible compiler and installed Qt on your system, you need to
download and install CMake (http://www.cmake.org) to actually build the software.
CMake is a platform independent configuring system that is used for generating Makefiles,Visual Studio project files, or Xcode project files.

### Compiling ITK

Configure with:
```
CMAKE_CXX_FLAGS+="-std=c++11"
BUILD_SHARED_LIBS=FALSE
BUILD_EXAMPLES=FALSE
BUILD_TESTING=FALSE
ITKV3_COMPATIBILTY=TRUE
```
Then build ITK.
```
make -j12 all
```
You may need to use the CMake GUI in Windows. It is best to configure with "NMake Makefiles". Once you have configured and generated, you can build in a command prompt.
```
cd C:\ITK_DIR
mkdir build
cd build
nmake all
```

###Compiling VTK

Configure with:
```
VTK_Group_Qt=ON
VTK_QT_VERSION=5
Qt5_DIR="/PATH/TO/YOUR/Qt5"
BUILD_SHARED_LIBS=FALSE
BUILD_EXAMPLES=FALSE
BUILD_TESTING=FALSE
```
Then build ITK.
```
make -j12 all
```
You may need to use the CMake GUI in Windows. It is best to configure with "NMake Makefiles". Once you have configured and generated, you can build in a command prompt.
```
cd C:\VTK_DIR
mkdir build
cd build
nmake all
```

### Compiling Shapeworks Studio
Once CMake, Qt, ITK, and VTK have been installed and/or built, run CMake from your build directory and give a path to the ShapeworksStudio directory containing the master CMakeLists.txt file.

#### Unix and OSX
```     
mkdir ShapeWorksStudio/build
cd ShapeWorksStudio/build
cmake -DVTK_DIR=Path/To/Your/VTK/build -DITK_DIR=Path/To/Your/ITK/build -DQT_DIR=Path/To/Your/Qt5/build -DCMAKE_BUILD_TYPE=Release ../src
make
```
Depending on how you obtained Qt, you may need to specify other Qt directories:
```
-DQT5WidgetsDIR="Path/To/Qt/5.6/gcc/lib/cmake/Qt5Widgets"
-DQT5OpenGLDIR="Path/To/Qt/5.6/gcc/lib/cmake/Qt5OpenGL"
```
#### Windows
Open a Visual Studio 64 bit Native Tools Command Prompt. 
Follow these commands:
```
mkdir C:\Path\To\ShapeWorksStudio\build
cd C:\Path\To\ShapeWorksStudio\build
cmake -G "NMake Makefiles" -DVTK_DIR="C:/Path/To/Your/VTK/build" -DITK_DIR="C:/Path/To/Your/ITK/build" -DQT_DIR="C:/Path/To/Your/Qt5/build" -DCMAKE_BUILD_TYPE=Release ../src
nmake
```
**NOTE** Be sure to copy the Qt5 DLL files to the Executable directory for the program to run.
```
C:\Qt5_DIR\msvc2015\5.6\bin\Qt5Widgets.dll
C:\Qt5_DIR\msvc2015\5.6\bin\Qt5Core.dll
C:\Qt5_DIR\msvc2015\5.6\bin\Qt5OpenGL.dll
C:\Qt5_DIR\msvc2015\5.6\bin\Qt5Gui.dll
```
#### All Platforms
Your paths may differ slightly based on your Qt5, ITK, and VTK versions and where they are installed/built.

The console version ``ccmake``, or GUI version can also be used.
You may be prompted to specify your location of the Qt installation.
If you installed Qt in the default location, it should find Qt automatically.
After configuration is done, generate the make files or project files for your favorite
development environment and build.

The ShapeworksStudio application will be built in bin/Application.

# Shapeworks Studio Support

For questions and issues regarding building the software from source,
    please email our support list: [shapeworks@sci.utah.edu](mailto:shapeworks@sci.utah.edu)
