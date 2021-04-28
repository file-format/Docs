{
  "date" : "2021-04-26",
  "keywords" : [ "m4a", "mp3", "file", "extension", "format", "what is m4a file format", "music", "m4a file format", "M4A vs MP3", "m4a file format specification"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about M4A file format and APIs that can create, convert and open M4A files.",
  "title" : "M4A - MPEG-4 Audio File",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-04-26"
}

## What is an M4A file?
The **M4A file format** is an audio file created by using the AAC (Advanced Audio Coding) which is known as a lossy compression. The word M4A abbreviated as MPEG 4 Audio. These audio files usually have .m4a file extension. This is especially true of un-protected content. It may store various types of audio content, such as audiobooks, songs and podcasts. M4A is usually realized as more advanced format than MP3, which had not been typically designed for audio only. It is just an audio layer in MPEG 1 or 2 video files. M4A format is encrypted by FairPlay Digital Rights Management as were sold via the iTunes Store use the .m4p extension. The Apple iPhones use MPEG-4 audio for their ringtones but those audio files use the .m4r extension.


## M4A vs MP3

Both M4A and [MP3](https://docs.fileformat.com/audio/mp3/) are audio-only file formats. 

**M4A**: Better than MP3 in terms of quality and sizes when encoded at the same bit rate. The .m4a file extension is so common because they have been used by Apple for use in the iTunes Music Store. The M4A is an audio file which is compressed using MPEG-4 technology; an algorithm for lossy compression. It is basically associated with “MPEG-4 Audio Layer”, files with .m4a extension are the audio layer of MPEG-4 movies. It is intended to overtake MP3 and become the new standard in audio compression. It is very near to MP3 in many ways but introduced to have a better quality in a same or even smaller file size. The M4A format was first introduced by Apple. The format type is also realized as the Apple lossless Encoder (ALE).

Therefore, currently the M4A couldn't get the MP3’s mainstream success because the audio format is not generally playable yet. It is somehow limited only to MacOS, iPod, and other Apple products.

**Mp3**: The most famous digital audio format. It was also one of first compression formats on the scene and became very popular among music lovers. Its mainstream success is so fast that the file type is capable of being played universally and with almost anything, hardware or software. In a general sense, the M4A will produce better sound quality, but many would argue that, whether it’s true or not, the sound difference is not distinguishable, and it would be a waste of time trying to convert MP3 files into M4A files. Eventually, the conversion will just make you lose the original sound quality.

## M4A file format specification

The M4A files consist of consecutive chunks. Each chunk has 8 byte header and sub-divided as: 
- 4-byte chunk size (big-endian, high byte first)
- 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", "jP2 ", "wide", "load", "ctab", "imap", "matt", "kmat", "clip", "crgn", "sync", "chap", "tmcd", "scpt", "ssrc", "PICT".

First chunk will be of type "ftype" and has a sub-type at offset 8. The M4A defined by sub-type which must be "M4A_", for M4B sub-type must be "M4B_" and for M4P sub-type must be "M4P_".

Iterating chunks, until chunk of unknown type is detected, It will compose M4A (MPEG-4 Audio) file.






## References ##

* [MPEG-4 Part 14 - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Example](https://www.file-recovery.com/m4a-signature-format.htm)
