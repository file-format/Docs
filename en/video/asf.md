{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ASF - Advanced Systems File Format",
  "description":"Learn about ASF file format and APIs that can create and open ASF files.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-02-16"
}

## What is a ASF file?

A file with .asf extension is a multimedia file format for storing and playing digital media streams over the network. It is a container file format that can have both video and audio content for streaming online. You will rarely find ASF files, and more probably come across the Windows Media Audio ([WMA](/audio/wma/)) and Windows Media Video ([WMV](/audio/wmv/)) files that both specify ASF files having content encoded with respective codecs. Windows media files can be created and read using the Windows Media Format SDK.

## ASF File Format

An ASF file can comprise of multiple independent or dependent streams. This can include multiple audio streams for multichannel audio, or multiple bitrate video streams. The multiple bitrate lets the streams suitable for transmission over different bandwidths. Moreover, the streams in an ASF file can be in compressed or uncompressed format. The best compression is achieved with the Microsoft Windows Media Audio and Video 9 Series codecs. Complete specifications of ASF file format are available on [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF Top-Level File Structure

ASF files logically contain three types of top-level objects:

* `Header Object` - mandatory and must be placed at the beginning of every ASF file
* `Data Object` - mandatory and must follow the header object
* `Index Object(s)` - optional, but useful in providing time-based random access into ASF files

The following image shows the top-level file structure of ASF files.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Top-Level Header Object

The Header object provides a well-known byte sequence at the beginning of the ASF files and can optionally contain metadata such as bibliographic information. It contains all the information that is required to properly interpret the information within the data object. The Header Object may include a number of standard objects including, but not limited to:

 * File Properties Object - Contains global file attributes.
 * Stream Properties Object - Defines a digital media stream and its characteristics.
 * Header Extension Object - Allows additional functionality to be added to an ASF file while maintaining backward compatibility.
 * Content Description Object - Contains bibliographic information.
 * Script Command Object - Contains commands that can be executed on the playback timeline.
 * Marker Object - Provides named jump points within a file.

The Header Object is represented using the following structure.

|Field name	|Field type	|Size (bits)|
---|---|---|
|Object ID|	GUID|	128|
|Object Size|	QWORD|  	64|
|Number of Header Objects|	DWORD|  	32|
|Reserved1|	BYTE|	8|
|Reserved2|	BYTE|	8|

#### ASF Top-Level Data Object

All the digital media data for an ASF file is contained in the data object and is stored in the form of ASF data packets. Each data packet is of a fixed length and contains data for one or more digital media streams.

#### ASF Top-Level Index Objects

ASF top-level index objects has the following two types:

 * `Simple Index Object` - Contains a time-based index of the video data in an ASF file. The time interval between index entries is constant and is stored in the Simple Index Object.
 * `Index Object` - Refers to the Index Object, the Media Object Index Object, and the Timecode Index Object, whose formats are all similar. The Index Object, like the Simple Index Object, indexes by time with a fixed time interval, but is not limited to video streams.

## References

* [ASF File Format - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime File Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)
