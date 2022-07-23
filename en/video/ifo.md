{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "IFO File - What is an IFO file?",
  "description":"Learn about IFO file format and APIs that can create and open IFO files.",
  "linktitle" : "IFO",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2022-07-12"
}

## What is an IFO file?

A .ifo file is an information file that is part of DVD specifications. The acronym IFO stands for information. IFO files provide information about the contents of the disc to the DVD player such as about the video files, menus, subtitles, and any special features that the DVD may have. This is the file that tells the DVD player what to display when the menu appears, the start of different chapters in the DVD, and the location and time of the video and audio files on the DVD. VLAN VLC Player can open IFO files.

IFO files are saved with **.ifo** extension.

## IFO File Format - More Information

IFO files are saved as text files and can be opened with any text editor such as Microsoft Notepad++, Notepad and Apple TextEdit. The headers in the IFO file tell DVD players about the starting screen, the location of each video track on disc, the audio tracks location, and other related information.

IFO files can damage if the DVD gets scratches. That is why a BUP file gets created as a backup of the IFO file. In case the IFO file can't be read, the BUP file is read instead. These files are co-located alongside [VOB](https://docs.fileformat.com/video/vob/) file that contains an index of the contents on the disc.

## References

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [Inside Video DVD-Video Files](https://en.wikibooks.org/wiki/Inside_DVD-Video/IFO_Files)
