{
  "date" : "2019-12-09",
  "keywords" : [ "zip file", "zip file format", "what is a zip file", "file", "zip example", "zip file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ZIP",
  "description":"What is a ZIP file and APIs that can create and open ZIP files.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2019-12-09"
}

## What is a ZIP file? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the ZIP file size. ZIP file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKZIP](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made ZIP file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## Brief History of ZIP File Format

The history fo ZIP file format dates back to the event of lawsuite fielded by System Enhancement Associates (SEA) against PKWARE for using its ARC utility without permissions for its trademark and the copyrights of product's appearance and user interface. Prior to this, Phil Katz, had rewritten SEA's source code and released PKXARC, an ARC extractor, and PKARC, a file compressor, as freeware for MS-DOS based systems. Losing to the lawsuit, PKWARE couldn't use the anything related to ARC anymore. This is where the creation of a new file compression came into being, named as ZIP which was made part of PKZIP utility at PKWARE, Inc.

Katz released the ZIP file format specifications into the public domain, while retaining the proprietary rights over his compression and extraction utility i.e. PKZIP. The ZIP compression system was (and is) able to archive files in a folder by means of a 32-bit cyclic redundancy check ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) algorithm to compress file sizes. Unlike ARC, .ZIP folders included a directory file that played the role of a cryptographer's code book, holding the information necessary to render the compressed files.

## Supported Compression Methods in ZIP

As per .ZIP File Format specifications, the following compression methods are supported.

* Store - implies no compression
* Shrink
* Reduction (This implies compression factors ranging from level 1 to level 4)
* Implode
* Deflate
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd version I, Rev 1

DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## ZIP File Format Specifications

ZIP files have capability to store multiple files using different compression techniques while at the same time supports storing a file without any compression. Each file is stored/compressed individually which helps to extract them, or add new ones, without applying compression or decompression to the entire archive.

### Overall ZIP File Format

Each Zip file is structured in the following manner:


|ZIP File format
---|
|Local File Header 1
|File Data 1
|Data Descriptor 1
|Local File Header 2
|File Data 2
|Data Descriptor 2
|      ....
|      ....
|Local File Header N
|File Data N
|Data Descriptor N
|Archive Decryption Header
|Archive Extra Data Record
|Central Directory

ZIP file format uses 32-bit CRC algorithm for archiving purpose. In order to render the compressed files, a ZIP archive holds a directory at its end that keeps the entry of the contained files and their location in the archive file. It, thus, plays the role of encoding for encapsulating information necessary to render the compressed files. ZIP readers use the directory to load the list of files without reading the entire ZIP archive. The format keeps dual copies of the directory structure to provide greater protection against loss of data.

Each file in a ZIP archive is represented as an individual entry where each entry consists of a Local File Header followed by the compressed file data.The Directory at the end of archive holds the references to all these file entries. ZIP file readers should avoid reading the local file headers and all sort of file listing should be read from the Directory. This Directory is the only source for valid file entries in the archive as files can be appended towards the end of the archive as well. That is why if a reader reads local headers of a ZIP archive from the beginning, it may read invalid (deleted) entries as well those are not part of the Directory being deleted from archive.

The order of the file entries in the central directory need not coincide with the order of file entries in the archive.

### ZIP File Entries

Entries in ZIP file are arranged one after another where each entry consists of:

* Local File Header
* Optional Extra Data Fields
* User data (optionally compressed/optionally encrypted)

The Local File Header of each entry represents information about the file such as comment, file size and file name.  The extra data fields (optional) can accommodate information for extensibility options of the ZIP format.

#### Local File Header

The Local File Header has specific field structure consisting of multi-byte values. All the values are stored in little-endian byte order where the field length counts the length in bytes. All the structures in a ZIP file use 4-byte signatures  for each file entry. The end of central directory signature is 0x06054b50 and can be distinguished using its own unique signature. Following is the order of information stored in Local File Header.


|Offset|Bytes|Description
---|---|---|
|0|4|Local file header signature # 0x04034b50 (read as a little-endian number)
|4|2|Version needed to extract (minimum)
|6|2|General purpose bit flag
|8|2|Compression method
|10|2|File last modification time
|12|2|File last modification date
|14|4|CRC-32
|18|4|Compressed size
|22|4|Uncompressed size
|26|2|File name length (n)
|28|2|Extra field length (m)
|30|n|File Name
|30+n|m|Extra Field

#### Central Directory File Header


|Offset|Bytes|Description
---|---|---|
|0|4|Central directory file header signature # 0x02014b50
|4|2|Version made by
|6|2|Version needed to extract (minimum)
|8|2|General purpose bit flag
|10|2|Compression method
|12|2|File last modification time
|14|2|File last modification date
|16|4|CRC-32
|20|4|Compressed size
|24|4|Uncompressed size
|28|2|File name length (n)
|30|2|Extra field length (m)
|32|2|File comment length (k)
|34|2|Disk number where file starts
|36|2|Internal file attributes
|38|4|External file attributes
|42|4|Relative offset of local file header. This is the number of bytes between the start of the first disk on which the file occurs, and the start of the local file header. This allows software reading the central directory to locate the position of the file inside the ZIP file.
|46|n|File name
|46+n|m|Extra field
|46+n+m|k|File comment

#### End of Central Directory Record


|Offset|Bytes|Description
---|---|---|
|0|4|End of central directory signature # 0x06054b50
|4|2|Number of this disk
|6|2|Disk where central directory starts
|8|2|Number of central directory records on this disk
|10|2|Total number of central directory records
|12|4|Size of central directory (bytes)
|16|4|Offset of start of central directory, relative to start of archive
|20|2|Comment length (n)
|22|n|Comment

## References

* [PKWARE ZIP File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Structure of PKZip File](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)
