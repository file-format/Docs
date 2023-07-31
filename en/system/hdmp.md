{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HDMP File - Windows Heap Dump File Format",
  "description":"Learn about HDMP file format and APIs that can create and open HDMP files.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2022-08-19"
}

## What is a HDMP file?

HDMP file is an uncompressed memory dump when an application or program crashes due to an error. It is only created by Windows XP/Vista and contains a dump of the application's status when it was crashed. Being uncompressed, the HDMP files take more space on the disc as compared to the Minidump [MDMP](/system/mdmp/) files that are compressed for reporting purpose.

Applications that can be used to **open** or analyze HDMP files include Microsoft Visual Studio with Debugging tools for Windows.

## HDMP File Format

HDMP files are stored to disc as binary files and do not provide any benefit if opened without appropriate applications. These contain relevant system data recorded when the error occurred.

### Difference between HDMP and MDMP File Formats

HDMP are uncompressed memory dump files. In contrast, MDMP are mini dump files that are compressed for reduction in file size and sending to Microsoft for reporting the issue.

## Reference ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)
