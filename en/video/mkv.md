{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MKV File Format",
  "keywords" : [ "mkv", "matroska video", "mkv format", "how to play mkv files" ],
  "description":"Learn about MKV file format and APIs that can create and open MKV files.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2020-17-11"
}

## What is an MKV File? ##

MKV (Matroska Video) is a multimedia container similar to [MOV](/video/mov/) and [AVI](/video/avi/) format but it supports more than one audio and subtitle tracks in the same file. An MKV file is the Matroska multimedia container format used for video. MKV is based on Extensible Binary Meta Language and it supports several video and audio compression formats. The major difference between MKV and other video formats is that MKV is a container and not a codec. MKV files are saved with the .mkv file extension. MKV can incorporate audio, video, and subtitles in a single file even if those elements use different types of encoding. For example, you could have an MKV file that contains H.264 video and MP3 or AAC for audio. MKV also supports descriptions, ratings, cover art, and even chapter points. There are several key features that MKV future proof. These features include:

- Support for Fast seeking.
- Ability to select different audio and video streams.
- Support for subtitles(hard-coded and soft-coded).
- Support for metadata, chapters, and menus.
- Capability to stream online.
- Ability to recover erroneous files that provide the capability to play corrupted files.

## Brief History ##

MKV file originated in 2002 in Russia. The lead developer was Lasse Kärkkäinen who worked with the founder of Matroska, Steve Lhomme, and a team of programmers. MKV was developed as an open standards project, which means that it is open source and free to use. As time went on, the format was improved and became the basis of WebM multimedia format in 2010.

## Matroska Design ##

Matroska adds the following constraints to the EBML specification.

- The **EBML Header**'s **docType** must be 'matroska'.
- The **EBML Header**'s **EBMLMaxIDLength** must be 4.
- The **EBML Header**'s **EBMLMaxSizeLength** must be between 1 and 8 (inclusive).

All the top-level elements are coded on 4 octets.

- Language codes: Matroska (version 1 through 3) used language codes that can be either the 3 letters bibliographic ISO-639-2 form (like "fre" for french), or additional country code could be used like like "fre-ca" for Canadian French. Starting in Matroska version 4, either ISO 639-2 or BCP 47 MAY be used for language codes, although BCP 47 is recommended.
- Physical Types: These have different meaning for both audio and video files. For example, ChapterPhysicalEquiv = 60 means (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) for audio and (DVD / VHS / LASERDISC) for video.
- Block Structure - Block Header: Block header contains information regarding track number, timestamps, type of lacing, etc.
- Lacing: It is a mechanism to save space when storing data that is typically used for small blocks of data (frames). There are 3 types of lacing:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock Structure: It is inspired by the **Block structure** with the main difference being the addition of **Keyframe** and **Discardable** flags. Other than that, everything is the same.

## Matroska Structure ##

A Matroska document must be composed of at least one **EBML Document** using the **Matroska Document Type**. Each **EBML Document** must start with an **EBML Header** followed by the **EBML Root Element** that is defined as a Segment. Matroska defines several Top-Level Elements that may occur within the **Segment**.

EBML uses a system of Elements to compose an EBML Document, The following is the list of Top-Level elements in the Matroska file:

- **EBML Document**: Wrapper for the whole file.
- **EBML Header**: It contains the header information for the file like DocType.
- **Segment**: The top element that contains all other top-level elements.
- **SeekHead**: It contains the position of Segments of other Top-Level Elements.
- **Info**: It contains general information about the Segment.
- **Tracks**: A Top-Level Element of information with many tracks described.
- **Chapters**: It is used to define basic menus and partition data.
- **Cluster**: The Top-Level Element containing the Block structure.
- **Cues**: A Top-Level Element that contains all entries local to the Segment which speed seeking access.
- **Attachments**: This contains attached files.
- **Tags**: This element contains metadata describing Tracks, Editions, Chapters, Attachments, or the Segment as a whole.

The following table shows the structure of the Matroska document with most of the elements displayed in a hierarchy:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| EBML Header | | | |
| Segment | SeekHead| Seek | SeekID |
| | | | SeekPosition |
| | Info | SegmentUID | |
| | | SegmentFilename | |
| | | PrevUID | |
| | | PrevFilename | |
| | | NextUID | |
| | | NextFilename | |
| | | SegmentFamily | |
| | | ChapterTranslate | |
| | | TimestampScale | |
| | | Duration | |
| | | DateUTC | |
| | | Title | |
| | | MuxingApp | |
| | | WritingApp | |
| | Tracks | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | Name |
| | | | Language |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | Video | FlagInterlaced |
| | | | | FieldOrder |
| | | | | StereoMode |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | Color |
| | | | Audio | SamplingFrequency |
| | | | | Channels |
| | | | | BitDepth |
| | Chapters | EditionEntry | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | ChapterAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | ChapterFlagHidden |
| | | | | ChapterDisplay | ChapString |
| | | | | | ChapLanguage |
| | Cluster | Timestamp |
| | | SilentTracks |
| | | Position |
| | | PrevSize |
| | | SimpleBlock |
| | | BlockGroup |
| | | EncryptedBlock |
| | Cues | CuePoint | CueTime |
| | | | CueTrackPositions |
| | Attachments | AttachedFile | FileDescription |
| | | | FileName |
| | | | FileMimeType |
| | | | FileUID |
| | | | FileReferral |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | Tags | Tag | Targets | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |

## How to play MKV files ##

Even though the support for the MKV format has grown rapidly, it is still not an industry standard and not all media players support it. There are two options to play MKV files, downloading a compatible media player, or downloading the codecs for the media player of your preference.

### Compatible video players ###

While the MKV video format is not as common as the MP4, [MOV](/video/mov/), and [AVI](/video/avi/) formats, many media players still support opening and playing MKV files, including:

- VLC
- MPlayer
- KMPlayer
- DivX Player
- MKV File Player
- The Core Media Player

### Using Codecs ###

If you do not want a new media player and prefer to use your existing player, you will need to install some codecs(shorthand for compression/decompression). Even though downloading codecs is a valid option, you should be careful about the source and these may contain malware.

## References ##

- [What Is an MKV File?](https://www.lifewire.com/mkv-file-4135396)
- [What Is an MKV File and How Do You Play Them?](https://www.howtogeek.com/200736/what-is-an-mkv-file-and-how-do-you-play-them/)
- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)
- [Extensible Binary Meta Language](https://tools.ietf.org/id/draft-ietf-cellar-ebml-03.html#:~:text=EBML%20uses%20a%20system%20of,other%20EBML%20Elements%20%2C%20or%20both.)
