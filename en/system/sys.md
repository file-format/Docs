{
  "date" : "2021-07-08",
  "keywords" : [ "SYS", "extension", "file", "format", "system", "Driver", "System File", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SYS - System File Format",
  "description":"Learn about SYS file format and APIs that can create and open SYS files.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-07-08"
}

## What is an SYS file? ##

The SYS files are "System files" used in Windows OS and MS-DOS applications. These files cannot be opened directly and consist of the driver and configuration of the device. The SYS files are responsible for containing files of core functions of the operating system. These are considered critical files of the device driver and can also be used when any issue of the race driver is to be solved. These are responsible for the proper functioning of a computer system, and the .sys files must be correct and complete. 


## Technichal Specification ##

The .sys files are actually the subset of the [BMP](/image/bmp/) format as it only allows specific combinations. The usual format of these files is like LOGOS.SYS, LOGOW.SYS, and LOGO.SYS. Any other files do not have this format.

These files are mostly used within the *C* directory of Windows at the time of installation. Most issues that revolve around device drivers are resolved by updating the Windows OS. The details and information of these files can be viewed by using the built-in programs of Windows OS. These also comprise the references to different modules in an operating system.
Some of the examples of system files are :

*  IO.SYS ( These store device drivers of disk operating system)
*  MSDOS.SYS ( These contain kernel or the core code of operating system)
*  CONFIG.SYS ( These contain various configuration options)
*  KEYBOARD.SYS ( These contain keyboard layout related information) 
*  COUNTRY.SYS ( These contan country and codepage related information)

## SYS File Format ##

Microsoft developed the files with .sys extensions. Variables and functions are included in SYS files. These are mostly used by Microsoft operating system. These files are mainly located in the root directory of the disk:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Some common warning about SYS files are as follow:

*	The names of these files should not be changed as these files are responsible for core functions and variables of the operating system
*	These files should not be deleted because their absence of these files can cause errors
*	The .sys files should not be downloaded from the internet until you are sure about the legitimacy of the source
*	One should not mess with these files as changing them or messing with these causes serious system errors
*	If these files become corrupted by some virus or malware, these should be re-installed

## SYS Example ##

The following is an example of a simple SYS system configuration file:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```