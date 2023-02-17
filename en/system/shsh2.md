{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH2 File - iOS SHSH Blob File Format",
  "description":"Learn about what is an SHSH2 file.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
    }
  },
  "lastmod" : "2023-02-16"
}

## What is an SHSH2 file?

An SHSH2 file, also known as a SHSH blob or ECID SHSH, is a digital signature used by Apple to authenticate and verify firmware updates for iOS devices such as iPhones, iPads, and iPods. It contains a unique identifier for the device that is known as ECID (Exclusive Chip ID). It also contains information about the firmware version installed on the device.

## SHSH2 File Format - More Information

SHSH2 files are saved to disc in binary file format and the internal file structure details of this file format is not available publicly.

When a new version of iOS is installed on an Apple device such as iPhone, iPad, or Mac, an SHSH2 file is generated. This SHSH2 file is sent to Apple servers which reads and verifies this digital signature file. Based on this information, the server allows or prevents the installation.

The same happens when an update is requested. When a user requests an update or restore of their device through iTunes or another software, Apple's servers will check that the SHSH2 file matches the device's ECID and firmware version before allowing the update to proceed.

## References

* [SHSH Blob - By Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)
