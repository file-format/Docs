{
  "date" : "2021-04-11",
  "keywords" : [ "xapk file", "xapk file format", "what is a xapk file", "file", "xapk example", "xapk file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XAPK - Meta Package File Format",
  "description":"Learn about XAPK file format and APIs that can create and open XAPK files.",
  "linktitle" : "XAPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-11"
}

## What is a XAPK file?

A file with .xapk extension is a compressed package file that is used to install Android apps on mobile devices. It is a container file format that incorporates APK and additional associated files required for the installation. The other associated file is an OBB file that stores additional files such as graphics, media files, and app data that are required to keep the application running. XAPK files are not supported by Google Play and are used for distributing on third-party Android app download websites only. These can be installed to an Android device using XAPK Installer.

## XAPK File Format

XAPK files are compresed using the standard [ZIP](/compression/zip/) file format. These can be extracted using a standard compression/decompression software such as WinZIP. Once the XAPK file is extracted to the disc, it contains the following files in folder.

 * APK - Standard installation file for installing the application on Android devices
 * OBB - Additional file that contains relevant resource files

## References

* [Android Package File](https://en.wikipedia.org/wiki/Android_application_package)
