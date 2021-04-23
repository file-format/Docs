{
  "date" : "2021-04-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PEA - PeaZip Archive File Format",
  "description":"Learn about PEA file format and APIs that can create and open PEA files.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-21"
}

## What is a PEA file?

A file with .pea extension, acronym for Pack, Encrypt, and Authenticate, is a [zip](/compression/zip/) archive created with [PeaZip](https://peazip.github.io/) archiving software application. It features compression and multiple volume output, and offers a flexible security model through Authenticated Encryption and cryptography. This provides both privacy and authentication of the data. The PeaZip utility is available as open-source engine that can be compiled for different OS as per requirements.

## PEA File Format

The [PEA file format specifications](https://peazip.github.io/pea_help.pdf) are publicly available for developer's reference. PEA archives are binary files with flexible security model and redundant integrity checks ranging from checksums to cryptographically strong hashes. This defines three different levels of communication to control:

 * Streams - the actual output data stream that is formed by multiple input files and can be written written to multiple output volumes
 * Objects - input files and folders sent to .pea archive
 * Volumes - output archive file that can be spanned to user defined size

Each one of these are optional and can be incorporated as per user requirements. The PEA file format can store a single stream containing unlimited objects. Each stream is up to 2^64 bytes in size.

PEA files offer optional integrity check and authenticated encryption using AES in EAX or HMAC mode, alternatively Twofish and Serpent in EAX mode.

### PEA Archive Header

The archive header is 10 bytes and is structured as follow.

|Bytes|Description|
---|---|
|1 | Magic byte field for file format disambiguation: $EA|
|1 | Version Number|
|1 | Revision Number|
|1 | Volume control scheme|
|1 | Declaring the OS where the stream was built|
|1 | Declaring OS date and time encoding|
|1 | Declaring objects name character encoding|
|1 | Declaring CPU type (encoded in 7 bit) and endianness (in msb)|
|1 | Reserved for future use|

## How to open PEA file?

Some of the software applications that can open PEA files include:

 * PeaZip

## References

* [PEA File Format Specifications](https://peazip.github.io/pea_help.pdf)
* [PEA File Format](https://peazip.github.io/pea-file-format.html#.pea_specifications)
