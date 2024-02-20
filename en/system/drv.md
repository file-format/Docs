{
  "date": "2021-07-08",
  "keywords": [
    "DRV",
    "extension",
    "file",
    "format",
    "system",
    "Driver",
    "Windows Device Driver",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "DRV - Windows Device Driver",
  "description": "Learn about DRV file format and APIs that can create and open DRV files.",
  "linktitle": "DRV",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-drv"
    }
  },
  "lastmod": "2021-07-08"
}

## What is a DRV file? ##

The files with a .drv extension belong to the Windows Device Driver. Windows Operating System uses these files to connect internal and external hard devices. DRV files are consist of instructions and parameters for how a device and operating system link together. These files help to install device drivers for proper functioning with Windows. Also, the devices linked with the PC's motherboard via bus or cable require DRV files.


## DRV File Format ##

DRV files are usually packaged as dynamic libraries ([DDL](/system/dll/) files) or [EXE](/executable/exe/) files. These files can be supported on all system platforms, such as smartphones, and there is no assurance each platform will properly support these files. However, some most common devices that use the .drv file extension are:

*	Sound cards
*	Graphic cards
*	Printers
*	Storage devices
*	Network adapters
*	Computer hardware accessories

It is recommended not to open DRV files sent via email because this file format contains viruses and other malicious programs. Make sure to perform a comprehensive scan before opening any unknown DRV file.


## DRV Example ##

```
// Include necessary files...
#include <font.defs>
#include <media.defs>
#include <hp.h>
#include <epson.h>
#include <label.h>

// Localizations are provided for all of the base languages supported by
// CUPS...
#po ar ""
#po ca ""
#po de ""
#po el ""
#po es ""
#po fr ""
#po no ""
#po ru ""
#po sk ""
#po sv ""
#po th ""
#po tr ""
#po uk ""

// MediaSize sizes used by label drivers...
#media "w90h18/1.25x0.25\"" 90 18
#media "w90h162/1.25x2.25\"" 90 162
#media "w108h18/1.50x0.25\"" 108 18
#media "w108h36/1.50x0.50\"" 108 36
#media "w108h72/1.50x1.00\"" 108 72
#media "w108h144/1.50x2.00\"" 108 144
#media "w144h26/2.00x0.37\"" 144 26
#media "w576h360/8.00x5.00\"" 576 360
#media "w576h432/8.00x6.00\"" 576 432
#media "w576h468/8.00x6.50\"" 576 468

// Common stuff for all drivers...
Attribute "cupsVersion" "" "2.2"
Attribute "FileSystem" "" "False"
Attribute "LandscapeOrientation" "" "Plus90"
Attribute "TTRasterizer" "" "Type42"

Font *

Version "2.1"

// Dymo Label Printer
{
  Manufacturer "Dymo"
  ModelName "Label Printer"
  Attribute NickName "" "Dymo Label Printer"
  PCFileName "dymo.ppd"
  DriverType label
  ModelNumber $DYMO_3x0
  Throughput 8
  ManualCopies Yes
  ColorDevice No

  HWMargins 2 14.9 2 14.9

  *MediaSize w81h252
  MediaSize w101h252
  MediaSize w54h144
  MediaSize w167h288
  MediaSize w162h540
  MediaSize w162h504
  MediaSize w41h248
  MediaSize w41h144
  MediaSize w153h198

  Resolution k 1 0 0 0 136dpi
  Resolution k 1 0 0 0 203dpi
  *Resolution k 1 0 0 0 300dpi

  Darkness 0 Light
  Darkness 1 Medium
  *Darkness 2 Normal
  Darkness 3 Dark
}

```
