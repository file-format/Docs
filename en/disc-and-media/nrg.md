{
  "date": "2021-08-16",
  "keywords": [
    "nrg file",
    "nrg file format",
    "what is a nrg file",
    "file",
    "nrg example",
    "nrg file extension",
    "extension",
    "format",
    "nrg footer",
    "file format of nrg",
    "Nero Burning Rom",
    "Nero AG"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about NRG file format and APIs that can create and open NRG files.",
  "title": "NRG - Disk Image File Format",
  "linktitle": "NRG",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nrg"
    }
  },
  "lastmod": "2021-08-16"
}

## What is an NRG file?

An image file format that is created by the use of an optical disc is considered an NRG file format. This format is specifically created by Nero for the utility of Nero Burning Rom. For the storage of disc images, this format is considered to be used as it is appropriate for these specific files. These files could be in the form of an exact copy of a CD or DVD or may have several files that can be mounted as a disk. Other more popular file formats like [ISO](/compression/iso/) file formats are those into which these files can be converted to some basic utilities. Mostly, the NRG files are used to create backups or copies of some important data or discs.

## NRG File Format ##

This file format was developed by Nero AG as a disk image format. It had the specific property of Nero Burning Rom utility as it was developed to store disc images. Its first version was specified to store values as 32-bit integers. However, its second version was launched and contained support for 64-bit integers.

## Technical Specification ##

At the beginning of the file, this format does not store its data as a header. Like a footer, it is attached at the end of the file. In the form of chunks of IFF, the information of the image is stored. The offset of the first chunk can be obtained by reading the NRG footer at the last 8 bytes to 12 bytes of the file. In all versions of NRG file format, there are chunks, DAOI, CD text, session information media type, disc information, Relo, and end of the chain attached with it. The byte order is big-endian and all integer values are unsigned at the time of storage.

### Main Chunks ###

#### Cue Sheet ####

This cue sheet is available easily in all the NRG files format versions. The chunk of **CUEX** means the blocks of fixed-size concatenation and each of these represents the cue point. 

#### DAO Information ####

This information is also present in all the NRG format versions. The chunks of **DAOI** store the relevant specific info in 2 parts. Its first part consists of the session-specific data only. Its second part just repeats the grey information related to tracking and it is only once for every track. 

#### CD-text ####

This is available in NRG’s second version. The chunk of **CDTX** consists of the CD-text pack's raw concatenation having 18 bytes for each.

#### Extended Track Information ####

This is available in every version of the file format of NRG. These chunks are utilized for storing the tracking information for the at once sessions track. This data is repeated only once in the case of each track. 

#### Session Information ####

This is also available in every version of the file format of NRG. The information of session chunks needs to be utilized for scanning the session’s image quickly and then track count. 

#### End of chain ####

The chunk of end means the signals that now there are not any more chunks that need to be read and this is also available in NRG's all versions.


## References ##

* [NRG - by Wikipedia](https://en.wikipedia.org/wiki/NRG_(file_format))

