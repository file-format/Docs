{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "APPX - What is an APPX file?",
  "description":"Learn about APPX file format and APIs that can create and open APPX files.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-12-16"
}

## What is an APPX file?

An APPX file is a distributable package file format that is used for distribution and installation of an application. It was introduce with Windows 8 to be published on Microsoft Windows Store. It contains all the files required to install a Windows application. These include metadata, files, and credentials information. A more modern packaging file format is MSIX that is currently more commonly used as compared to APPX.

## APPX File Format - More Information

APPX files are saved as compressed files in [ZIP](/compression/zip/) file format. This makes the entire package as an archive file with reduced file size that is easy to be uploaded to the Microsoft Store.

## How to view files in an APPX file?

In order to view the contents or files inside an APPX file, the following steps should be followed.

 1. Since APPX files are stored as compressed ZIP files, rename the file to .zip extension
 1. Use any decompression tool such as 7-Zip, WinZip, or WinRAR to extract the files contained in the APPX file

## How to Create an APPX file?

There are two methods that can be used to create APPX files.

 1. Using MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) is used to create both app packages (.msix or .appx) and app package bundle files .msixbundle or .appxbundle). In addition, it can extract files from an app package. MakeApp.exe is available with Windows 10 SDK and can be used from command prompt.
 1. Using Microsoft Visual Studio - Developers usually [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) using Microsoft Visual Studio. Once the application development is complete and the app is ready to be published, APPX package file can be created by publishing it from within the Visual Studio.

## References

 * [Create an MSIX package or bundle with MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Create APPX files using Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)
