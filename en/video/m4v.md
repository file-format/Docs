{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "M4V",
  "linktitle" : "M4V",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2019-09-14"
}

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection aiming to protect privacy or copy. Videos and audio tracks are wrapped around by container files to achieve indexing and organizing the streams for playback. In addition, containers also provide the feature of chapters similar to those on DVDs. M4V is used by Apple to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used for the purchase of the video. However, if DRM-protection is removed from M4V files, then these files can be played in other video players by just changing the extension from .m4v to .mp4 and that’s the reason that M4V files are associated with MPEG-4. M4V uses H.264 for video and **[AAC](/audio/aac/)** and Dolby Digital for audio encoding and decoding.

## M4V File Structure ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V defined by sub-type which must be "M4V_". Further chunks type are predefined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT". Iterating chunks, until unknown type is detected, we compose M4V file.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. At offset 32 (hex: 20) is located the second chunk, which has a size of 30,322 (hex: 00 00 76 72, big-endian, lower-byte first) and type **moov** (hex: 6D 6F 6F 76). The next chunk is located at offset 32+30,322#30,354 (hex: 00 00 76 92) and has a size 8 (hex: 00 00 00 08) and type **free** (hex: 66 72 65 65).

### Codecs Used in M4V ###

#### Video Codec H.264 ####

H.264 is a video compression standard that converts digital video into a format that requires less space when required transmission or storage. M4V uses H.264 for video compression. Its application ranges from DVD, TV, Videoconferencing, and video streaming over the internet. H.264 consists of two main parts: Encoder – Which compresses the video, Decoder – Which uncompress the compressed video back. In the figure below, encoding and decoding processes are highlighted along with other processes covered in the H.264 standard.

##### Video Coding and Decoding Process in H.264 #####

For the compressed H.264 bitstream, video encoder conducts the prediction, transformation and encoding process while the decoder carries out the inverse process of decoding, inverse transform, and reconstruction to produce back the video file. H.264 takes half the size of the MPEG.

#### Audio Codec ####

Advanced Audio Coding (AAC) is an audio codec for lossy digital audio compression and is used in M4V container. AAC is the successor of the [MP3](/audio/mp3/) format and achieves better quality than MP3 with the same bitrate. AAC format throws away some information during the compression process which is of less importance. AAC is a variable bitrate (VBR) block-based codec where each block decodes to 1024 time-domain samples.

### References ###

* [https:~~/~~/en.wikipedia.org/wiki/M4V](https://en.wikipedia.org/wiki/M4V)
* [https:~~/~~/en.wikipedia.org/wiki/H.264/MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)
* [https:~~/~~/www.vcodex.com/an-overview-of-h264-advanced-video-coding/](https://www.vcodex.com/an-overview-of-h264-advanced-video-coding/)
