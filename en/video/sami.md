{
  "date": "2023-05-16",
  "keywords": [
    "sami file",
    "what is a sami file",
    "example of sami file",
    "file",
    "sami file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "SAMI File Format - Subtitles And Metadata Interchange File",
  "description": "Learn about SAMI format and APIs that can create and open SAMI files.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
      "parent": "video"
    }
  },
  "lastmod": "2023-05-16"
}

## What is a SAMI file?

A file with the extension ".sami" typically refers to a Subtitles And Metadata Interchange (SAMI) file. SAMI is a captioning format used for displaying subtitles or closed captions in videos. It was originally developed by Microsoft for their Windows Media Player.

SAMI files contain timing information and text content for subtitles or closed captions, allowing them to be synchronized with a video playback. The format supports basic formatting options such as font style, color, and positioning of the subtitles on the screen.

SAMI files are usually plain text files and can be opened and edited using a text editor. The contents of a SAMI file typically include a header section that provides information about the file, followed by individual subtitle entries with their respective timing and text.

Here's an example of what a SAMI file might look like:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI files are commonly used in conjunction with video players or media players that support subtitle display, such as Windows Media Player or VLC Media Player. The player reads the SAMI file and synchronizes the subtitles with the video content, allowing viewers to read the captions while watching the video.

## Supported HTML tags

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI>:`` The root element that encapsulates the entire SAMI file.
- ``<HEAD>:`` Contains header information for the SAMI file.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- ``<FONT>:`` Defines font properties for the enclosed text. Attributes like Color, Face, Size, and Style can be used to modify the font appearance.
- ``<BR>:`` Inserts a line break within a subtitle.
- ``<B>:`` Renders the enclosed text in bold.
- ``<I>:`` Renders the enclosed text in italics.
- ``<U>:`` Renders the enclosed text underlined.
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

These are some of the basic tags supported by SAMI files. It's important to note that SAMI does not support the full range of HTML tags and attributes. The supported tags are primarily focused on styling and positioning the subtitles rather than providing extensive document structuring or interactivity.

## References
* [SAMI](https://en.wikipedia.org/wiki/SAMI)
