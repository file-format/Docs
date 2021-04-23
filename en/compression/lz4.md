{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LZ4 - LZ4 Compressed File Format",
  "description":"Learn about LBR file format and APIs that can create and open LZ4 files.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-19"
}

## What is an LZ4 file?

A file with .lz4 extension is a compressed archive file created with applications/utilities that support [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)) compression. The LZ4 algorithm focuses on trade-off between speed and compression ratio. Compressed LZ4 archives can be created using the LZ4 command-line utility and can be decompressed using the same.

## LZ4 File Format

The LZ4 file format, based on the LZ4 compression algorithm, is independent of CPU type, operating system, file system and character set. It is suitable for file compression and streaming compression using the LZ4 algorithm. The initial implementation of the LZ4 format was carried out in [C](/programming/C/) language by Yann Collet in 2011 and is available for developer's reference on [Github](https://github.com/lz4/lz4).

### LZ4 Frame Format

The general structure of LZ4 file format is as shown below.

|MagicNb|F. Descriptor|	Block|(...)|EndMark	|C. Checksum|
---|---|---|---|---|---|
|4 bytes|	3-15 bytes|||			4 bytes|	0-4 bytes|

#### Magic Number

4 Bytes, Little endian format. Value : 0x184D2204

#### Frame Descriptor

The frame descriptor consists of 3 t0 15 bytes and is the most important part of the specifications. Together, the Magic_Number and Frame_Descriptor fields are referred to as LZ4 Frame Header, and its size varies between 7 and 19 bytes. It is as shown below.

|FLG|	BD|	(Content Size)|	(Dictionary ID)|	HC|
---|---|---|---|---|
|1 byte|	1 byte|	0 - 8 bytes|	0 - 4 bytes|	1 byte|

#### Data Blocks

Each data block follows the following order.

|Block Size|	data|	(Block Checksum)|
---|---|---|
|4 bytes|		|0 - 4 bytes|

#### EndMark

The flow of blocks ends when the last data block is followed by the 32-bit value 0x00000000.

#### Content Checksum

The Content_Checksum verifies the validity of the content being decoded correctly and is carried out using the result of xxHash-32 algorithm. It validates the results of successful transmission of all blocks in the correct order and without any error.

## How to open LZ4 file?

LZ4 files can be opened using the [LZ4](http://lz4.github.io/lz4/) utility that is available as open source for developer's reference.

## References

* [LZ4 Frame Format](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [LZ4 Compression Algorithm - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))
