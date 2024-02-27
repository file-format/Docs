{
  "date": "2023-06-21",
  "keywords": [
"underfil",
"hvad er en underfil",
"eksempel på MicroDVD undertekstfil",
"Undertekstudvidelser",
"Åbn Sub",
"Undertekst filtyper",
"hvordan man åbner SUB fil",
"fil",
"SUB filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SUB-filformat - MicroDVD-undertekstfil",
  "description": "Lær om SUB-format og API'er, der kan oprette og åbne SUB-filer.",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub-da",
      "parent": "video"
}
},
  "lastmod": "2023-06-21"
}

## Hvad er SUB fil?

En SUB-fil er et MicroDVD-undertekstfilformat, der bruges til at vise undertekster i videoer, som typisk har filtypenavnet .sub. Disse filer indeholder timingoplysninger og tekst for hver undertekstindgang.

MicroDVD undertekstfiler bruger simpelt tekstbaseret format, hvor hver undertekstindgang består af flere linjer. Den første linje indeholder undertekstens timingoplysninger, inklusive start- og sluttidsstempler. De efterfølgende linjer indeholder egentlig underteksttekst.

Here is an example of MicroDVD subtitle file:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Undertekstudvidelser

Subtitles can have various file extensions depending on format they are in. Some common subtitle file extensions include:

- **.srt:** SubRip subtitle format. It is one of most widely used subtitle formats and is supported by many media players and video editing software.
- **.sub:** Subtitle file format that can be used by different subtitle formats, such as MicroDVD, SubViewer and SubStation Alpha.
- **.ass or .ssa:** Advanced SubStation Alpha or SubStation Alpha subtitle format. It supports advanced features like text formatting, positioning and effects.
- **.vtt:** WebVTT (Web Video Text Tracks) format used for displaying subtitles on web videos. It is commonly used with HTML5 video players.
- **.idx/.sub:** Format used by DVD subtitles. The .idx file contains timing and formatting information, while .sub file contains the actual subtitle text.
- **.smi or .sami:** Synchronized Accessible Media Interchange format. It is commonly used for closed captions and subtitles in Windows Media Player.

## Hvad menes med Open Sub?

Open Sub betyder typisk OpenSubtitles, som er en populær online platform, der leverer undertekster til film og tv-serier på flere sprog. Det tilbyder en stor samling af undertekstfiler bidraget fra dets brugerfællesskab. Du kan besøge OpenSubtitles-webstedet (www.opensubtitles.org) for at søge efter og downloade undertekster til dine ønskede film eller tv-serier.

## Undertekst filtyper

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

## Hvordan åbner jeg filen SUB?

Følgende medieafspillere kan åbne SUB-filen som et undertekstspor.

- VideoLAN VLC medieafspiller
- MPlayer

Følg disse trin for at åbne SUB-filen i VLC-afspilleren

- Åbn VLC-afspiller og afspil din video
- Fra VLC Media Player-menulinjen skal du vælge **Undertekster > Tilføj undertekstfil ....**
- Naviger til SUB-fil og åbn den

Hvis du har brug for at redigere SUB-fil, kan du åbne den med en hvilken som helst teksteditor, f.eks. Microsoft Notepad (Windows) eller Apple TextEdit (Mac).

## Referencer
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)


