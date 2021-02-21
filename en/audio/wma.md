{
  "date" : "2021-02-20
  ",
  "keywords" : [ "WMA", "file", "extension", "format", "audio interchange file format", "music" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about WMA file format and APIs that can create and open WMA files.",
  "title" : "WMA - Windows Media Audio File",
  "linktitle" : "WMA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-02-20"
}

## What is a WMA file?

A file with .wma extension represents an audio file that is saved in the Advanced Systems Format (ASF) format. ASF is Microsoft's proprietary format that contains bitstreams encoded by Windows Media Audio 9. In addition to the the audio content, a WMA file also contains metadata objects such as title, album, artist, and genre of the track. WMA files are primarily used for streaming over the web similar to [.mp3](/audio/mp3/) files.

## WMA File Format

A WMA file is binary file format and is contained in the ASF file format. It specifies the encoding of metadata about the file similar to the ID3 tags used by the MP3 files. The WMA codec has bene in use by Microsoft in its Protected Interoperable File Format (PIFF) since 2008. However, it has not been declared as standardized audio codec by the related industry standards such as DECE UltraViolet and MPEG-DASH.

### WMA Type Specific Data

The type-specific information for the Windows Media Audio codec is stored in the following format as part of the Type-Specific Data of the Stream Properties Object.

```
struct WMA_TYPE_SPECIFIC_DATA
{
    WAVEFORMATEX wfx;
    DWORD        dwSamplesPerBlock;
    WORD         wEncodeOptions;
    DWORD        dwSuperBlockAlign;
};
```
## References

* [ASF Overview - Microsoft](https://docs.microsoft.com/en-us/windows/win32/wmformat/overview-of-the-asf-format?redirectedfrom=MSDN)
*
