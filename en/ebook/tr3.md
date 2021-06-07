{
  "date" : "2021-04-10",
  "keywords" : [ "TR3", "File", "Extension", "File Format", "eBook", "TomeRaider", "Yadabyte" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about TR3 file format and APIs that can create and open TR3 files.",
  "title" : "TR3 - TomeRaider 3 eBook File",
  "linktitle" : "TR3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-04-10"
}

## What is a TR3 file? ##

TR3 file is a TomeRaider 3 eBook that provides support for fast searching and compression. That can function properly through TomeRaider related program. Yadabyte is the developer of this software, a British software, and web development company based in the UK. The TomeRaider eBook reader application can be used for proper functioning and managing the content of these TR3 files. This related eBook reader can be installed in computers running on Microsoft Windows-based systems and many transferrable gadgets. TR3 file belongs to the group of eBook Files used in operational systems such as Windows 10, Windows 7, Windows 8 / 8.1, Windows Vista, Windows XP. 

TR3 specific [HTML tags](http://www.yadabyte.com/TR3Tutorial/TR3_tag.htm) are as follow:

|Tag|Description|
---|---|
|\<new> |To create TomeRaider files from text files, the New tag is all that is needed. <new> tag defines the start of the pages.|
|\<CATDEF> ... \</CATDEF> |defines the category name|
|\<META> ... \</META> |is a tag used to define all of the metadata used in the file format. This tag includes a number of parameters.|
|\<EXPMSG> |This tag controls the message that appears when a file has expired. Whenever a user attempts to view a page after the file has expired, the expiration message appears instead of the actual page text.|
|\<DIEMSG> |This tag is similar to EXPMSG. It is used to display a message when the file dies.|
|\<ENGMSG> |This tag is used to create the message that displays for encrypted pages. The message appears instead of the page text if the user attempts to open an encrypted page before unlocking it.|
|\<expmsg>,\<diemsg> and \<encmsg> |Ignored within the page text. They must be placed in the file header section before the first <new> tag.|
|\<SELECTION> . \</ SELECTION> |Used to support Query's. This tag must be before the first <new> tag. It compiles the selection data for the user's query.|
|\<catset>. \</catset>| Used to assign category names for each subject.|


## Problems to open a TR3 file ##

Here is the list of some common issues which may arise and cause misfunctioning of the file format:

 *	Corrupt file
 *	Infected File due to virus
 *	Improper links to the TR3 file in archive accesses
 *	No access right in the system to open the files
 *	Outdated drive in your system
 *	Removal of  the report of the TR3 from the Windows archive
 *	Contacting the developer may be a better option for better output
