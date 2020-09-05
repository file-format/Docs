{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OST - Outlook Storage File Format",
  "description":"Learn about OST file format and APIs that can create and open OST files.",
  "linktitle" : "OST",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is an OST file? #

OST or Offline Storage Files represent user's mailbox data in offline mode on local machine upon registration with Exchange Server using Microsoft Outlook. It is automatically created on the first use of Microsoft Outlook upon connectivity with server. Once the file is created, the data is synchronized with the email server so that it is available offline as well in case of disconnectivity from email server. OST files can user mailbox items such as emails, contacts, calendar information, notes, tasks and other similar data. Users can create emails and other data items in OST file even in the absence of connection to the server, but these will not be synchronized with the server. Once the connection is established, the local file is synchronized with the server again so that both the server and the local copy are at the same level of information.

## OST File Format ##

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* 32-bit ANSI Format
* 64-bit Unicode Format

PST File format [specifications](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx), as available from Microsoft, are also applicable to OST file format as free and irrevocable patent licensing through the Open Specification Promise. It consists of following distinguishable elements:

* file header
* file header data
* index branch node
* index leaf node
* (file) offset index
* (item) descriptor index
* local descriptors
* item table type

### Header Information ###

The HEADER structure of OST file is located at the very beginning of the file at 0 offset. It contains metadata information about the OST file and the ROOT information to access the NDB Layer data structures described above. The HEADER structure differs for the Unicode and ANSI versions of OST File Format.

The header starts with a 4-bytes magic word **!BDN** represented by bytes (0x21, 0x42, 0x44, 0x4E). Another 2-bytes magic number, **SM** (0x53, 0x4D),  is located at offset 8 from the start of file. Version information (ANSI or Unicode) lies at an offset of 10 from start of file. Hex value (0x17) specifies Unicode OST file while 0x0E or 0x0F represents ANSI file format.

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

### References ###

* [Outlook Personal Folders (.ost) File Format](https://msdn.microsoft.com/en-us/library/ff385210(v#office.12).aspx)
* [Personal Folder File Format Specifications](https://github.com/libyal/libpff/blob/master/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
