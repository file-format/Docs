{
  "date": "2021-08-27",
  "keywords": [
    "wsh file",
    "wsh file format",
    "what is a wsh file",
    "file",
    "wsh example",
    "wsh file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about WSH file format and APIs that can create and open WSH files.",
  "title": "WSH - Windows Script File",
  "linktitle": "WSH",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-wsh"
    }
  },
  "lastmod": "2021-08-27"
}

## What is a WSH file?
A file with .wsh extension contains properties and parameters for a certain programming language script such as VB or VBS etc. The actual need of WSH is to use them for customizing the execution of certain scripts. WScript or CScript are required to run and both of these are included with the Windows operating system. WSH files were initially provided on Windows 95 on the installation discs as an optional configurable and installable for the Control Panel, and then a default component of Windows 98.

## WSH file format
WSH (Windows Script Host) may be used for a various purposes, including administration, logon scripts and general automation. WSH establishes an environment for scripts to run. it invokes the suitable script engine and allocate a set of services and objects for the script to work with. These scripts can be run in GUI mode, from a COM object or command line mode, providing flexibility to the user for both interactive or non-interactive scripts. 

### Examples
Here is very simple example which shows some VBScript which uses the root WSH COM object "WScript" to display a message with an 'OK' button. When this script will be launched the CScript or WScript engine would be called and the runtime environment will be established.

```
WScript.Echo "Hello world"
WScript.Quit
```


## References 

* [Windows Script Host - by Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)


