{
  "date": "2023-06-21",
  "keywords": [
"alitiedosto",
"mikä on alitiedosto",
"esimerkki MicroDVD-tekstitystiedostosta",
"Tekstityksen laajennukset",
"Avaa Sub",
"Tekstitystiedostotyypit",
"kuinka avata SUB-tiedosto",
"tiedosto",
"SUB tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SUB-tiedostomuoto - MicroDVD-tekstitystiedosto",
  "description": "Opi SUB-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata SUB-tiedostoja.",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub-fi",
      "parent": "video"
}
},
  "lastmod": "2023-06-21"
}

## Mikä on SUB-tiedosto?

SUB-tiedosto on MicroDVD-tekstitystiedostomuoto, jota käytetään tekstityksen näyttämiseen videoissa. Tiedostotunniste on yleensä .sub. Nämä tiedostot sisältävät kunkin tekstityksen ajoitustiedot ja tekstin.

MicroDVD-tekstitystiedostot käyttävät yksinkertaista tekstipohjaista muotoa, jossa jokainen tekstitys koostuu useista riveistä. Ensimmäinen rivi sisältää tekstityksen ajoitustiedot, mukaan lukien aloitus- ja lopetusaikaleimat. Seuraavat rivit sisältävät varsinaista tekstitystekstiä.

Here is an example of MicroDVD subtitle file:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Tekstityksen laajennukset

Subtitles can have various file extensions depending on format they are in. Some common subtitle file extensions include:

- **.srt:** SubRip subtitle format. It is one of most widely used subtitle formats and is supported by many media players and video editing software.
- **.sub:** Subtitle file format that can be used by different subtitle formats, such as MicroDVD, SubViewer and SubStation Alpha.
- **.ass or .ssa:** Advanced SubStation Alpha or SubStation Alpha subtitle format. It supports advanced features like text formatting, positioning and effects.
- **.vtt:** WebVTT (Web Video Text Tracks) format used for displaying subtitles on web videos. It is commonly used with HTML5 video players.
- **.idx/.sub:** Format used by DVD subtitles. The .idx file contains timing and formatting information, while .sub file contains the actual subtitle text.
- **.smi or .sami:** Synchronized Accessible Media Interchange format. It is commonly used for closed captions and subtitles in Windows Media Player.

## Mitä Open Sub tarkoittaa?

Open Sub tarkoittaa yleensä OpenSubtitlesia, joka on suosittu online-alusta, joka tarjoaa tekstityksiä elokuville ja TV-ohjelmille useilla kielillä. Se tarjoaa laajan kokoelman käyttäjäyhteisönsä tuottamia tekstitystiedostoja. Voit vierailla OpenSubtitles-sivustolla (www.opensubtitles.org) etsiäksesi ja ladataksesi tekstityksiä haluamillesi elokuville tai TV-sarjoille.

## Tekstitystiedostotyypit

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

## Kuinka avata SUB-tiedosto?

Seuraavat mediasoittimet voivat avata SUB-tiedoston tekstitysraitana.

- VideoLAN VLC -mediasoitin
- MPlayer

Voit avata SUB-tiedoston VLC-soittimessa seuraavasti

- Avaa VLC-soitin ja toista videosi
- Valitse VLC Media Playerin valikkopalkista **Tekstitys > Lisää tekstitystiedosto...**
- Siirry SUB-tiedostoon ja avaa se

Jos haluat muokata SUB-tiedostoa, voit avata sen millä tahansa tekstieditorilla, esim. Microsoft Notepad (Windows) tai Apple TextEdit (Mac).

## Viitteet
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)


