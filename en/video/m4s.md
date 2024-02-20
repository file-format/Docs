{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "M4S File - What is an M4S file?",
  "description": "Learn about M4S file format and APIs that can create and open M4S files.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4s"
    }
  },
  "lastmod": "2022-07-18"
}

## What is an M4S file?

An M4S file is a small segment of a video that is streamed over the internet using the **MPEG-DASH** streaming technique. It contains a video segment in the form of binary data. The receiving application (usually a web browser or media players) plays these segments in the order they are received. The first M4S segment is identified by the initialization data that it contains. In **summary**, M4S files are small individual media segments of a complete file.

## M4S File Format

M4S files are based on the [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). These small segments of a large file can be downloaded independently via HTTP. Thus, if you have a large [MP4](/video/mp4/) movie file, it can be streamed using the MPEG-DASH (Dynamic Adaptive Streaming over HTTP) technique by segmenting it as M4S segment files. If this large movie file is downloaded to disc as M4S, multiple M4S files are downloaded. If all these .m4s segments are concatenated, a complete playable file is produced. The media players can't play the file unless the first initialization segment is also available with the file.

## About MPEG-DASH Streaming

MPEG-DASH uses adaptive bitrate streaming technique that makes it possible to stream high quality media content over the internet. This is done by breaking the content into a sequence of small segments that are streamed over HTTP. Large media files such as movie, podcasts, or live broadcast of a sports event can be streamed this way. These segments are encoded at different bit rates. The MPEG-DASH enabled media players automatically selects the segment with the highest bit rate using a bit rate adaptation algorithm. This avoids stalling or re-buffering events in the playback.

### Open-Source API for M4S files

There are open source APIs available that can be used to read and convert M4S files.

 * [libdash](https://github.com/bitmovin/libdash) - .NET API for M4S files
 * [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - Javascript client for M4S file
 * [Go Library for creating Dash Files](https://github.com/zencoder/go-dash)

### Open-Source API to Convert M4S to MP4

 * [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## References ###

* [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamic Adaptive Streaming over HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)
