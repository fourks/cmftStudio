[cmft](https://github.com/dariomanesku/cmft)Studio - cubemap filtering tool
========================================================================================

GUI counterpart of [cmft](https://github.com/dariomanesku/cmft) - cross-platform open-source cubemap filtering tool.

It reaches very fast processing speeds by utilizing both multi-core CPU and OpenCL GPU at the same time!

Download
--------

 * [cmftStudio - Windows 64bit](https://github.com/dariomanesku/cmftStudio-bin/raw/master/cmftStudio_win64.zip)<br />
 * [cmftStudio - Linux 64bit](https://github.com/dariomanesku/cmftStudio-bin/raw/master/cmftStudio_lin64.zip)<br />
 * [cmftStudio - OSX 64bit](https://github.com/dariomanesku/cmftStudio-bin/raw/master/cmftStudio_osx64.zip)<br />
 * *In case you need 32bit binaries, compile from source.*<br />
 <br />
 * [cmftStudio - Sample project 0](https://www.dropbox.com/s/qoy4h6bbp0bcdh4/SampleProject0.csp?dl=1)<br />
 * [cmftStudio - Sample project 1](https://www.dropbox.com/s/ojzyufs4ooh76g5/SampleProject1.csp?dl=1)<br />
 <br />

![cmftStudioCover](https://github.com/dariomanesku/cmftStudio/raw/master/res/cmftStudio_cover.jpg)

Known issues !
--------

### Windows

- There seem to be some rendering problems when using OpenGL backend with a Radeon GPU. For now, on Windows, use DirectX9 or DirectX11 rendering backends until the problem gets fixed. More details [here](https://twitter.com/dariomanesku/status/571303845478985728).<br \>

### Linux

- Window resize and maximize do not work properly! If you use them the application might crash or not display correctly. Avoid doing that until the issue gets fixed.<br \>

### OSX

- Application may display garbage in the first frame upon start. This does not affect usability, just looks ugly.<br \>


Installing
--------

- Windows: No installation available. Put the cmftStudio.exe along with cmftStudio.conf in a desired folder and use it from there
- Linux: Use 'make install' and 'make uninstall'. This will create /usr/local/bin/cmftStudio and a desktop shortcut.


Building
--------

	git clone http://github.com/dariomanesku/cmftStudio.git
	git clone http://github.com/dariomanesku/cmft.git
	git clone http://github.com/dariomanesku/dm.git
	git clone http://github.com/dariomanesku/bgfx.git
	git clone http://github.com/dariomanesku/bx.git
	cd cmftStudio
	make

- After calling `make`, *\_projects* folder will be created with all supported project files. Deleting *\_projects* folder is safe at any time.<br \>
- All compiler generated files will be in *\_build* folder. Again, deleting *\_build* folder is safe at any time.<br \>

### Windows

- Visual Studio solutions can be found in *\_projects/vs20XX/*.<br \>

### Linux

- From 'cmftStudio' directory call 'make linux-debug64' to build the application. Application should be run from the 'runtime' directory where the config file is.
	cd runtime
	./../_build/linux64_gcc/bin/cmftStudioDebug
- Application can be installed or removed from the system by calling 'make linux-install' and 'make linux-uninstall'.

### OS X

- XCode
  - XCode solution can be found in *\_projects/xcode4/*.<br \>
  - XCode project contains one scheme with 4 build configurations (debug/release 32/64bit). Select desired build configuration manually and/or setup schemes manually as desired. In case you need 64bit build, it is possible to just set *Build Settings -> Architectures -> Standard Architectures (64-bit Intel) (x86_64).*<br \>
  - Also it is probably necessary to manually set runtime directory (it is not picking it from genie for some reason). This is done by going to "*Product -> Scheme -> Edit Scheme... -> Run cmftDebug -> Options -> Working Directory (Use custom working directory)*" and specifying *runtime/* directory from cmft root folder.<br \>
- Makefile
  - Makefile can be found in *\_projects/gmake-osx/*.<br \>
  - Project can be build from the root directory by running `make osx-release64` (or similar).<br \>
  <br \>


Screenshot
------------

![cmftStudioAplha1](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_alpha1.jpg)
![cmftStudioSpheres0](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_spheres0.jpg)
![cmftStudioSpheres1](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_spheres1.jpg)
![cmftStudioOsx1](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_osx1.jpg)
![cmftStudioOsx0](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_osx0.jpg)


Planned features
------------

 * Add support for rendering transparent materials.
 * Add GGX specular filter and shading model.


Older screenshots taken during development
------------

![cmftStudio3](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_vn0.jpg)
![cmftStudio4](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio_vn1.jpg)
![cmftStudio5](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio3.jpg)
![cmftStudio1](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio1.jpg)
![cmftStudio1O](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio1_cmft_output.jpg)
![cmftStudio0](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftStudio0.jpg)
![cmftViewerG01](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer_g01.jpg)
![cmftViewerG02](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer_g02.jpg)
![cmftViewer7](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer7.jpg)
![cmftViewer8](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer8.jpg)
![cmftViewerF01](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer_f01.jpg)
![cmftViewer0](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer0.jpg)
![cmftViewer2](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer2.jpg)
![cmftViewer3](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer3.jpg)
![cmftViewer4](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer4.jpg)
![cmftViewer5](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer5.jpg)
![cmftViewer6](https://github.com/dariomanesku/cmftStudio/raw/master/screenshots/cmftViewer6.jpg)


Environment maps
------------

- [NoEmotion HDRs](http://noemotionhdrs.net/).<br />
- [sIBL Archive - Hdrlabs.com](http://www.hdrlabs.com/sibl/archive.html).<br />


Recommended tools
------------

- [PVRTexTool](http://community.imgtec.com/developers/powervr/) - for opening \*.dds and \*.ktx files.<br />
- [GIMP](http://www.gimp.org) - for opening \*.tga files.<br />
- [Luminance HDR](http://qtpfsgui.sourceforge.net/) - for opening \*.hdr files.<br />


Similar projects
------------

- [CubeMapGen](http://developer.amd.com/tools-and-sdks/archive/legacy-cpu-gpu-tools/cubemapgen/) - A well known tool for cubemap filtering from AMD.<br \>
- [IblBaker](https://github.com/derkreature/IBLBaker) - A similar open-source project.
- [Marmoset Skyshop](http://www.marmoset.co/skyshop) - Commercial plugin for Unity3D Game engine.
- [Knald Lys](https://www.knaldtech.com/lys-open-beta/) - Commercial tool from KnaldTech.


Contribution
------------

Everyone is welcome to contribute to cmftStudio by submitting code, bug reports, feature requests, testing on different platforms, profiling, etc.

When contributing to the cmftStudio project you must agree to the BSD 2-clause licensing terms.


Resources
------------
 - Grenade model - **[Kurt Kupser](http://kurtkupser.squarespace.com/)** \[[link](http://kurtkupser.squarespace.com/#/thermite-grenade/)\].
 - Flintlock model - **[Ben Cooney](http://ben3d.co.uk/)** \[[link](http://ben3d.co.uk/flintlock)\].
 - Cerberus gun model - **[Andrew Maximov](https://twitter.com/divers1ty)** \[[link](http://artisaverb.info/Cerberus.html)\].
 - Shack environment map - **[Jon Tojek](https://twitter.com/Tojek_VFX)** \[[link](http://tojek.com/vfx/?attachment_id=139)\].
 - Bolonga environment map - **[Marmoset pano pack](http://www.marmoset.co/panos)**


Thanks to
------------

* [Marko Radak](http://markoradak.com/) - Initial cover photo design and realization.
* [Dorian Cioban](https://www.linkedin.com/in/doriancioban) - Additional cover photo improvements.
* All authors of used assets in the project.


Contact
------------

Reach me via Twitter: [@dariomanesku](https://twitter.com/dariomanesku).


[License (BSD 2-clause)](https://github.com/dariomanesku/cmftstudio/blob/master/LICENSE)
-------------------------------------------------------------------------------

    Copyright 2014-2015 Dario Manesku. All rights reserved.

    https://github.com/dariomanesku/cmftStudio

    Redistribution and use in source and binary forms, with or without
    modification, are permitted provided that the following conditions are met:

       1. Redistributions of source code must retain the above copyright notice,
          this list of conditions and the following disclaimer.

       2. Redistributions in binary form must reproduce the above copyright notice,
          this list of conditions and the following disclaimer in the documentation
          and/or other materials provided with the distribution.

    THIS SOFTWARE IS PROVIDED BY COPYRIGHT HOLDER ``AS IS'' AND ANY EXPRESS OR
    IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF
    MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO
    EVENT SHALL COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT,
    INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING,
    BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE,
    DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF
    LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE
    OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF
    ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.


Disclaimer
---------

Licence applies only to cmftStudio project, NOT including the assets supplied in the sample projects. If you wish to use available third party resources, for any purpose, you must contact their respected authors/companies personally.
