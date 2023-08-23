{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MPG File Format",
  "keywords" : [ "MPG", "file", "extension", "format", "video format","what is an mpg file format", "mpg file format", "mpg file player","mpeg compression", "video", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Learn about MPG file format and APIs that can create and show that how to open the MPG files.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-07-26"
}

## What is an MPG file format? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. Other extensions such as .m2ts also exist specifying the accurate container, in this case, MPEG-2 TS, but this has little pertinence to MPEG-1 media. The [.mp3](/audio/mp3/) is the most common extension for files containing MP3 audio. An MP3 file is a typical stream of raw audio; the traditional way to tag MP3 files is by writing stream data to "garbage" segments of each frame, which save the media information but are discarded by the **mpg file player**. This is a similar technique used to tag the AAC files, but less supported nowadays.

## MPEG Compression ##

The name MPEG stands for Moving Pictures Experts Group. MPEG is a tool for video compression, which involves the compression of images and sounds, as well as synchronization of the two.
There currently are several MPEG standards.

- MPEG-1 is proposed for intermediate data rates, on the order of 1.5 Mbit/sec.
- MPEG-2 is proposed for high data rates of at least 10 Mbit/sec.
- MPEG-3 was proposed for HDTV compression but was found to be redundant and was merged with MPEG-2.
- MPEG-4 is proposed for very low data rates of less than 64 Kbit/sec.


## Program stream of MPG file format ##

The program stream is a container for multiplexing digital audio, video, and more. The Program Stream format is specified in the 1st part of MPEG-1 (ISO/IEC 11172-1) and 1st part of MPEG-2, Systems (ISO/IEC standard 13818-1/ITU-T H.222.0). The MPEG-2 Program Stream is analog-based and similar to ISO/IEC 11172 Systems layer and forward compatible.

### Coding details ###

Here are the coding details of partial MPEG-2 Program Stream pack header format:

|           Name           |  Number of bits   |                                         Description                                         |
---|---|---|
|        sync bytes        |        32         |                                         0x000001BA                                          |
|       marker bits        |         2         | 01b for MPEG-2 version. The marker bits for the MPEG-1 version are 4 bits with value 0010b. |
|  System clock [32..30]   |         3         |                         System Clock Reference (SCR) bits 32 to 30                          |
|        marker bit        |         1         |                                      1 Bit always set.                                      |
|  System clock [29..15]   |        15         |                                 System clock bits 29 to 15                                  |
|        marker bit        |         1         |                                      1 Bit always set.                                      |
|   System clock [14..0]   |        15         |                                  System clock bits 14 to 0                                  |
|        marker bit        |         1         |                                      1 Bit always set.                                      |
|      SCR extension       |         9         |                                                                                             |
|        marker bit        |         1         |                                      1 Bit always set.                                      |
|         bit rate         |        22         |                              In units of 50 bytes per second.                               |
|       marker bits        |         2         |                                     11 Bits always set.                                     |
|         reserved         |         5         |                                   reserved for future use                                   |
|     stuffing length      |         3         |                                                                                             |
|      stuffing bytes      | 8*stuffing length |                                                                                             |
| system header (optional) |     0 or more     |                       if system header start code follows: 0x000001BB                       |

The following table shows the partial system header format:

|                   Name                    | Number of bytes | Description |
---|---|---|
|                sync bytes                 |        4        | 0x000001BB  |
|               header length               |        2        |             |
|        rate bound and marker bits         |        3        |             |
|           audio bound and flags           |        1        |             |
|    flags, marker bit, and video bound     |        1        |             |
| Packet rate restriction and reserved byte |        1        |             |


## References ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)


