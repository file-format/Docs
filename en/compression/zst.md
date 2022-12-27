{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ZST File - Zstandard Compressed File Format",
  "description":"Learn about ZST file format and APIs that can create and open ZST files.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst",
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-12-26"
}

## What is a ZST file?

A ZST file is a compressed file that is generated with the Zstandard (zstd) compression algorithm. It is a compressed file that is created with lossless compression by the algorithm. ZST files can be used to compress different types of files such as databases, file systems, networks, and games. The Zstandard is governed by [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) that describes the overall compression mechanism, media type, and content encoding.

## ZST File Format

ZST files are stored in compressed file format to disc. The compression mechanism is as described by RFC 8878 that obsoletes RFC 8478.

## ZST Frames

A ZST file consists of one or more frames. Each frame can be either a Zstandard frame or a skippable frame. A Zstandard frame contains compressed data, whereas a skippable frame contains custom user metadata.

### Zstandard Frame

A Zstandard frame has the following structure.

|Field|Size in Bytes|
---|---|
|Magic_Number	|4 bytes|
|Frame_Header	|2-14 bytes|
|Data_Block	|n bytes|
|[More Data_Blocks]	||
|[Content_Checksum]	|4 bytes|

### Skippable Frame

A skippable frame lets the insertion of user-defined metadata in a flow of concatenated frames. The structure of a skippable frame is as follow.

|Magic_Number	|Frame_Size	|User_Data|
---|---|---|
|4 bytes	|4 bytes	|n bytes|

## References ##

* [RFC 8878 Zstandard Compression](https://www.rfc-editor.org/rfc/rfc8878)
