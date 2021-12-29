{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MSIX - What is an MSIX file?",
  "description":"Learn about MSIX file and APIs that can create and open MSIX files.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-12-16"
}

## What is an MSIX file?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. This is the modern package file format as compared to the [APPX](/programming/appx/) and MSI that will be finally phased out to this new file format. It can be used for deployment of Win32, WPF, and Windows Forms apps. MSIX files are reliable, and target network and disk space optimization. Developers use these to distribute programs to end users through the Microsoft Store (previously known as Windows Store).

## MSIX File Format - More Information

MSIX files are [ZIP](/compression/zip/)-compressed, with all the files included inside the packaged file. In addition to the app related files, the MSIX file contains [.xml](/web/xml/) configuration files that contain information related to the app installation.

## What's Inside an MSIX package?

An MSIX package consists of the following files.

 * `AppxBlockMap.xml` - Known as the package block map file, it is an XML document that contains a list of app's files with indexes and cryptographic hashes for each block of data that is stored in the package.
 * `AppxManifest.xml` - An XML document that contains the information required for the deployment, display, and update of an MSIX app. This info includes package identity, package dependencies, required capabilities, visual elements, and extensibility points.
 * `AppxSignature.p7x` -  A file that is generated when the package is signed. All MSIX packages are required to be signed before install. With the AppxBlockmap.xml, the platform is able to install the package and be validated.

## References

 * [MSIX Overview](https://docs.microsoft.com/en-us/windows/msix/overview)
 * [Create APPX files using Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)
