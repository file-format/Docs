{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LBR - LU Library Archive File Format",
  "description":"Learn about LBR file format and APIs that can create and open LBR files.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-19"
}

## What is a LBR file?

A file with .lbr extension is an archive file created with LU program and used on CP/M and DOS operating systems during 1980s. It is no longer being used and has been replaced by modern archiving file formats. The format does not compress the member files and acts as container archive for these. The archiving feature was mostly used for transfer of archived files over the internet. Since LBR didn't offer compression, other utilities such as SQ or CRUNCH were used to compress the member files pre-archiving or the resultant archive file post-archiving to reduce its size.

## LBR File Format

LBR file format was designed by Gary P. Novosielski and has no technical details available publicly. LBR files start with a 0x00 byte, followed by 11 spaces (0x20), then two 0x00 bytes, then two bytes that are not both 0x00. Being container file format, it can be extracted using the LU.COM and NULU.COM.

## References

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))
