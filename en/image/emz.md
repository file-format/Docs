{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EMZ File Format - A Windows Compressed Enhanced Meta file",
  "description":"Learn about EMZ file format and APIs that can create and open EMZ files.",
  "linktitle" : "EMZ",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2020-10-24"
}

## What is an EMZ file?

A file with .emz extension is a compressed container of Enhanced Metafile ([EML](/image/emf/) file). These are compressed using the [GZIP](/compression/gz/) compression technique which is the commonly used compression method on UNIX and LINUX operating systems. Unlink ZIP (/compression/zip/), GZIP compresses the archive as a whole instead of compressing individual files. EMZ files are smaller in size as compared to the EMF files and help in fast transfer during online file sharing. Some of the applications that can open EMZ files include Microsoft Visio 2019, Microsoft Office 2019, XnView MP, and File Viewer Plus.

## EMZ File Format

EMZ files are [Gzip](/compression/gz/) compressed and contains [EMF](/image/EMF/) inside. Gzip uses the DEFLATE algorithm for compression of the archive and is different in applying compression. An EMZ file can be decompressed by using GZip compression utilities such as GNU Zip. The file format consists of:

 * File Header
 * Optional Headers
 * Compressed Data
 * File Footer

The GZIP file format [specifications version 4.3](http://tools.ietf.org/html/rfc1952) published by Internet Engineering Task Force (IETF) contains detailed information about the file format.

## References

 * [RFC1952: GZIP file format specification](http://tools.ietf.org/html/rfc1952), by [IETF](https://forensicswiki.org/index.php?title#IETF&action#edit&redlink#1)
 * [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)
