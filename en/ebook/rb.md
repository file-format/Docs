{
  "date": "2021-03-08",
  "keywords": [
    "RB",
    "Nuvo Media’s Rocket eBook device",
    "file",
    "extension",
    "format",
    "eBook"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about RB file format for Nuvo Media’s Rocket eBook device and APIs that can create and open RB files.",
  "title": "RB - Rocket eBook File",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-rb"
    }
  },
  "lastmod": "2021-03-08"
}

## What is an RB file?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Although Rocket eBook is capable of displaying images, but only in black and white display. It has a screen of 106 dpi or 480 x 320 pixels on a 4.5 x 3-inch touch screen. The Rocket eBook connects to a computer via a serial port connection to download eBooks in RB file format. The RB files are capable to use DRM but this technology is not being used in modern eBooks. The RB file conventionally contains an HTML file with the images and a pseudo-OPF file with all of the metadata (.info).

## Technical Specification of RB File Format ##

A magic number (in hex) appears in the file's first 4 bytes: B0 0C B0 0C.

It appears that the next two bytes are a version number, like "02 00", which stands for major version 2 and minor version 0.

The next four bytes contain the text "NUVO", followed by 4 bytes of 00h.

The next 4-byte is the date when the book was created, encoded as an int16. This puts us at offset 0Eh. ORocketLibrary's old version encoded the year's full value (i.e., 1999 was "CF 07", 2000 was "D0 07"). In the recent version, tm_year is stored verbatim, i.e. 100 for year 2000 ("64 00"). After the year comes an int8 representing the 1-relative month number, and an int8 representing the day of the month.

The next 6 bytes are 00h. For time setting, these may be reserved.

The absolute offset of the "Table of Contents" is contained in an int32 at offset 18h.

After this is an int32 containing the length of the .rb file. This is used to determine whether the files are complete or not.

This whole chunk of bytes (20h to 128h) appears to be needed only by a title that is encrypted. In non-encrypted titles, they are always zero.

In most cases, the table of contents follows (at offset 128). It begins with an int32 count of the number of "page" entries (.rb-file sections) in the ToC. Each entry consists of a name (zero-padded to 32 bytes), followed by 3 int32s: the length of the data segment, the position in the .rb file, and a flag for this entry. As of today, the known values are: 1 (encrypted), 2 (information page), and 8 (deflated). The names are all tailored, as necessary, to ensure they are all unique.

## References

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)
