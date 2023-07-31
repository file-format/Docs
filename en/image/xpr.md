{
  "date" : "2022-03-21",
  "keywords" : [ "xpr file", "xpr file format", "what is an xpr file", "file", "xpr example", "xpr file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XPR File Format - Microsoft Expression Design Graphic File",
  "description":"Learn about XPR file format and APIs that can create and open XPR files.",
  "linktitle" : "XPR",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2022-03-21"
}

## What is an XPR file?

An XPR file is a vector image file created with the now-discontinued Microsoft Expression Graphics (EGD) software. It contains graphics information that can used as user interface mockup. XPR files were later replaced by .design files in Microsoft Expression Design. XPR files could be opened with Microsoft Expression Studio that has been discontinued for quite some time now.

## XPR File Format Vulnerability

XPR files were identified to benefit a vulnerability in Microsoft Expression Design, leading to allow execution of remote code. In the reported issue, if a user opened a legitimate .xpr file that is lcoated in the network directory along with dynamic link library (DLL) file, Microsoft Expression Design could attempt to load the DLL file and execute the code it contained. This was later fixed by Microsoft in a security update.

## References

* [Vulnerability in Expression Design Could Allow Remote Code Execution (2651018)](https://learn.microsoft.com/en-us/security-updates/securitybulletins/2012/ms12-022)
