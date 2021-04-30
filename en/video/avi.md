{
  "date" : "2019-10-11",
  "keywords" : [ "AVI", "Compressed Audio Video", "File", "Extension", "File Format", "Multimedia Container", "XVid", "DivX", "Codecs", "Resource Interchange File Format", "RIFF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AVI File Format - An Audio Video Interleave File",
  "description":"Learn about AVI file format and APIs that can create and open AVI files.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-04-23"
}

## What is an AVI file? ##

The **AVI** file format is an Audio Video multimedia container file format that was introduced by Microsoft. It holds the audio and video data created and compressed using several codecs (Coders/Decoders) such as **XVid** and **DivX**. Since different codecs can be used to encode the AVI contents, the retrieving applications i.e. AVI players, should be able to open these only if they have the required codecs installed with which the AVI contents were created. The format is supported by default on all **Microsoft Windows** platforms as well as on almost all other major platforms. Several applications and APIs provide the capability to create/save, read and convert AVI to other popular formats such as MP4, MOV, WMV, etc.

## AVI File Format ##

A file having a .avi extension is an AVI file. It's a sub-format of the Resource Interchange File Format(RIFF). RIFF organizes data into blocks, or "chunks", that are identified with a FourCC tag. An AVI file is simply one "chunk" in a RIFF formatted file.

In the first sub-chunk, the header of the file is identified by the "hdrl" tag; its contents include the video's width, height, and frame rate. In the second sub-chunk, the motion tag represents the video's frame rate. The AVI video is comprised of the actual audio/visual data in this chunk. There is also a third optional subchunk with the "idx1" tag, which indicates the position within the file of the individual data chunks that belong to the file.

## Brief History ##

AVI was introduced by Microsoft in 1992 with the aim to provide a more robust and advanced audio and video file format. The format quickly became popular with the usage of the internet, allowing individuals to share video files directly and indirectly via cloud-based media storage.

## How to Open/Play AVI files? ##

The following is the list of programs that support AVI files:

 *  Windows Media Player
 *  VLC Media Player
 *  Adobe Premiere Pro
 *  Nullsoft Winamp
 *  CyberLink PowerDirector 365
 *  Xilisoft Video Converter Ultimate
 *  Apple QuickTime Player
 *  Eltima Elmedia Player
 *  olimsoft OPlayer
 *  BIT LABS Simple MP4 Video Player

## References ##

* [AVI - By Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)
* [FileInfo](https://fileinfo.com/extension/avi)
