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

### Limitations  ###

* Aspect ratio information cannot be encoded in the original AVI specification, although the later OpenDML specification (AVI 2.0) offers a standardized method
* Although AVI files are widely used in film and television post-production, various approaches to adding a time code to them are competing, affecting the format's usability.
* A video file encoded in AVI cannot use a compression technique that requires future frames data beyond the frame being encoded (B-frame)
* It is problematic to use AVI files with variable bitrates (VBR) (such as MP3 audio at sample rates below 32 kHz)
* An AVI file encoding standard definition feature films as normally used is likely to incur overhead of about 5 MB per hour, depending on how the file is used
* Subtitles must be hardcoded into the video stream or distributed in a separate file in case AVI files cannot accommodate attachments such as fonts and subtitles

## Brief History ##

AVI was introduced by Microsoft in 1992 with the aim to provide a more robust and advanced audio and video file format. The format quickly became popular with the usage of the internet, allowing individuals to share video files directly and indirectly via cloud-based media storage.

## References ##

* [AVI - By Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)
