---
title: Platform Specifications
category: info
tags: build
---
<head>
<link rel="stylesheet" href="stylesheets/styles.css">
<link rel="stylesheet" href="stylesheets/github-dark.css">
<link rel="shortcut icon" href="images/favicon.ico"/>
</head>
<div class="wrapper">
<header>
<h1>Shapeworks Studio Pages</h1>
<p>Web pages for Shapeworks Studio</p>
<p class="view"><a href="https://github.com/SCIInstitute/ShapeworksStudio">View the Project on GitHub <small>SCIInstitute/ShapeworksStudio</small></a></p>
<ul>
<!-- <li><a href="https://github.com/SCIInstitute/seg3d.pages/zipball/master">Download <strong>ZIP File</strong></a></li> -->
<!-- <li><a href="https://github.com/SCIInstitute/seg3d.pages/tarball/master">Download <strong>TAR Ball</strong></a></li> -->
<li><a href="https://github.com/SCIInstitute/ShapeworksStudio">View On <strong>GitHub</strong></a></li>
</ul>
<img src="https://sciinstitute.github.io/shapeworks.pages/images/splash.bmp" align="center" hspace="0">
</header>
<section>
<h2>Specifications</h2>

<h4>Minimum recommended system configuration for usage:</h4>
<ul>
	<li>Windows 7+, OSX 10.9+, and OpenSuse 13.1+ Recommended. Other platforms may work, but are not officially supported. </li>
	<li>CPU: Core Duo or higher, recommended i5 or i7</li>
	<li>Memory: 4Gb, recommended 8Gb or more</li>
	<li>Graphics Memory: minimum 128MB, recommended 256MB or more</li>
</ul>
<h3>Build from source</h3>
ShapeworksStudio can be <a href="build.html">compiled</a> from source on Linux platforms (OpenSuSE, Ubuntu etc.), OSX, and Windows. It requires at least the following:
<ul>
	<li>C++11 64-bit compatible compiler</li>
	<li>Git 1.8 or higher <a href="https://git-scm.com/">(https://git-scm.com/)</a></li>
	<li>CMake 2.8+ <a href="http://www.cmake.org/">(http://www.cmake.org/)</a></li>
	<li>Visualization ToolKit (VTK 7.* recommended) <a href="http://www.vtk.org/">(http://www.vtk.org/)</a></li>
	<li>Insight Toolkit (ITK 4.7+ recommended) <a href="http://www.itk.org/">(http://www.itk.org/)</a></li>
	<li>Qt 5.* <a href="http://www.qt.io/developers/">(http://www.qt.io/developers/)</a></li>
	<li>NVIDIA card and drivers for Linux</li>
	<li>Graphics cards must support OpenGL 2.0 or greater (not available on older Intel embedded graphics cards).</li>
</ul>
Consult the distribution-specific section for additional package information and the developer documentation for build instructions.
<br/><br/>
<h4>Windows</h4>
The current source code must be compiled with the 64-bit version of Visual Studio 2015.
<br/><br/>
<h4>Mac OS X</h4>
The source code base was built with Xcode as well as GNU Make and works for both environments on OS X 10.9+.
<br/><br/>
<h4>Linux specifications</h4>
The code base has been tested for use with GCC, and this is the recommended compiler for linux. Compiler must support C++11.
<br/><br/>
<h4>OpenSuSE</h4>
We are currently testing on 64-bit Leap 42.1 (OpenSuSE package repository information).
<br/>
OpenSuSE RPMs:
<ul>
	<li>gcc</li>
	<li>gcc-c++</li>
	<li>Make</li>
	<li>CMake</li>
	<li>git</li>
	<li>glu-devel</li>
	<li>libXmu-devel</li>
	<li>CMake-gui</li>
	<li>CMake</li>
</ul>
</section>
</div>
<footer>
<p>Project maintained by <a href="https://github.com/SCIInstitute">SCIInstitute</a></p>
<p>Hosted on GitHub Pages &mdash; Theme by <a href="https://github.com/orderedlist">orderedlist</a></p>
</footer>
