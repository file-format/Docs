{
  "date": "2022-02-16",
  "keywords": [
    "obb file",
    "obb file format",
    "what is an obb file",
    "file",
    "obb example",
    "obb file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "OBB File Format - Android Opaque Binary Blob File",
  "description": "Learn about OBB file format and APIs that can create and open OBB files.",
  "linktitle": "OBB",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-obb"
    }
  },
  "lastmod": "2022-02-16"
}

## What is an OBB file?

An OBB file is an expansion file that contains additional data that is in addition to the Android [APK](/compression/apk/) file. Google Play store does not allow to have a an Android APK file with size more than 100 MB. But some applications may require high definition graphics, media files, or other large assets to be hosted in addition to the APK files. That is where the OBB file types come in. Google Play allows to attach these expansion files as a supplement to the APK file.

## OBB File Format

OBB files are saved as binary files along with the APK files. When an APK accompanies the OBB files, Google Play hosts the expansion files on its server and no additional cost is charged to the developer. These additional files are stored the device's shared storage on SD card or USB-mountable partition when the app is downloaded for installation.

The OBB files are downloaded and installed upon downloading. But in some cases, these are downloaded for installation when the application is run for the first time.

### OBB Maximum File Size

Google Play Store lets you uploaded OBB expansion files of size up to 2 GB. Large size fils are recommended to be uploaded as compressed [ZIP](/compression/zip/) files for efficient uploading via internet.

These expansion files can be hosted either as **main** primary expansion file for additional resources required by the app or an optional patch expansion file intended for small updates to the main expansion file.

## References

* [Android Developers - Expansion Files](https://developer.android.com/google/play/expansion-files)
