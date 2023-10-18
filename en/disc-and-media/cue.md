{
  "date" : "2021-06-09",
  "keywords" : [ "cue", "file", "extension", "format", "what is a cue file", "music", "cue file format", "cue file format specification", "cue sheet", "CDRWIN"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about CUE file format and APIs that can create, convert and open CUE files.",
  "title" : "CUE - Cue Sheet File",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2021-07-01"
}

## What is a CUE file?

A file with .cue extension, also known as cue sheet file, is a metadata file that contains information about the layout of tracks on a CD or DVD. These are supported by media players and optical disc authoring applications. The main audio data stored on the CD is referenced by the cue file, along with the specifications of track lengths, disc titles, and performers. Thus if a single audio file contains multiple tracks, the cue file can be used to divide the audio into multiple files or reference various tracks.

## CUE File Format

CUE or cue sheet files are stored in plain text format that is human-readable. Information in a cue file are commands with one or more parameters. These commands either apply to the whole file or to an individual track, depending on the particular command and the context. The CDRWIN user guide describes the specifications for the cue sheet syntax and semantics.

## CUE Sheet Essential Commands

|Command|Description|
---|---|
|FILE| Refers to the file containing the data and its format such as [MP3](/audio/mp3/), [WAV](/audio/wav/), or plain binary disc image)|
|TRACK| Defines the track context information such as its number and type or mode.|
|INDEX| Represents the position as an index within the FILE. The format is mm:ss:ff (minute-second-frame).|
|PREGAP and POSTGAP|This indicates the pregap or post-gap of a track, which is not stored in any data file. The length is specified in the same minute-second-frame format as for INDEX.|

### CUE Sheet Example

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```

## Other CUE files

Here are other file types that use the **.cue** file extension.

**Disk and Media**
- [CUE - Cue Sheet File](/disc-and-media/cue/)
- [CUE - CDRWIN Cue Sheet](/disc-and-media/cue-cdrwin/)

## References

* [.cda file - By Wikipedia](https://en.wikipedia.org/wiki/.cda_file)
