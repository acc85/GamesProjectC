GamesProjectC
=============

C++ Games Project

##Install MingW

Got to the following Link:

- [MingW Sourceforge Windows exe](http://sourceforge.net/projects/mingw/files/Installer/mingw-get-inst/mingw-get-inst-20120426/mingw-get-inst-20120426.exe/download)

- [MingW Sourceforge tar](http://sourceforge.net/projects/mingw/files/Installer/mingw-get-inst/mingw-get-inst-20120426/mingw-get-inst-src-20120426.tar.xz/download)

For the windows installation, just open the EXE and install.

For linux, download the tar, extract it, make and build


## Seting Up Eclipse

To install Eclipse you can either download the Eclipse C/C++ IDE from:

[Windows 32-bit](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/juno/R/eclipse-cpp-juno-win32.zip)
[Windows 64-bit](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/juno/R/eclipse-cpp-juno-win32-x86_64.zip)

[Linux 32-bit](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/juno/R/eclipse-cpp-juno-linux-gtk.tar.gz)
[Linux 64-bit](http://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/juno/R/eclipse-cpp-juno-linux-gtk-x86_64.tar.gz)

Or you if you already have Eclipse somewhere on your machine, you can download the Plugins from the repository, depending on which version you have. If you are having trouble with installation stalling at a certain percentage. Do the Following:

```plugin
Create a shortcut to to eclipse or if you already have a shortcute, add the following to to Target after your the location of the eclipse:

--vmargs -Djava.net.preferIPv4Stack=true

##Setting Up Project

Once you have setup mingW and Eclipse, clone the project into eclipse via git.

Afterwards to must set up the compiler flags for the project. You can do it for both debug and release builds. To do this, RightCclick on the Root Project Folder GameProject or whatever you named it and choose Properties, then from there go to C/C++ Build->Settings, then on the right side choose MingGW C++ Linker then Miscellaneous, At the Top it will say configuration with a drop down box for Debug, Release and Allconfiguration. i suggest adding it for All configuration, so select the option form the drop down box, then add the folowing into the Linker Flags box: 

```LinkerFlags

-static-libgcc -static-libstdc++

You should be able to build and compile your program.

