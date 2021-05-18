{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "APK - Android Package File Format",
  "description":"Learn about APK file format and APIs that can create and open APK files.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-27"
}

## What is an APK file?

A file with .apk extension is a Google Android app file that is used to install apps (applications) on the Android devices. It is created as an executable file using the official IDE Google Android Studio, and is uploaded to Google Play store to be downloaded and installed by end users. APK files can be generated and made available for manual installation as well prior to publishing to Google Play store. However, in manual case, you need to be sure about the source of such file as to avoid any malware infecting mobile devices.

## APK File Format

APK files are packaged as compressed in [ZIP](/compression/zip/) file format that can be opened with any ZIP file opening software. The .apk extension of such a file can be renamed to .zip and open the file in any ZIP application or extract its contents.

## APK Package Contents

A single APK file contains all the necessary files that are required for its installation and execution. When such an APK file is opened in a ZIP application, the following mostly used files and folders are found.

 * `META-INF/`: Directory that contains the manifest file, signature, and a list of resources in the archive
 * `lib/`: Directory containing compiled code related to specific platforms such as armeabi-v7a, x86, arm64-v8a, etc.
 * `res/`: Directory containing Non-compiled resources such as images
 * `assets/`: Directory containing applications assets, which can be retrieved by AssetManager.
 * `androidManifest.xml`: Contains the name, versioning information and contents of the APK file
 * `classes.dex`: These are compiled Java classes that can be run on Dalvik virtual machine and by the Android Runtime
 * `resources.arsc`: Compiled resources file such as strings

## How to open an APK file?

If you have an APK file, you can open it using the following programs.

|Operating System|Programs that can open APK files|
---|---|
|Windows| Google Android Studio, Corel WinZip, 7-Zip, RARLAB WinRAR, Google Android SDK|
|Mac|Google Android Studio, Apple Archive Utility|
|Linux| Google Android SDK|

## References

* [APK File Format](https://en.wikipedia.org/wiki/Android_application_package)
