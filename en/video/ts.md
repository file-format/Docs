{
  "date" : "2021-12-26",
  "keywords" : [ "TS", "file", "extension", "format", "MPEG-2", "Transport Stream", "video"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TS File Format - What is a .ts file?",
  "description":"Learn about TS file format and APIs that can create and open TS files.",
  "linktitle" : "TS",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2019-09-14"
}

## What is a TS file?

A file with .ts extension is a video stream that stores the data on DVDs. It compresses videos using standard MEPG-2 ([.mpeg](/video/mpg/)) compression algorithm for maximum efficiency and compatibility across different media types such as internet streaming and broadcasting. TS file format was created so that it can be played on devices with poor internet connections, such as smart TV.

## TS File Format - More Information

Data in a TS file is similar to [MP4](/video/mp4/) file, but it is divided into tiny chunks. Each chunk consists of a tiny piece of video, followed by ting bit of audio, and an optional caption. A single TS file consists of many such chunks. In addition to video, audio and caption, each chunk also comprises of some additional data for detecting errors in the chunk. Due to this, TS files are somewhat larger in size.

### Why to use TS File Format?

So, if TS files are somewhat large in size, what advantage does it offer to use them instead of other file formats? Well, in broadcasting, the tiny chunks of video and audio can be sent over the communication media (wired or radio) in real-time. The extra data in the chunks is used by the receiver to skip the error-prone chunks.

In addition, TS files are used because the broadcasting system doesn't need the whole stream to play it. The transmission can be picked up and can be used in real time by assembling audio and video.

## How to Play TS Files?

Well, TS files can be opened and played in popular [VideoLAN VLC media player](https://www.videolan.org/vlc/features.html) which is freely available for download.

## References ##

* [MPEG Transport Stream - Wikipedia](https://en.wikipedia.org/wiki/MPEG_transport_stream)
