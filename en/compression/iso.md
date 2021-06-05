{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ISO - Disk Image File Format",
  "description":"What is an ISO file and APIs that can create and open ISO files.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-19"
}

## What is an ISO file?

A file with .iso extension is an uncompressed archive disk image file that represents the contents of entire data on an optical disc such as CD or DVD. Based on the [ISO-9660](https://www.iso.org/standard/17505.html) standard, the ISO image file format contains the disc data along with the filesystem information that is stored in it. The capability of ISO files to contain an exact replica of the content makes it the perfect file type for creating copies of CDs/DVDs and are mostly used to store bootable data for installation. Most of the times, ISO files are burnt to USB/CD/DVD as bootable content for booting the machine for installation. ISO files have MIME type application/x-iso9660-image.

## ISO File Format

ISO file format is not like other container file file formats although it archives the specified contents of data. The archive is created as a binary file with the exact structure of the content and filesystem information. The ISO file format is described by the [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) as follow.

### Top Level Structure of ISO File

The overall structure of the file consists of:

 * `System Area` - 32,768 bytes and is unused by ISO_9660
 * `Data Area` - consists of Volume descriptor set and Path tables, directories and files

### Volume Descriptor Set

The data area starts with the volume descriptor set, a set of one or more volume descriptors terminated with a volume descriptor set terminator. These collectively act as a header for the data area, describing its content (similar to the BIOS parameter block used by FAT, HPFS and NTFS formatted disks).

A volume descriptor set is as shown below.

|Volume Descriptor Set|
---|
|Volume descriptor #1|
|...|
|Volume descriptor #N|
|Volume descriptor set terminator|

#### Volume Descriptor

Each volume descriptor is 2048 bytes in size and has the following structure:

|Part	|Type	|Identifier	|Version	|Data|
---|---|---|---|---|
|Size	|1 byte	|5 bytes (always 'CD001')	|1 byte (always 0x01)	|2,041 bytes|

## References

* [Optical Disk Image - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [File Signatures](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)
