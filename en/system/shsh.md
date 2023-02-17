{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH File - iPhone/iPod Touch SHSH Blob File Format",
  "description":"Learn about what is an SHSH file.",
  "linktitle" : "SHSH",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh",
      "parent" : "system"
    }
  },
  "lastmod" : "2023-02-16"
}

## What is an SHSH file?

An SHSH file, also known as a Signature HaSH, is a digital signature used by Apple to authenticate and verify firmware updates for iOS devices such as iPhones, iPads, and iPods.

## Differnece between SHSH and SHSH2 File Formats

Like an SHSH2 file, the SHSH file contains a unique identifier for the device called an "ECID" (Exclusive Chip ID), as well as information about the firmware version installed on the device. However, SHSH files were used in older versions of iOS (prior to iOS 10) and have since been replaced by SHSH2 files.

## SHSH File Format - More Information

SHSH files are saved to disc in binary file format. The internal file structure details of this file format is not available publicly.

SHSH files are important for users who want to downgrade their device's firmware to a previous version that is no longer being signed by Apple. By saving the SHSH files for a specific firmware version when it is still being signed by Apple, users can later use them to bypass Apple's signature verification and install that firmware version on their device. This process is also known as `jailbreaking`.

## References

* [SHSH Blob - By Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)
