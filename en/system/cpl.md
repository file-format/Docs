{
  "date": "2021-06-29",
  "keywords": [
    "CPL",
    "extension",
    "file",
    "format",
    "system",
    "Control Panel File",
    "Windows",
    "programs",
    "computer",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "CPL - Control Panel File",
  "description": "Learn about CPL file format and APIs that can create and open CPL files.",
  "linktitle": "CPL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cpl"
    }
  },
  "lastmod": "2021-06-29"
}

## What is a CPL file? ##

A CPL file is a type of "system" file. It is used by the Windows operating system. A CPL file is short for Control Panel File. These files are binary files that open with the control panel in a Microsoft Windows operating system and are used to represent and open the tools available in the control panel, such as Mouse, Displays, Networking, amongst others. The CPL files are typically stored in the system folder on your device. These files should not be opened manually.


## CPL File Format ##

Different CPL files in your Windows operating system are connected to represent different control panel items. All control panel items are linked to a CPL file and have the suffix “.cpl” attached to their items. 

Some common types of CPL files with their formats are:

* Inetcpl.cpl – For Internet properties on your device
* Appwiz.cpl – To Add or Remove Programs properties on your device
* Desk.cpl – For the Display properties
* Main.cpl – For properties related to Mouse, Fonts, Keyboard, and Printers. 
* Netcpl.cpl – For Network related properties
* System.cpl – For System related properties and to Add New Hardware wizard
* TimeDate.cpl – For Date or Time properties
* Mlcfg32.cpl – For Microsoft Exchange or Windows Messaging properties
* Intl.cpl – This pertains to Regional Settings properties
* Modem.cpl – For Modem related properties
* Themes.cpl – Stores Desktop Themes and properties. 
* Password.cpl – For Password properties
* Mmsys.cpl – For Multimedia properties
* Wgpocpl.cpl – Pertains to Microsoft Mail Post Office

## Brief History ##

CPL file type was developed by Microsoft Windows and is an integral part of the Windows operating system since Windows 1.0. It is still used in all Windows versions, and all control panel item properties are stored using this file type.

## CPL Example ##

A sample CPL file can be seen below:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```