{
  "date" : "2019-10-11",
  "keywords" : [ "mov file", "mov file format", "what is an mov file", "file", "mov example", "mov file extension","extension", "format", "QuickTime", "MPEG-4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MOV File Format - Quick Movie File",
  "description":"Learn about MOV file format and APIs that can create and open MOV files.",
  "linktitle" : "MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-07-29"
}

## What is a MOV file?

MOV or QuickTime file format is a multimedia container which is developed by Apple: contains one or more tracks, each track holds a particular type of data i.e. Video, Audio, text, etc. MOV format is compatible both in Windows and Macintosh systems. MOV uses MPEG-4 coded for compression and tracks are maintained in objects called atoms which are placed in a hierarchical data structure.

## Brief History

MPEG-4 file format has evolved from QuickTime format specification in 2001, which has also been approved by the International Organization for Standardization. MPEG-4 Part 1 systems specification was published in 1999 but in 2001 a revision file format [MP4](/video/mp4/) was published. MP4's first version was revised in 2003 as MPEG-4 Part 14 (ISO/IEC 14496-14:2003). In 2004 MP4 was generalized to define a general structure for all time-based media files. Therefore, now it is used as a basis for various other multimedia file formats.

## QuickTime File Format

In order to work with digital multimedia, QTFF can hold many kinds of data. As it can describe any kind of media structure so QTFF is an ideal format for the exchange of digital media. The file format consists of a flexible collection of object-oriented objects. For the storage of movies on disks, QuickTime uses two structures i.e. atoms and QT atoms.  

### Atoms

Atom is the basic unit of the QuickTime file. There are two major fields in any atom before any other field: Size and Type fields. The size field shows the size of the atom while the type field indicates the type of data stored in the atom. By nature, atoms are hierarchical which means that one atom can contain other atoms which can still contain others. The layout of a sample atom is shown in the following image.

Each atom has two parts, header, and data. The header contains the size and type fields and the data part contains the actual data. Further, each field is explained below:

### Atom Size

The atom’s header and contents are indicated by a 32-bit integer known as the size of the atom. The size field contains the size of the atom in bytes, expressed in a 32-bit unsigned integer.

### Atom Type

The type of the atom is also shown by a 32-bit integer, which is mostly treated as a four-character field with knemonic value, such as ‘moov’ (0x6D6F6F76) for a movie atom, or ‘trak’ (0x7472616B) for a track atom. Once atom type is known, it allows interpreting its data.

### QT Atoms and Atom Containers

QT atoms provide a general-purpose storage format and have an extended header consisting of Size, Type, Atom ID, and Count of Child atoms fields. QT atoms are wrapped in an atom container, a unique data structure having a header with a lock count. There is one root atom in each atom container which is the QT atom. The layout of the QT atom is shown in the figure below.

QT atom container header has the following data:

Reserved: A 10-byte element with a value of 0.

Lock Count: 16-bit integer with a value of 0.

QT atom headers have the following data:

**Size -** QT atom header and contents are indicated in bytes by a 32-bit integer. In the case of a leaf atom, then this field contains the size of a single atom.

**Type -** Type of the atom is indicated by a 32-bit integer. In case it is the root atom, then the value is set to ‘sean’.

**Atom ID -** It’s a 32-bit integer that shows the atom ID and must be unique for all siblings. Root atom always the value of atom ID as 1.

**Reserved -** A 16-bit integer that must be set to 0.

**Child count -** A 16-bit integer that indicates the number of child atoms of an atom.

**Reserved -** A 32-bit integer that must be set to 0.

## File Structure

MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV defined by sub-type which must be "qt ". To compose MOV file, iterating chunks is needed until unknown type is detected.

Here is a sample example: Inspecting a sample MOV file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. The first block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. At offset 32 (hex: 20) is located the second chunk, which has a size of 8 and type **mdat** (hex: 6D 64 61 74).

The next chunk is located at offset 32+8#40 (hex: 28) and has a size 3,263,028 (hex: 00 31 CA 34) and type **mdat** (hex: 6D 64 61 74) at offset 44 (hex: 2C). The next chunk is located at offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) and has a size 21,189 (hex: 00 00 52 C5) and type **moov** (hex: 6D 6F 6F 76) at offset 1,836,019,574 (hex: 00 31 CA 60). This is the last chunk, so total file size is 3,263,068+21,189#3,284,257 bytes.

## References

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)
