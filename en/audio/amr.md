{
  "date" : "2021-04-29",
  "keywords" : [ "amr", ".amr", "file", "extension", "format", "what is an amr file", "music", "amr file format", "amr file","convert amr file to mp3", "play amr file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about AMR file format and APIs that can create, convert and open AMR files.",
  "title" : "AMR - Adaptive Multi-Rate Codec File",
  "linktitle" : "AMR",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-04-29"
}

## What is an AMR file?
The file with .amr extension is an audio data format relevant to **Adaptive Multi-Rate** audio codec; consists of a multi-rate narrowband speech codec which encodes narrowband signals at 4.75-12.2 kbit/s bit rate with toll quality speech starting at 7.4 kbit/s; uses link adaptation to select from one of eight different bit rates based. 

## AMR File Format
AMR file format uses many coding techniques, the ACELP (Algebraic Code Excited Linear Prediction) algorithm one of the best technique; designed for compressing human spoken audio in a more efficient way. The AMR was set as the standard voice or speech codec by 3GPP in 1999. The AMR file format is also used to store the spoken audio by using **Adaptive Multi-Rate** audio codec which is used by many smart phones to store recorded speeches.

### File format structure
The AMR( Adaptive Multi-Rate ) is an audio format; widely used in various mobile applications and devices, typically in audio player/recorder or in VoIP kind of applications. AMR can be further classified as:

1. AMR-NB( NarrowBand )
2. AMR-WB( WideBand )

Usually, AMR refers to AMR-NB. The AMR file format has the following structure:

Each AMR file contains a 6-byte header that recognize the file as an AMR audio. This header is always set to:
- 0x23
- 0x21
- 0x41
- 0x4D
- 0x52
- 0x0A

This is usually simialr across all AMR-NB files. If the header following a standard, it is likely that the file is corrupted and should not be used. the AMR file consists of a whole number of packed frames of audio. These frames each compose 20ms of audio. Each frame can be encoded using any of the valid AMR-NB modes (0-7, 8 SID in DTX mode). Since, the frames can be encoded at different bit rates, this typical method is called Adaptive Multi-Rate(AMR). 
#### AMR modes
Following are the different AMR modes and their corresponding bitrates:

|MODE| BIT RATES|
---|---|
|0| AMR 4.75 - Encodes at 4.75kbit/s|
|1 | AMR 5.15 - Encodes at 5.15kbit/s|
|2 | AMR 5.9 - Encodes at 5.9kbit/s|
|3 | AMR 6.7 - Encodes at 6.7kbit/s|
|4 | AMR 7.4 - Encodes at 7.4kbit/s|
|5 | AMR 7.95 - Encodes at 7.95kbit/s|
|6 | AMR 10.2 - Encodes at 10.2kbit/s|
|7 | AMR 12.2 - Encodes at 12.2kbit/s|

Frame size of AMR modes in bytes (including the header byte) are given below:

|CMR |MODE |FRAME SIZE( in bytes )|
---|---|---|
|0 |AMR 4.75 |13|
|1 |AMR 5.15 |14|
|2 |AMR 5.9 |16|
|3 |AMR 6.7 |18|
|4 |AMR 7.4 |20|
|5 |AMR 7.95 |21|

## References

* [Adaptive Multi-Rate audio codec - By Wikipedia](https://en.wikipedia.org/wiki/Adaptive_Multi-Rate_audio_codec)
* [RTP Payload Format and File Storage Format for AMR and AMR-WB Audio  codecs](https://tools.ietf.org/html/rfc4867#page-35)
