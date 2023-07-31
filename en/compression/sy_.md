{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SY_ File Format - Compressed SYS File",
  "description":"Learn about SY_ file format and APIs that can create and open SY_ files.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-06-24"
}

## What is a SY_ file?

A SY_ file is a compressed .sys file that is used by software installers to reduce the size of the installation files packaged inside the installer. This reduces the overall size of the installer. SY_ files can be expanded using the Microsoft Expand command line utility that expands one or more compressed files.

## SY_ File Format - More Information

SY_ files are saved to disc as compressed binary files. However, their internal file format is not available publicly. The Microsoft Expand command line utility can expand SY_ files using one of the following command lines.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
When expanded, the SY_ files are converted to [SYS](https://docs.fileformat.com/system/sys/) file.

SY_ files are similar to EX_ and DL_ files.

## References

 * [StuffIt - By Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)
