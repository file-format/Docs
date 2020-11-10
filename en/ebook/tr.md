{
  "date" : "2019-12-12",
  "keywords" : [ "TR", "file", "extension", "format", "E-Book", "Digital book" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about TR file format and APIs that can create and open TR files.",
  "title" : "TR - TomeRaider EBook File Format",
  "linktitle" : "TR",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2020-11-12"
}

## What is a TR file?

A file with a .tr extension is TomeRaider 2 e-book file that is created with TomeRaider eReader software. These files can be opened on both Windows and Handheld devices such as Android, Palm OS, and EPOC, and are categorized as text files. The TomeRaider software developed by [Yadabyte](http://www.yadabyte.com/index.php) website and the official website provides more information about the TR files. The TR2 file format was replaced by TR3 (TomeRaider 3) format. TR files offer fast searching and high compression levels.


## Brief History

TomeRaider was developed by a UK based software and web development company Yadabyte in 1999. The company took it further to TomeRaider version 3.

## TR File Format

The latest release of TR file format is version 3 that provides support for fast searching and compression. It compresses text files to 45-60% of the original size. This enables TomeRaider ebook reader to perform fast searching, indexing and compression. The TR file format is suitable for large reference documents and most documents require a DRM key for being encrypted. TR specific [HTML tags](http://www.yadabyte.com/TR3Tutorial/TR3_tag.htm) are as follow.

|Tag|Description|
---|---|
|\<new> |This is the cornerstone of the TR file. The New tag defines new sections within the file. It is all that is needed to turn any text file into a TomeRaider file. <new> tag defines start of the pages.|
|\<CATDEF> ... \</CATDEF> |defines the category name|
|\<META> ... \</META> |is a tag used to define all of the metadata used in the file format. There are lots of parameters used with this tag.|
|\<EXPMSG> |This tag is used to create the message that displays after the file has been expired. Any text after this tag will be included in the expiration message. When the user tries to view any page after the file has been expired, the actual page is replaced by this message just before display. So, the user sees the expiration message instead of the actual page text.|
|\<DIEMSG> |This tag is similar to EXPMSG. It is used to display a message after the file has died.|
|\<ENGMSG> |This tag is used to create the message that displays for encrypted pages. If the user tries to view an encrypted page without having unlocked the file, this message is displayed instead of the actual page text.|
|\<expmsg>,\<diemsg> and \<encmsg> |Ignored within the page text. They must be placed in the file header section before the first <new> tag.|
|\<SELECTION> . \</ SELECTION> |Used to support Query's. This tag must be before the first <new> tag. It precompiles the selection data that will appear when the user queries the selection.|
|\<catset>. \</catset>| Used to assign category names for each subject.|

## References

* [TR Tags - Yadabyte](http://www.yadabyte.com/TR3Tutorial/TR3_tag.htm)
