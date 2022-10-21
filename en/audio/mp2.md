{
  "date" : "2021-06-11",
  "keywords" : [ "mp2", "mp2 file", "extension", "format", "what is an mp2 file", "music", "mp2 file format"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MP2 file format and APIs that can create, convert and open MP2 files.",
  "title" : "MP2 - MPEG Layer 2 Audio File Format",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-06-11"
}

## What is an MP2 file?

An MP2 file which is also called as MPA file is an Audio file compressed with Layer II of MPEG-1 or MPEG-2; a lossy audio compression format defined by ISO/IEC 11172-3 alongside MPEG-1 Audio Layer I and MPEG-1 Audio Layer III ([MP3](/audio/mp3/)), to reduce the audio file size. Whereas, MP3 is more popular than MP2 because of its smaller size and availability over the internet. Therefore MP2 is still a vital standard for audio broadcasting.

## MP2 File Format

MPEG Audio Layer II (MP2) is the core algorithm of the MP3 standards. MPEG-1 Audio Layer 2 encoding was obtained from the MUSICAM audio codec. It started as the Digital Audio Broadcast (DAB) project in Germany as a part of the EUREKA research program. The Eureka 147 contained three main elements: Transmission Coding & Multiplexing, COFDM Modulation and MUSICAM Audio Coding (Masking pattern Universal Sub-band Integrated Coding And Multiplexing). The MUSICAM was one of the few encodings which was able to achieve high audio quality at bit rates in the range of 64 to 192 kbit/s per monophonic channel. The goal was to provide low delay, low complexity, error robustness, short access units and fulfill the technical requirements of broadcasting, telecommunication and recording on digital storage media.

MP2 is a sub-band audio encoder, which can compressed in the time domain with a low-delay filter bank generating 32 frequency domain components. By comparison, MP3 is a transform audio encoder with hybrid filter bank, which means that compression applied in the frequency domain after a hybrid transformation from the time domain. The MP2 encoder may exploit inter channel redundancies using optional "joint stereo" intensity encoding.

### MP2 File Format Specifications

The MP2 file format is based on successive digital frames of 1152 sampling intervals with four possible formats:

- mono format
- stereo format
- intensity encoded joint stereo format (stereo irrelevance)
- dual channel (uncorrelated) format
Some important technical specifications of MP2 are given in the table below:

|Specification| Description|
---|---|
|**Sampling rates**|  32, 44.1 and 48 kHz|
|**Bit rates**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 and 384 kbit/s|
|**Additional sampling rates**|16, 22.05 and 24 kHz|
|**Additional bit rates**|8, 16, 24, 40 and 144 kbit/s|
|**Multichannel support**|Up to 5 full range audio channels and an LFE-channel (Low Frequency Enhancement channel)|

## References ##

* [MPEG-1 Audio Layer II - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)
