{
  "date" : "2021-02-26",
  "keywords" : [ "OPUS", "file", "extension", "format", "Audio Coding" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about AAC file format and APIs that can create and open AAC files.",
  "title" : "AAC - Advanced Audio Coding File",
  "linktitle" : "OPUS",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-02-26"
}

## What is an OPUS file?

Opus is an audio file format created by Xiph.Org Foundation and later being standardized by IETS (Internet Engineering Task Force). It has been developed mainly for internet streaming, Voice over IP (VOIP), video conferencing and in-game chat that is why it is designed to retain low-latency while maintaining a real time interactive communication. Keeping the sound quality of an Opus file, many bling listening tests have marked Opus as high quality audio format than any other audio format at any given bitrate.

## Brief History ##

AAC file format is an enhanced version of MP3 with some improvements. Contributed by several companies including the Fraunhofer Institute (Fraunhofer IIS - developers of MP3), Nokia, Dolby, AT&T and Sony, the format was declared as an international standard by Moving Picture Experts Group (MPEG) in Apr, 1997. Later in 1999, the MPEG-2 Part 7 was updated and included in the MPEG-4 family of standards. It was known as MPEG-4 Part 3, identified as ISO/IEC 14496-3: 1999 or MPEG-4 Audio.

## AAC File Format Specifications ##

The AAC file format specifications allow more flexibility to design codec than MP3 does, resulting in more concurrent encoding strategies and efficient compression. The format has been choice of selection by a number of hardware platforms for its improvements over MP3 in terms of providing support for more options even at less bitrates. The AAC file format specifications are available as [MPEG-2 Part 7](https://www.iso.org/standard/43345.html) and [MPEG-4 Part 3](https://www.iso.org/standard/53943.html) (not free to download). The format uses following media types:

* audio/aac
* audio/aacp
* audio/3gpp
* audio/3gpp2
* audio/mp4
* audio/mp4a-latm
* audio/mpeg4-generic

## AAC vs MP3 - Improvements ##

The main differences between AAC and MP3 in terms of improvements are as follow:

* AAC supports a wider range of channels (up to 48) and sampling rates (from 8 kHz to 96 kHz)
* AAC has better coding frequencies above 16 kHz
* AAC has wider limits of variation in the frequency-time resolution of a bank of filters that have lead to improved coding of transients and stationary parts of the audio signal
* More efficient and simple bank of filters: a hybrid filter bank has been replaced by the standard MDCT (modified discrete cosine transform)
* Supports enhanced effectiveness of compression usingTemporal Noise Shaping (TNS), the prediction coefficients of MDCT-time (long term prediction), parametric stereo, perceptual noise substitution, spectral band replication (SBR).
* more flexible joint stereo (different methods can be used in different frequency ranges);

## How to Open/Play AAC files? ##

Despite being MP3 more popular as predecessor of AAC, the lateral enjoys almost equal attention for the reason that it is being used as default audio format for a number of popular video/audio streaming agencies as well as audio hardware. Some popular programs that can open or play such files include:

* Apple iTunes
* VideoLAN VLC media player
* JetAudio
* MediaPlayer Classic

References

* [AAC - By Wikipedia](https://en.wikipedia.org/wiki/Advanced_Audio_Coding)
