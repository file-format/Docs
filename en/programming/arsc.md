{
  "date": "2019-10-11",
  "keywords": [
    "arsc",
    ".arsc",
    "what is a arsc file",
    "how to open arsc file",
    "extension",
    "file",
    "arsc file",
    "arsc file format",
    "arsc file extension",
    "arsc File Example"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ARSC - Android Package Resource Table File ",
  "description": "Learn about ARSC file format and APIs that can create and open ARSC file.",
  "linktitle": "ARSC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-arsc"
    }
  },
  "lastmod": "2021-06-22"
}

## What is an ARSC file?

An ARSC file is an Android Resource table file that contains the application's list of resources in a table-format. This contains information such as Resource names, properties, and IDs. ARSC files are part of APK packages that are used to install these Android apps. All the resources such as images, layouts, styles, and strings, in an android application are converted into binary files when the APK file is generated. The ARSC file is also generated at the same, containing list of all the program's compiled resources and their IDs.

## ARSC File Format

The .arsc extension files are binary files generated after the compiler, such as ANT (Eclipse) or Gradle (AS), compiles the Android application code to produce the [APK](/compression/apk/) file. You can extract the APK file using any archiving utility such as WinZip to view its contents, which are the compiled java class files i.e. classes.dex. In addition to these, it contains this ARSC file as well that contains meta-information about:

 * The XML nodes
 * The attributes
 * The Resource IDs

 Resources in an APK file are referred by the Resource IDs, while the attributes are resolved to a value at runtime. The Android aapt tool collects all of the resources defined in files at build time and assigns resource IDs to them. After identifiers are assigned to the compiled resources, a R.java file is generated from the source code as well as the resources.arsc.

## References

* [Binary Resource Table Structure](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)
* [Take Screenshot on Android](https://how-to-take-screenshot.com/)
