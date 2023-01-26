{
  "date" : "2023-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about ISZ file format and APIs that can create and open ISZ files.",
  "title" : "ISZ File Format - Zipped ISO Disk Image",
  "linktitle" : "ECM",
  "menu" : {
    "docs" : {
      "identifier":"disc_and_media-ecm",
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2023-01-25"
}

## What is an ISZ file?

ISZ is a file format used for storing disk images, similar to ISO or NRG. The ISZ format is a compressed version of the ISO format, which reduces the file size of the image while still maintaining the exact contents of the original image. ISZ files can be used to create backups of CDs, DVDs, or other optical media, or to store and distribute software and other types of data.

An ISZ file can be opened and mounted as a virtual drive using a program such as UltraISO, Alcohol 120%, or ISOBuster. These programs allow the user to access the contents of the ISZ file as if they were on a physical disk. The files in the ISZ file can also be extracted and used directly.

It is worth to note that ISZ is not a widely used format and not all the tools can open it. Also, depending on the type of image you're trying to open, there are other more popular image formats like ISO, BIN/CUE and NRG that are more widely supported.

## Difference between ISZ and ISO

ISZ and ISO are both file formats used to store and distribute digital media.

An ISO file is a type of image file that contains a complete copy of the data on a CD, DVD, or other disc. It is often used to distribute software and games, as well as to create backups of optical media. ISO files can be opened and used like a physical disc, and can be burned to a CD or DVD.

An ISZ file, on the other hand, is a type of compressed image file that is similar to an ISO file, but uses a different compression method called "zisofs". This method is designed to compress the data on the disc, making the resulting ISZ file smaller than the equivalent ISO file. ISZ files can also be used like a physical disc, but they need to be decompressed before they can be used.

So ISZ files are compressed version of ISO, but they can't be used directly, it needs to be decompressed before using it.

## How to open ISZ file?

To open an ISZ file, you will need a program that is capable of decompressing the file and mounting it as a virtual disc.

One such program is UltraISO, which is a commercial software specifically designed for working with ISO and ISZ files. It allows you to open, edit, and extract the contents of an ISZ file. It can also convert ISZ files to ISO or other disc image formats.

Another program that can open ISZ files is MagicISO. This is also a commercial software and it also allows you to open, edit, and extract the contents of an ISZ file, and convert it to other disc image formats.

There are also several free alternatives such as Daemon Tools Lite, Gizmo Drive, and Virtual CloneDrive. These programs allow you to mount ISZ files as virtual discs, allowing you to access their contents as if they were on a physical disc.

You can also use the command line tool 'zisofs-tools' to decompress the ISZ file to ISO.

## References
* [UltraISO](https://www.ultraiso.com/)
