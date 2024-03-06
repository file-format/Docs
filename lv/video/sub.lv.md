{
  "date": "2023-06-21",
  "keywords": [
"apakšfails",
"kas ir apakšfails",
"MicroDVD subtitru faila piemērs",
"Subtitru paplašinājumi",
"Atveriet Sub",
"Subtitru failu veidi",
"kā atvērt SUB failu",
"failu",
"SUB faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SUB faila formāts — MicroDVD subtitru fails",
  "description": "Uzziniet par SUB formātu un API, kas var izveidot un atvērt SUB failus.",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub-lv",
      "parent": "video"
}
},
  "lastmod": "2023-06-21"
}

## Kas ir SUB fails?

SUB fails ir MicroDVD subtitru faila formāts, ko izmanto, lai parādītu subtitrus videoklipos, un parasti tam ir .sub faila paplašinājums. Šie faili satur laika informāciju un tekstu katram subtitru ierakstam.

MicroDVD subtitru faili izmanto vienkāršu teksta formātu, kur katrs subtitru ieraksts sastāv no vairākām rindiņām. Pirmajā rindā ir informācija par subtitru laiku, tostarp sākuma un beigu laikspiedoli. Nākamajās rindās ir faktiskais subtitru teksts.

Here is an example of MicroDVD subtitle file:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Subtitru paplašinājumi

Subtitles can have various file extensions depending on format they are in. Some common subtitle file extensions include:

- **.srt:** SubRip subtitle format. It is one of most widely used subtitle formats and is supported by many media players and video editing software.
- **.sub:** Subtitle file format that can be used by different subtitle formats, such as MicroDVD, SubViewer and SubStation Alpha.
- **.ass or .ssa:** Advanced SubStation Alpha or SubStation Alpha subtitle format. It supports advanced features like text formatting, positioning and effects.
- **.vtt:** WebVTT (Web Video Text Tracks) format used for displaying subtitles on web videos. It is commonly used with HTML5 video players.
- **.idx/.sub:** Format used by DVD subtitles. The .idx file contains timing and formatting information, while .sub file contains the actual subtitle text.
- **.smi or .sami:** Synchronized Accessible Media Interchange format. It is commonly used for closed captions and subtitles in Windows Media Player.

## Ko nozīmē Open Sub?

Open Sub parasti nozīmē OpenSubtitles, kas ir populāra tiešsaistes platforma, kas nodrošina subtitrus filmām un TV pārraidēm vairākās valodās. Tā piedāvā plašu subtitru failu kolekciju, ko nodrošina tās lietotāju kopiena. Varat apmeklēt OpenSubtitles vietni (www.opensubtitles.org), lai meklētu un lejupielādētu subtitrus vēlamajām filmām vai seriāliem.

## Subtitru failu veidi

Subtitle files come in various formats, each with its own file type or extension. Here are some common subtitle file types:

- **SubRip Subtitle Format (.srt):** This is one of most widely used subtitle formats. SRT files are plain text files that contain subtitle entries with timestamps and corresponding text.
- **SubViewer Subtitle Format (.sub):** SubViewer files are similar to SRT files, contain subtitle entries with timestamps and text, may support additional features such as text formatting and colors.
- **SubStation Alpha (.ssa) and Advanced SubStation Alpha (.ass):** These formats support advanced features like text formatting, styling, positioning and animation effects. SSA and ASS files are commonly used for anime subtitles.
- **MicroDVD Subtitle Format (.sub):** MicroDVD format uses .sub files and includes timing information and text for each subtitle entry. It is often used with media players and video editing software.
- **DVD Subtitles (.sub and .idx):** DVD subtitles typically consist of two files: the .sub file, which contains subtitle text, and .idx file, which contains timing and formatting information.
- **WebVTT (.vtt):** WebVTT is a subtitle format used for web videos, commonly used with HTML5 video players and supports basic formatting options.
- **MPL2 Subtitle Format (.mpl):** MPL2 files are used with MPlayer, a media player for Unix-like systems, contain subtitle entries with timestamps and text.
- **iTunes Timed Text (.itt):** iTunes Timed Text files are used for subtitles in Apple's iTunes and other Apple platforms. They support features like text styling and positioning.
- **Teletext Subtitle Format (.srt or .txt):** Teletext subtitles are commonly used in broadcast television. They are usually saved as plain text files with .srt or .txt extensions.

## Kā atvērt SUB failu?

Tālāk norādītie multivides atskaņotāji var atvērt SUB failu kā subtitru celiņu.

- VideoLAN VLC multivides atskaņotājs
- MPlayer

Lai atvērtu SUB failu VLC atskaņotājā, veiciet šīs darbības

- Atveriet VLC atskaņotāju un atskaņojiet savu video
- VLC Media Player izvēlņu joslā atlasiet **Subtitri > Pievienot subtitru failu...**
- Pārejiet uz SUB failu un atveriet to

Ja jums ir nepieciešams rediģēt SUB failu, varat to atvērt ar jebkuru teksta redaktoru, piemēram, Microsoft Notepad (Windows) vai Apple TextEdit (Mac).

## Atsauces
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)


