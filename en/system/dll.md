{
  "date" : "2021-06-29",
  "keywords" : [ "DLL", "extension", "file", "format", "system", "Dynamic Link Library", "settings", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DLL - Dynamic Link Library",
  "description":"Learn about DLL file format and APIs that can create and open DLL files.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-06-29"
}

## What is a DLL file? ##

A DLL file or Dynamic Link Library is a type of executable file. It is one of the most commonly found extension files on your device and is usually stored in the System32 folder on your Windows. The DLL extension file was developed by Microsoft and is popularly used by them. It has a high popularity user rating. The DLL works as a shelf that contains the *drivers/procedures/functions/properties* that are designed and applied for a program/application by the windows server. A single DLL file can also be shared amongst various windows programs. These extension files are vital for the smooth running of Windows programs on your device as they are responsible for enabling and running various functions on the program such as writing and reading files, connecting with other devices that are external to your setup.
These Files however can only be opened on a device that supports any version of Windows (windows 7/windows 10/etc.) and hence cannot be opened directly on a device that supports Mac OS. (If you want to open a DLL file on Mac OS, various external applications can help open them.)


## DLL File Format ##

DLL file was developed by Microsoft and has the extension ".dll" that represents the type. It has been an integral part of the Windows 1.0 server, and beyond. It is a binary file type and supported by all versions of Microsoft Windows. This file type was created as means to create a shared library system within Windows programs, to allow for separate and independent edits or changes in the program libraries without the need to re-linking the programs.


## DLL Example ##

Example code for a DLL entry point can be found below:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
    }
    return TRUE;
}

```

## Reference ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)