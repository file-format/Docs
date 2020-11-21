{
  "date" : "2020-17-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Matroska",
  "keywords" : [ "matroska", "multimedia container format" ],
  "description":"Matroska is a multimedia container format that is based on EBML (Extensible Binary Meta Language)",
  "linktitle" : "Matroska",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2020-17-11"
}

## What is a Matroska Format? ##

Matroska is a multimedia container format that is based on EBML (Extensible Binary Meta Language), a binary derivative of [XML](/web/xml/). Due to EMBL, Matroska gains significant advantages in terms of future format extensibility along with backward compatibility.

## Brief History ##

The project originated in 2002 in Russia with Lasse Kärkkäinen as the lead developer. He worked with Steve Lhomme (founder of Matroska), and a team of programmers. Matroska Multimedia Container was developed as an open standards project, which means that it is open source and free to use. With the passage of time, the format was improved and in 2010, it became the basis of WebM multimedia format.

## Features ##

As Matroska is designed with the future in mind, it provides the following features:

- Fast seeking in the file
- Support for chapters, menus, and metadata.
- Selectable subtitle/audio/video streams
- Modularly expandable
- Recovery of erroneous files that enables playback of corrupted files.
- Online streaming capability.

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

## References ##

- [Matroska by Wikipedia](https://en.wikipedia.org/wiki/Matroska)
- [Matroska.org](https://www.matroska.org/)
- [Extensible Binary Meta Language](https://tools.ietf.org/id/draft-ietf-cellar-ebml-03.html#:~:text=EBML%20uses%20a%20system%20of,other%20EBML%20Elements%20%2C%20or%20both.)
