{
  "date" : "2022-03-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
   "toc" : true,
  "description" : "Learn about WUD file format and APIs that can create and open WUD files.",
  "title" : "WUD File Format - Wii U Disk Image File",
  "linktitle" : "WUD",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2022-03-13"
}

## What is a WUD file?

A file with .wud extension is a disk image created from a Wii U game disc. The resultant disc image file can be loaded by video game emulators such as [Cemu](https://cemu.info/) to emulate the game. WUD files are large in size and are therefore created as multiple segments in order to be transferred easily. The game information is exported as WUD file segments of approximately 2 GB file size. The opening application, like Cemu, needs all these segmented files to be merged into a single WUD file prior to opening these.

## WUD File Format

WUD files are saved to disc in proprietary file format and can be loaded in Cemu emulator to emulate Wii U applications on PC. Due to its large size, WUD files are [compressed](/compression/) to reduce its file size. The resultant compressed file is known as WUX file.

## References

* [Wii U Emulator - Cemu](https://cemu.info/)
* [Cemu - Wikipedia](https://en.wikipedia.org/wiki/Cemu)
