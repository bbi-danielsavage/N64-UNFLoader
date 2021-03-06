# UNFLoader

[![Build Status](https://dev.azure.com/buu342/buu342/_apis/build/status/buu342.N64-UNFLoader?branchName=master)](https://dev.azure.com/buu342/buu342/_build/latest?definitionId=1&branchName=master)

**The code in this repo might be unstable! For stable versions, head to the [releases page](https://github.com/buu342/N64-UNFLoader/releases)**

UNFLoader is a USB ROM uploader (and debugging) tool designed to unify developer flashcarts for the Nintendo 64. The goal of this project is to provide developers with USB I/O functions that work without needing to worry about the target flashcart, provided by a single C file (`usb.c`) targeting libultra. An very basic debug library (`debug.c`) that makes use of said USB library is also provided.

Currently supported devices:
* 64Drive Hardware 1.0 (No longer comercially sold), using firmware 2.05+
* [64Drive Hardware 2.0](http://64drive.retroactive.be/), using firmware 2.05+
* EverDrive 3.0 (No longer comercially sold), using OS version 3.04+
* [EverDrive X7](https://krikzz.com/store/home/55-everdrive-64-x7.html), using OS version 3.04+
* [SummerCart64](https://github.com/Polprzewodnikowy/SummerCollection)
</br>

### Table of contents
* [UNFLoader](UNFLoader)
    - [System Requirements](UNFLoader#system-requirements)
    - [How to use UNFLoader](UNFLoader#how-to-use-unfloader)
    - [How to build UNFLoader for Windows](UNFLoader#how-to-build-unfloader-for-windows)
    - [How to build UNFLoader for Linux](UNFLoader#how-to-build-unfloader-for-linux)
* [USB + Debug Library](USB%2BDebug%20Library)
    - [How to use the USB library](USB%2BDebug%20Library#how-to-use-the-usb-library)
    - [How to use the Debug library](USB%2BDebug%20Library#how-to-use-the-debug-library)
    - [How these libraries work](USB%2BDebug%20Library#how-these-libraries-work)
* [Example ROMs](Examples)
    - [Print "Hello World"](Examples#1-hello-world)
    - [Handle thread faults](Examples#2-thread-faults)
    - [Read from USB](Examples#3-raw-usb-reading)
    - [Interpret USB commands](Examples#4-command-interpreter)
* [Extending UNFLoader](#extending-unfloader)
* [Known Issues and Suggestions](#known-issues-and-suggestions)
* [Credits](#credits)
</br>

### Extending UNFLoader

This repository has a [wiki](../../wiki) where the tool, it's libraries, and the supported flashcarts are all documented. It is recommended that you read through that to familiarize yourself with everything. If you want to submit changes, feel free to fork the repository and make pull requests!
</br>
</br>
### Known issues and suggestions

All known issues are mentioned in the [issues page](../../issues). Suggestions also belong there for the sake of keeping everything in one place.
</br>
</br>
### Credits
Marshallh for providing the 64Drive USB application code which this program was based off of.

KRIKzz, saturnu, networkfusion, lambertjamesd, and jsdf for providing sample code for the EverDrive 3.0 and/or X7.

fraser and networkfusion for all the help provided during the development of this project as well as their support.

networkfusion for lending me his remote test rig for the ED3 and X7, as well as setting up the azure pipeline system and helping organize this repo.

danbolt for helping test this on Debian, as well as providing changes to get the tool compiling under macOS.

korgeaux for implementing support for his SummerCart64.

CrashOveride for ensuring the samples compile on his Linux libultra port. 

This project uses [lodePNG](https://github.com/lvandeve/lodepng) by Lode Vandevenne, [ncurses](https://invisible-island.net/ncurses/) by the GNU Project, [pdcurses](https://github.com/wmcbrine/PDCurses) by William McBrine, and the [D2XX drivers](https://www.ftdichip.com/Drivers/D2XX.htm) by FTDI.

The folk at N64Brew for being patient with me and helping test the program! Especially command_tab, networkfusion, CrashOveride, gravatos, PerKimba, manfried and kivan117. You guys are the reason this project was possible!
