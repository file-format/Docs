{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "PST - Outlook Personal Information Store File Format",
  "description": "Learn about PST file format and APIs that can create and open PST files.",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-pst"
    }
  },
  "lastmod": "2019-09-10"
}

## What is a PST file?

Files with .pst extension represent Outlook Personal Storage Files (also called Personal Storage Table) that store variety of user information. User information is stored in folders of different types that include emails, calendar items, notes, contacts, and several other file formats. PST files are used for archiving emailing data offline that can be later loaded and viewed in various applications.

## PST File Format Specifications

PST File format [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) are available from Microsoft as free and irrevocable free patent licensing through the Open Specification Promise.

### Type of PST Formats

PST file formats are categorised in two types based on the encoding of file type. ANSI encoded PST files are older file formats and are supported by Outlook 2002 and earlier versions only. Such files have a maximum size limit of 2 GB (2^^31^^ Bytes) and do not support Unicode. A more modern file format type, based on Unicode encoding, removes the file size limitation and can reach maximum data size of 50GB.

### Logical Organization of PST File Format

At the base of PST file format lies B-Tree that keeps data sorted and allows searches, sequential access, insertions, deletions etc. in logarithmic time. The overall structure of a PST file is organized in three layers.

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

`Node Database (NDB) Layer` - Node database layer lies at the lower level of a PST file and include database of nodes. These nodes actually represent lower-level storage facilities of the PST file format. NDB layer comprises of header, file allocation information, blocks, and BTrees (Node BTree and Block BTree) from storage point of view. Nodes and Blocks of NDB Layer are linked via Data BID which is one of the four properties of Node reference i.e. NID (Node ID), Parent NID, Data BID (Block BID) and SubNode BID.

`Lists, Tables and Properties Layer -` LTP layer provides the logical understanding of higher-level concepts on top of NDB. Besides other elements, LTP layer mainly comprises of Property Context (PC) and Table Context (TC). PC is a collection of properties, while TC represents a two-dimensional matrix of collection of properties vs. the presence of these. Efficient implementation of PCs and TCs, the LTP layer uses following two types of data structures atop NDB Node:

* Heap On Node (HN) - enables sub-allocating the data stream of a node into small, variable-sized fragments.
* BTree on Heap (BTH) - BTH provides a convenient and practical way of searching through data PCs, described above, are implemented as BTHs and that is why it is implemented by building inside of an HN structure.

`Messaging Layer -` Higher level rules and business logic for working with PST files is implemented at this layer. The logical output of this layer results as Folder objects, Message objects, Attachment objects and Properties which is made possible by combining LTP and NDB layers. Rules and requirements, which need to be followed when modifying the PST contents, are also defined at this layer.

### Physical Organization of PST File Format

High level of file organization of PST file is as shown in the figure below. This is just an overview of different concepts from logical elements of PST file.

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### PST Header Information

The HEADER structure of PST file is located at the very beginning of the file at 0 offset. It contains metadata information about the PST file and the ROOT information to access the NDB Layer data structures described above. The HEADER structure differs for the Unicode and ANSI versions of PST File Format.

The header starts with a 4-bytes magic word **!BDN** represented by bytes (0x21, 0x42, 0x44, 0x4E). Another 2-bytes magic number, **SM** (0x53, 0x4D),  is located at offset 8 from the start of file. Version information (ANSI or Unicode) lies at an offset of 10 from start of file. Hex value (0x17) specifies Unicode PST file while 0x0E or 0x0F represents ANSI file format.

|Field|Description
---|---|
|dwMagic      (4 bytes)|MUST be "{ 0x21, 0x42, 0x44, 0x4E } ("!BDN")"
|dwCRCPartial (4 bytes)|The 32-bit CRC  value of the 471 bytes of data starting from wMagicClient (0ffset 0x0008)
|wMagicClient (2 bytes)|MUST be "{ 0x53, 0x4D }".
|wVer         (2 bytes)|File format version. This value MUST be 14 or 15 if the file is an ANSI PST file, and MUST be 23 if the file is a Unicode PST file.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. Creators of a new PST file based on this document SHOULD initialize this value to 19.
|bPlatformCreate (1 byte)|This value MUST be set to 0x01.
|bPlatformAccess (1 byte)|This value MUST be set to 0x01.
|dwReserved   (8 bytes)|
|bidUnused    (8 bytes Unicode only)|Unused padding added when the Unicode PST file format was created.
|bidNextP     (Unicode: 8 bytes; ANSI: 4 bytes)|Next page BID. Pages have a special counter for allocating bidIndex values. The value of bidIndex for BIDs for pages is allocated from this counter.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. For more details, see section 2.2.2.2.
|dwUnique     (4 bytes)|This is a monotonically-increasing value that is modified every time the PST file's HEADER structure is modified. The function of this value is to provide a unique value, and to ensure that the HEADER CRCs are different after each header modification.
|rgnid[]      (128 bytes)|A fixed array of 32 NIDs, each corresponding to one of the 32 possible NID_TYPEs (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE,NID_TYPE_ASSOC_MESSAGE)
|qwUnused     (8 bytes)|Unused space; MUST be set to zero. Unicode PST file format only.
|root         (Unicode: 72 bytes; ANSI: 40 bytes)|A ROOT structure (section 2.2.2.5).
|dwAlign      (4 bytes)|Unused alignment bytes; MUST be set to zero. Unicode PST file format only.
|rgbFM        (128 bytes)|Deprecated FMap. This is no longer used and MUST be filled with 0xFF. Readers SHOULD ignore the value of these bytes.
|rgbFP        (128 bytes)|Deprecated FPMap. This is no longer used and MUST be filled with 0xFF. Readers SHOULD ignore the value of these bytes.
|bSentinel    (1 byte)|MUST be set to 0x80.
|bCryptMethod (1 byte)|Indicates how the data within the PST file is encoded. MUST be set to one of the pre-defined values (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbReserved  (2 bytes)| Reserved; MUST be set to zero.
|bidNextB     (8 bytes)|Indicates the next available BID value. Unicode PST file format only.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. For more details, see section 2.2.2.2.
|dwCRCFull    (4 bytes)|The 32-bit CRC value of the 516 bytes of data starting from wMagicClient to bidNextB, inclusive. Unicode PST file format only.
|ullReserved  (8 bytes)|Reserved; MUST be set to zero. ANSI PST file format only.
|dwReserved   (4 bytes)|Reserved; MUST be set to zero. ANSI PST file format only.
|rgbReserved2 (3 bytes)|
|bReserved    (1 byte) |
|rgbReserved3 (32 bytes) |

### Data Protection ###

For security, PST files can also be password protected which requires the loading application to apply password before it can be viewed. Password applied to the PST file is stored in message store. However, this does not provide strong data protection as the password can be removed by available tools. Also, user specified password is not used as part of key for encoding and decoding cipher algorithms. Thus, there is no benefit of protecting data to be accessed by un-authorized parties. Storage of password as CRC-32 hash of the original string also makes it a weak method for data security against brute-force approach.

## References ##

* [Outlook Personal Folders (.pst) File Format](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Personal Folder File Format Specifications](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
