{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "QT File Format - Quick Movie File",
  "description":"Learn about QT file format and APIs that can create and open QT files.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-02-16"
}

## What is a QT file?

A file with .qt extension is a multimedia container file that is used by QuickTime framework to store multimedia file contents. Developed by Apple Inc. the QuickTime File Format (QTFF) is a multimedia container file that contains audio, video, or text for playback later on. It is the format of choice for the exchange of digital media between devices, applications, and operating systems. QT files are also saved in [MOV](/video/mov/) format that was also developed by Apple Inc. Some of the applications that can open QT files include Apple QuickTime player, VLC media player, and Media Player Classic with K-Lite Codec Pack.

## QT File Format

The QTFF is object-oriented that exposes of a flexible collection of objects for ease of parsing and expansion. Each track in a QT file contains a digitally-encoded media stream or a data reference to the media stream located in another file. The hierarchical data structure consisting of objects called atoms act as tracks containers. File format specifications for [QT file format](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html) are officially available by Apple Inc for developer's reference.

### Media description

Media description of a QuickTime file is stored separately from the media data. Information such as the number of tracks, video compression format, and timing information are stored in the media description (also known as movie resource, movie atom, or simply the movie). The media data is referenced by an index in this media structure. The media data is the actual sample data, such as video frames and audio samples, used in the movie.

### Atoms

Atom is the basic unit of QuickTime file. There are two major fields in any atom before any other field: Size and Type fields. Size field shows the size of the atom while the type field indicates the type of data stored in the atom. By nature, atoms are hierarchical which means that one atom can contain other atoms which can still contain others. The layout of a sample atom is shown in the following image.

Each atom has two parts, header and data. The header contains the size and type fields and data part contains the actual data. Further each field is explained below:

#### Atom Size

The atom’s header and contents are indicated by a 32 bit integer known as the size of the atom. The size field contains the size of the atom in bytes, expressed in a 32 bit unsigned integer.

#### Atom Type

Type of the atom is also shown by a 32-bit integer, which is mostly treated as a four-character field with knemonic value, such as ‘moov’ (0x6D6F6F76) for a movie atom, or ‘trak’ (0x7472616B) for a track atom. Once atom type is known, it allows interpreting its data.

![A Sample Atom](https://library.conholdate.app/view/OAZhVkEkm1IKa8LM0/qtsampleatom.png "QT File Format")

## File Structure ##

QT/MOV files consist of consecutive chunks. Every chunk has an 8 byte header: 4-byte chunk size (big-endian, high byte first) and 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". First chunk is of type "ftype" and has a sub-type at offset 8. MOV defined by sub-type which must be "qt ". To compose MOV file, iterating chunks is needed until unknown type is detected.

Here is a sample example: Inspecting a sample mov file’s binary data it is evident that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **qt~_~_** (hex: 71 74 20 20) which points to MOV file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. At offset 32 (hex: 20) is located the second chunk, which has a size of 8 and type **mdat** (hex: 6D 64 61 74).

The next chunk is located at offset 32+8#40 (hex: 28) and has a size 3,263,028 (hex: 00 31 CA 34) and type **mdat** (hex: 6D 64 61 74) at offset 44 (hex: 2C). The next chunk is located at offset 40 + 3,263,028#3,263,068 (hex: 00 31 CA 5C) and has a size 21,189 (hex: 00 00 52 C5) and type **moov** (hex: 6D 6F 6F 76) at offset 1,836,019,574 (hex: 00 31 CA 60). This is the last chunk, so total file size is 3,263,068+21,189#3,284,257 bytes.

## References ##

* [QT File Format - Apple Inc.](https://developer.apple.com/library/archive/documentation/QuickTime/QTFF/QTFFPreface/qtffPreface.html)
* [QuickTime File Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)
