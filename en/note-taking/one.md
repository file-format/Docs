{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ONE - Microsoft OneNote File Format",
  "linktitle" : "ONE - Microsoft OneNote File Format",
  "menu" : {
    "docs" : {
      "parent" : "note-taking"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a .ONE file? ##

File represented by .ONE extension are created by Microsoft OneNote application. OneNote lets you gather information using the application as if you are using your draftpad for taking notes. OneNote files can contain different elements that can be placed at non-fixed locations on document pages. These elements may contain text, digitized handwriting, and objects copied from other applications including images, drawings and multimedia (audio/video) clips. Microsoft now offers online version of OneNote as part of Office365 where Notes can be shared with other OneNote users over the internet.

## .ONE File Format Specifications ##

The OneNote file format provides an effective way for representing digital notes as hierarchical sets of sections and pages. Each page contains user-defined content in a specific structure for representation by the file format Document Object Model (DOM). The data model of for this format is as illustrated below.

![Data model of the OneNote File Format](https://i-msdn.sec.s-msft.com/dynimg/IC871934.png "Data model of the OneNote File Format")

### Structure Overview ###

As illustrated in the data model for OneNote file format, a OneNote document consists of different elements.

#### Section ####

A section is the top-most container in a OneNote file that further contains different elements in it like:

* Pages
* Metadata
* Properties

Metadata and properties include the section name, identification of the pages that are contained in the section, and the order in which those pages appear. The term "section" refers to all of the pages that are in a section and the representation of that data in a OneNote® revision store file, which has a .one file name extension. 

#### Page ####

User-defined content in a OneNote document is contained inside a page. Page information includes text, lists, tables, page titles, images and note tags. A page consists of outline objects to which most of the contained objects are added. Each page can be assigned a name for meaningful representation and objects can be added directly to pages as well. A page can further contain sub-pages in a hierarchical system.

#### Properties and Property Sets ####

OneNote contents consist of properties, property sets and file data objects. A property set is a collection of properties that represents some type of content. A file data object is a block of binary data that contains pictures, embedded files or audio/video content.

#### OneNote Notebook ####

A notebook is a collection of section files that are stored in the same directory. A collection of properties is used to specify settings such as order of the sections within the notebook and the color of the notebook.

### File Structure ###

A revision store file MUST begin with a **Header** structure. The remainder of the file is partitioned into blocks of bytes, where the size and structure of each block is specified by the field that references it. A block is reachable if it is referenced by the **Header** structure, or if it is referenced by a field in another reachable block. Data outside the **Header** structure and any reachable blocks MUST be ignored.

All structures are aligned on 1-byte boundaries. All integers are signed unless otherwise specified. All fields are [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) unless otherwise specified.

#### Header ####

The Header of .ONE file comprises of chunks that contain different unique ids and fields for representation of file information as follow:

**guidFileType (16 bytes): **A GUID that specifies the type of the revision store file. MUST be one of the values from the following table.


|#File Format|#Value
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

**guidFile (16 bytes): **A GUID that specifies the identity of this revision store file. SHOULD be globally unique.

**guidLegacyFileVersion (16 bytes): **MUST be "{00000000-0000-0000-0000-000000000000}" and MUST be ignored.

**guidFileFormat (16 bytes): **A GUID that specifies that the file is a revision store file. MUST be "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

**ffvLastCodeThatWroteToThisFile (4 bytes): **An unsigned integer. MUST be one of the values in the following table, depending on the file type.


|#File Format|#Value
|.one|0x0000002A
|.onetoc2|0x0000001B

**ffvOldestCodeThatHasWrittenToThisFile (4 bytes): **An unsigned integer. MUST be one of the values in the following table, depending on the file format of this file.


|#File Format|#Value
|.one|0x0000002A
|.onetoc2|0x0000001B

: **ffvNewestCodeThatHasWrittenToThisFile (4 bytes): **An unsigned integer. MUST be one of the values in the following table, depending on the file format of this file.
:  

(((

|#File Format|#Value
|.one|0x0000002A
|.onetoc2|0x0000001B
)))

**ffvOldestCodeThatMayReadThisFile (4 bytes): **An unsigned integer. MUST be one of the values in the following table, depending on the file format of this file.

(((

|#File Format|#Value
|.one|0x0000002A
|.onetoc2|0x0000001B
)))

**fcrLegacyFreeChunkList (8 bytes): **A **FileChunkReference32** structure  that MUST have a value of "fcrZero".

**fcrLegacyTransactionLog (8 bytes): **A **FileChunkReference32** structure that MUST be "fcrNil".

**cTransactionsInLog (4 bytes): **An unsigned integer that specifies the number of transactions in the transaction log. MUST NOT be zero.

**cbLegacyExpectedFileLength (4 bytes): **An unsigned integer that MUST be zero, and MUST be ignored.

**rgbPlaceholder (8 bytes): **An unsigned integer that MUST be zero, and MUST be ignored.

**fcrLegacyFileNodeListRoot (8 bytes): **A **FileChunkReference32** structure that MUST be "fcrNil".

**cbLegacyFreeSpaceInFreeChunkList (4 bytes): **An unsigned integer that MUST be zero, and MUST be ignored.

**fNeedsDefrag (1 byte): **MUST be ignored.

**fRepairedFile (1 byte): **MUST be ignored.

**fNeedsGarbageCollect (1 byte): **MUST be ignored.

**fHasNoEmbeddedFileObjects (1 byte): **An unsigned integer that MUST be zero, and MUST be ignored.

**guidAncestor (16 bytes): **A GUID that specifies the **Header.guidFile** field of the table of contents file, given by the following table:


|#Table of Contents File Format|#Location of Table of Contents File
|Section File - .One|(((
Table of contents file is located in the same directory as this file.
)))
|Table of Contents File - .onetoc2|(((
Table of contents file is located in the parent directory of this file.
)))

 If the GUID is {00000000-0000-0000-0000-000000000000}, this field does not reference a table of contents file.

**crcName (4 bytes): **An unsigned integer that specifies the CRC value of the name of this revision store file. The name is the Unicode representation of the file name with its extension and an additional null character at the end. This CRC is always calculated using the CRC algorithm for the .one file, regardless of this revision store file format.

**fcrHashedChunkList (12 bytes): **A **FileChunkReference64x32** structure that specifies a reference to the first **FileNodeListFragment** in a hashed chunk list. If the value of the **FileChunkReference64x32** structure is "fcrZero" or "fcrNil", the hashed chunk list does not exist.

**fcrTransactionLog (12 bytes): **A **FileChunkReference64x32** structure that specifies a reference to the first **TransactionLogFragment** structure in a transaction log. The value of the **fcrTransactionLog **field MUST NOT be "fcrZero" and MUST NOT be "fcrNil".

**fcrFileNodeListRoot (12 bytes): **A **FileChunkReference64x32** structure that specifies a reference to a root file node list. The value of the **fcrFileNodeListRoot** field MUST NOT be "fcrZero" and MUST NOT be "fcrNil".

**fcrFreeChunkList (12 bytes): **A **FileChunkReference64x32** structure that specifies a reference to the first **FreeChunkListFragment** structure. If the value of the **FileChunkReference64x32** structure is "fcrZero" or "fcrNil", then the free chunk list does not exist.

**cbExpectedFileLength (8 bytes): **An unsigned integer that specifies the size, in bytes, of this revision store file.

**cbFreeSpaceInFreeChunkList (8 bytes): **An unsigned integer that SHOULD specify the size, in bytes, of the free space specified by the free chunk list.

**guidFileVersion (16 bytes): **A GUID. When either the value of **cTransactionsInLog** field or the **guidDenyReadFileVersion** field is being changed, **guidFileVersion **MUST be changed to a new GUID.

**nFileVersionGeneration (8 bytes): **An unsigned integer that specifies the number of times the file has changed. MUST be incremented when the **guidFileVersion **field** **changes.

**guidDenyReadFileVersion (16 bytes): **A GUID. When the existing contents of the file are being changed, excluding the **Header** structure of the file and unused storage blocks, **guidDenyReadFileVersion** MUST be changed to a new GUID.

**grfDebugLogFlags (4 bytes): **MUST be zero. MUST be ignored.

**fcrDebugLog (12 bytes): **A **FileChunkReference64x32** structure that MUST have a value "fcrZero". MUST be ignored.

**fcrAllocVerificationFreeChunkList (12 bytes): **A **FileChunkReference64x32** structure that MUST be "fcrZero". MUST be ignored.

**bnCreated (4 bytes): **An unsigned integer that specifies the build number of the application that created this revision store file. SHOULD be ignored.

**bnLastWroteToThisFile (4 bytes): **An unsigned integer that specifies the build number of the application that last wrote to this revision store file. SHOULD be ignored.

**bnOldestWritten (4 bytes): **An unsigned integer that specifies the build number of the oldest application that wrote to this revision store file. SHOULD be ignored.

**bnNewestWritten (4 bytes): **An unsigned integer that specifies the build number of the newest application that wrote to this revision store file. SHOULD be ignored.

**rgbReserved (728 bytes): **MUST be zero. MUST be ignored.

## References ##

* [[MS-ONESTORE] - OneNote File Format](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)