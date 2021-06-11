{
  "date" : "2021-06-11",
  "keywords" : [ "wpl", "wpl file", "extension", "format", "what is a wpl file", "music", "wpl file format"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about WPL file format and APIs that can create, convert and open WPL files.",
  "title" : "WPL - Windows Media Player Playlist File",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-06-11"
}

## What is a WPL file?
A file with .wpl extension contains the playlist of songs to be run on the Microsoft Windows Media Player. These files are usually created by users for their video and audio collections. The content written in a WPL file, is just directory paths or locations for the multimedia files selected by the creator of the .wpl file, so the media player application can promptly find and play the multimedia content from their directory locations.

## WPL File Format
WPL (Windows Media Player Playlist) is a proprietary file format used in Microsoft Windows Media Player versions 9 or greater. It is a computer file format that stores multimedia playlists. By default, the playlist is saved with a .wpl(Windows Media Player Playlist) extension. You can use the [.m3u](/audio/m3u) extension instead, If you want to play your data discs in a device that doesn't support this extension. The elements of a WPL file are represented in XML format. The top-level element "smil" specifies that the file's elements follow the Synchronized Multimedia Integration Language (SMIL) structure. The file is created and saved with the .wpl extension and its MIME type is application/vnd.ms-wpl.

### WPL example
Here is an example of a wpl file:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## References ##

* [MPEG-1 Audio Layer II - By Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

