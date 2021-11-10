{
  "date" : "2019-10-11",
  "keywords" : [ "apk file", "apk file format", "what is a apk file", "file", "apk example", "apk file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "APK - Android Package File Format",
  "description":"Learn to know what is an APK file and APIs that can create and open APK files.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-27"
}

## What is an APK file?

A file with .apk extension is a Google Android app file that is used to install apps (applications) on the Android devices. It is created as an executable file using the official IDE Google Android Studio, and is uploaded to Google Play store to be downloaded and installed by end users. APK files can be generated and made available for manual installation as well prior to publishing to Google Play store. This helps in testing the functionality and behaviour of the generated APK package file. Therefore, one needs to be sure that the APK file is from a trusted source and does not contain any malware.

## APK File Format

APK files are packaged as compressed in [ZIP](/compression/zip/) file format that can be opened with any ZIP file opening software. The .apk extension of such a file can be renamed to .zip and open the file in any ZIP application or extract its contents.

## APK Package Contents

A single APK file contains all the necessary files that are required for its installation and execution. An APK file, when extracted with a ZIP application, contains the following files and folders.

 * `META-INF/`: Directory that contains the manifest file, signature, and a list of resources in the archive
 * `lib/`: Directory containing compiled code related to specific platforms such as armeabi-v7a, x86, arm64-v8a, etc.
 * `res/`: Directory containing Non-compiled resources such as images
 * `assets/`: Directory containing applications assets, which can be retrieved by AssetManager.
 * `androidManifest.xml`: Contains the name, versioning information and contents of the APK file
 * `classes.dex`: These are compiled Java classes that can be run on Dalvik virtual machine and by the Android Runtime
 * `resources.arsc`: Compiled resources file such as strings

## How to install APK file on Android Device?

In order to install an APK file on your Android devices, the following steps can be used.

 1. Download the APK using web browser
 2. Tap it – you should then be able to see it downloading on the top bar of your device
 3. Once it's downloaded, open Downloads, tap on the APK file, and tap Yes when prompted.

Following these steps will start installation of the app on your device.

## References

* [APK File Format](https://en.wikipedia.org/wiki/Android_application_package)
