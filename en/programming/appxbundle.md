{
  "date" : "2021-04-22",
  "keywords": [ "appxbundle file", "extension", "format","how to open appxbundle file","appxbundle file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "appxbundle - What is an APPXBundle file?",
  "description":"Learn about APPX file format and APIs that can create and open APPX files.",
  "linktitle" : "APPXBUNDLE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-12-19"
}

## What is an APPXBUNDLE file?

An APPXBUNDLE file is a package file created with [Microsoft Visual Studio](https://visualstudio.microsoft.com/) and is used for distribution of Windows apps (both Desktop and UWP) on [Microsoft Store](https://www.microsoft.com/en-us/store/apps/windows). It contains one or more versions of an app, targeting specific processor architecture such as x86, x64, or ARM. This lets the end user to receive and deploy the appropriate version of the app based on the computer architecture. APPXBUNDLE files are grouped together using the standard [ZIP](/decompression/zip/) file format. Microsoft Visual Studio's Publish method is used to publish the apps as a bundle. Single package apps are distributed as [APPX](/programming/appx/) files.

## APPXBUNDLE File Format

APPXBUNDLE files are published in ZIP file format. If you want to see the contents of the app package, you can extract the contents of it using decompression utilities such as [WinZIP](https://www.winzip.com/en/) or WinRAR.

## References

 * [Dependency packages for .appx and .appxbundle packages](https://www.ibm.com/docs/en/maas360?topic=catalog-dependency-packages-appx-appxbundle-packages)
 * [Create APPX files using Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)
