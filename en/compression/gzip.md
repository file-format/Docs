{
  "date": "2022-06-26",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "GZIP File Format - GNU Zipped Archive File",
  "description": "Learn about what is a GZIP file and APIs that can create and open GZIP files.",
  "linktitle": "GZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-gzip"
    }
  },
  "lastmod": "2022-06-26"
}

## What is a GZIP file?

A GZIP file is a compressed archive that is created with the standard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip) compression algorithm. The compressed archive may contain multiple files including compressed files, directories and file stubs. Most of the Unix systems include the open source gzip (GNU Zip) compressor utility for compression/decompression of files. GZIP files can be opened with applications such as [WinZip](https://www.winzip.com/en/).

## GZIP File Format - More Information

GZIP uses the [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) algorithm to compress files to archives. Two RFCs, [RFC1952](https://tools.ietf.org/html/rfc1952) and [RFC 1951](https://tools.ietf.org/html/rfc1951), define the specifications of the gzip wrapper format and deflate compressed data format, respectively.

GZIP files are often saved as [GZ](/compression/gz/) file format.

## References

* [gzip](http://www.gzip.org/)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: GZIP file format specification](https://datatracker.ietf.org/doc/html/rfc1952), by IETF
* [RFC 1951](https://tools.ietf.org/html/rfc1951)
