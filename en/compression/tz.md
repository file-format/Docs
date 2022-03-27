{
  "date" : "2022-03-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TZ - Zipped Tar Archive File Format",
  "description":"Learn about what is a TZ file and APIs that can create and open TZ files.",
  "linktitle" : "TZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-03-24"
}

## What is a TZ file?

A TZ file is a TAR archive compressed with Unix compression algorithm. It is a combination of [TAR](/compression/tar/) archive and [Z](/compression/z/) compressed files, and is a native compression format for Unix OS. TZ files can be opened using standard compression utilities such as WinZIP and WinRAR.

## TZ File Format

TZ files are saved as binary files using the UNIX compression algorithm. The use of Z files makes formatting, running and opening of files easier. TZ files are smaller in size as the Z compression achieves high compression. Resultant files occupy less space on disc and are easily transferrable over communication media.

## References

* [TAR - By Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR Basic Format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)
