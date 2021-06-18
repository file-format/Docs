{
  "date" : "2021-06-09",
  "keywords" : [ "m4b", "mp3", "file", "extension", "format", "what is m4b file format", "music", "m4b file format", "M4b vs MP3", "m4b file format specification"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about M4B file format and APIs that can create, convert and open M4B files.",
  "title" : "M4B - MPEG-4 Audiobook File Format",
  "linktitle" : "M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-06-09"
}

## What is an M4B file?
The file with .m4b extension is an audiobook generally used by Apple books and iTunes. The Audio used in this format is stored in MPEG-4 and compressed by using AAC encoding. An M4B file is very similar to M4A but having support the audiobook related features, such as bookmarking and chapter breaks. The M4B files are available in both DRM enabled and DRM free versions. DRM encryted audiobooks are usually paid audiobooks from iTunes Store. Whereas, DRM free can be found easily over the internet.

## M4B file format
The audiobook files containing metadata, images, bookmarks and hyperlinks can be saved with .m4a extension but generally .m4b extension is used while saving, just to specify that the file has an audiobook file format. Fairplay DRM (Digital Rights Management) is used by apply to protect their M4B files. So the files downloaded from iTunes can be played only on authorized devices or computers.


## M4B vs M4A

Both M4B and [MP3](https://docs.fileformat.com/audio/mp3/) are audio-only file formats. 

**M4B**: Wins when compared to MP3 in terms of quality if encode both at the same bit rate. The M4B is an audiobook file which is compressed using AAC encoding. It is basically associated with “MPEG-4 Audio Layer”, files with .m4b extension are the audio layer of MPEG-4 movies but with extra audiobook related features. Its goal is to overtake MP3 and become the new standard in audio compression. It is very close to MP3 in many ways but developed to have a better quality in a same or even smaller file size. The M4B format was first introduced by Apple. The format type is also realized as the Apple lossless Encoder (ALE).

Therefore, currently the M4B couldn't get the MP3’s mainstream success because the audio format is not commonly playable yet. 

**Mp3**: A digital audio format which is well familiar to everyone. A very first compression format on the scene and became very famous among music listeners. Its mainstream success is so rapid that the file type is being able to be played universally and compatible with almost anything, hardware or software. In a general sense, the M4A will produce better sound quality, but many would argue that, whether it’s true or not, the sound difference is not comparable, and it would be a waste of time trying to convert MP3 files into M4A files. Finally, the conversion will just make you lose the original sound quality.

## M4B file format specification

Similar to [M4A](/audio/m4a/), the M4B files also consist of consecutive chunks. Each chunk has 8 byte header and sub-divided as: 
- 4-byte chunk size (big-endian, high byte first)
- 4-byte chunk type - one of pre-defined signatures: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", "skip", "jP2 ", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt", "ssrc".

Similar to M4A the First chunk in M4B will be of type "ftype" and has a sub-type at offset 8. The M4B defined by sub-type which must be "M4B_".

Iterating chunks, until chunk of unknown type is detected, It will compose M4B (MPEG-4 Audio) file.

## References ##

* [MPEG-4 Part 14 - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Example](https://www.file-recovery.com/m4a-signature-format.htm)
