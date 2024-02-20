{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 - Microsoft OneNote File Format",
  "description": "Learn about ONETOC2 file format and APIs that can create and open ONETOC2 files.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc2"
    }
  },
  "lastmod": "2019-09-10"
}

## What is ONETOC2? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

When you create a notebook in OneNote 2016, it’s automatically saved in the new 2010-2016 file format. You’ll need this format if you want all the features in OneNote 2016, like math equations and linked notes, to work properly.

## ONETOC2 File Format ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### File Structure ###

A revision store file MUST begin with a **Header** structure. The remainder of the file is partitioned into blocks of bytes, where the size and structure of each block is specified by the field that references it. A block is reachable if it is referenced by the **Header** structure, or if it is referenced by a field in another reachable block. Data outside the **Header** structure and any reachable blocks MUST be ignored.

All structures are aligned on 1-byte boundaries. All integers are signed unless otherwise specified. All fields are [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7) unless otherwise specified.

#### Header ####

The Header of .ONE file comprises of chunks that contain different unique ids and fields for representation of file information as follow:

`guidFileType (16 bytes):` A GUID that specifies the type of the revision store file. MUST be one of the values from the following table.

|File Format|Value
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` A GUID that specifies the identity of this revision store file. SHOULD be globally unique.

`guidLegacyFileVersion (16 bytes):` MUST be "{00000000-0000-0000-0000-000000000000}" and MUST be ignored.

`guidFileFormat (16 bytes):` A GUID that specifies that the file is a revision store file. MUST be "{109ADD3F-911B-49F5-A5D0-1791EDC8AED8}".

`ffvLastCodeThatWroteToThisFile (4 bytes):` An unsigned integer. MUST be one of the values in the following table, depending on the file type.

|File Format|Value
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatHasWrittenToThisFile (4 bytes):` An unsigned integer. MUST be one of the values in the following table, depending on the file format of this file.


|File Format|Value
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` An unsigned integer. MUST be one of the values in the following table, depending on the file format of this file.
:  


|File Format|Value
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` An unsigned integer. MUST be one of the values in the following table, depending on the file format of this file.


|File Format|Value
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## References ##

* [[MS-ONESTORE] - OneNote File Format](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)
* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)
