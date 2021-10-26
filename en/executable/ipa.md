{
  "date" : "2021-08-30",
  "keywords" : [ "ipa file", "ipa file format", "what is a ipa file", "file", "ipa example", "ipa file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about IPA file format and APIs that can create and open IPA files.",
  "title" : "IPA - iOS Application Package File",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
    }
  },
  "lastmod" : "2021-08-30"
}

## What is a IPA file?
A file with .ipa extension belongs to the iOS and known as application package file. This is an archive (compressed using [ZIP](/compression/zip/) compression) file which stores an iOS application, but that application can only be installed on an iOS or ARM-based MacOS devices, such as an iPad, iPhone or iPod Touch. Mainly, iTunes, Apple Configurator 2, or any third party software can be used to install IPA files.

## IPA file format
The IOS developers who are developing the apps using the Apple Xcode are well familiar with IPA files because they need to package their developed apps as IPA files either for testing of app store deployment purposes. Although, the IPA files are known to be installed as iOS apps, however, you can also decompress them to view the app data contained. Since an IPA file contains only one binary for the ARM architecture of mobile phones and it does not contain a binary for the x86 architecture, Many .ipa files cannot be installed on the iPhone Simulator.
### Structure of a .ipa file
The following example shows the structure of an IPA: 

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
 The above is a built-in structure for iTunes and App Store to recognize. As per this structure:
- The Payload directory contains all the app data.
- The iTunes Artwork file is a 512×512 pixel PNG image, containing the app's icon for showing in iTunes and the App Store app on the iPad.
- The iTunesMetadata.plist contains various bits of information, ranging from the developer's name and ID, the copyright information, bundle identifier, the name of the app, genre, release date, purchase date, etc.
- The META-INF folder only contains metadata about what program was used to create the IPA.


## References 

* [.ipa - by Wikipedia](https://en.wikipedia.org/wiki/.ipa)

