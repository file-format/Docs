{
  "date" : "2021-06-09",
  "keywords" : [ "m4p", "mp3", "file", "extension", "format", "what is m4p file format", "music", "m4p file format", "M4b vs MP3", "m4p file format specification"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about M4P file format and APIs that can create, convert and open M4P files.",
  "title" : "M4P - MPEG-4 Audiobook File Format",
  "linktitle" : "M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-06-09"
}

## What is an M4P file?
The file with .m4p extension is an audio file which is usually available at Apple iTunes store for download. On the other words we can say that M4P is an AAC file but copy-protected by using a Digital Rights Management (DRM). It means that M4P files can be played only on authorized systems or devices. Usually M4P files are specific to Apple multimedia devices. So these files can be played only on Apple macbooks, podcasts, smart phones like iPhone 6 or iPhone 7. 

## M4P file format
The M4P stands for MPEG 4 Protected (audio), and it encodes the audio with advanced audio codec (AAC) and protects the file from un-authorized use of the file. This file format is usually considered as an iTunes Music Store's audio file format. Apple uses its FairPlay Digital Rights Management (DRM) system to protect M4P files. FairPlay DRM is based on technology developed by Veridisc. Its protection mechanism works by encrypting the AAC audio stream using the AES encryption. The user receives a master key which is assigned to his account for decryption. This file format was introduced  as a replacement of the MP3 file format, because the MP3 was not originally intended as an audio file, but as layer III in a MPEG 1 or 2 video file.


## M4P file format specification

Similar to [M4A](/audio/m4a/), the M4P files also consist of consecutive chunks. Each chunk has 8 byte header and sub-divided as: 
- 4-byte chunk size (big-endian, high byte first)
- 4-byte chunk type - one of pre-defined signatures: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free",  "skip", "ftyp", "jP2 ", "wide", "load", "imap", "matt", "chap", "kmat", "clip", "crgn", "sync", "tmcd", "PICT", "scpt", "ctab", "ssrc".

Similar to M4A the First chunk in M4P will be of type "ftype" and has a sub-type at offset 8. The M4P defined by sub-type which must be "M4P_".

Iterating chunks, until chunk of unknown type is detected, It will compose M4P (MPEG-4 Audio) file.

## References ##

* [MPEG-4 Part 14 - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A,M4B,M4P) Format & Recovery Example](https://www.file-recovery.com/m4a-signature-format.htm)
