{
"date": "2023-06-21",
  "keywords": [
"underfil",
"vad är en underfil",
"exempel på MicroDVD undertextfil",
"Undertexttillägg",
"Öppen sub",
"Subtext filtyper",
"hur man öppnar SUB-fil",
"fil",
"SUB filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SUB-filformat - MicroDVD-undertextfil",
  "description":"Läs mer om SUB-format och API:er som kan skapa och öppna SUB-filer.",
  "linktitle": "SUB",
  "menu": {
    "docs": {
      "identifier": "video-sub",
      "parent": "video"
}
},
"lastmod": "2023-06-21"
}

## Vad är SUB fil?

En SUB-fil är ett MicroDVD-undertextfilformat som används för att visa undertexter i videor, vanligtvis med filtillägget .sub. Dessa filer innehåller tidsinformation och text för varje undertextpost.

MicroDVD undertextfiler använder ett enkelt textbaserat format där varje undertextpost består av flera rader. Den första raden innehåller undertextens tidsinformation, inklusive start- och sluttidsstämplar. De efterföljande raderna innehåller faktisk undertext.

Här är ett exempel på MicroDVD-undertextfil:

```
{0}{100}Subtitle line 1
{150}{300}Subtitle line 2
{350}{550}Subtitle line 3
...
```

## Undertexttillägg

Undertexter kan ha olika filtillägg beroende på format de är i. Några vanliga filtillägg för undertexter inkluderar:

- **.srt:** SubRip undertextformat. Det är ett av de mest använda undertextformaten och stöds av många mediaspelare och videoredigeringsprogram.
- **.sub:** Undertextfilformat som kan användas av olika undertextformat, som MicroDVD, SubViewer och SubStation Alpha.
- **.ass eller .ssa:** Avancerat SubStation Alpha eller SubStation Alpha undertextformat. Den stöder avancerade funktioner som textformatering, positionering och effekter.
- **.vtt:** WebVTT-format (Web Video Text Tracks) som används för att visa undertexter på webbvideor. Det används ofta med HTML5-videospelare.
- **.idx/.sub:** Format som används av DVD-undertexter. .idx-filen innehåller information om timing och formatering, medan .sub-filen innehåller den faktiska undertexten.
- **.smi eller .sami:** Format för synkroniserat tillgängligt mediautbyte. Det används ofta för dold bildtext och undertexter i Windows Media Player.

## Vad menas med Open Sub?

Open Sub betyder vanligtvis OpenSubtitles som är en populär onlineplattform som tillhandahåller undertexter för filmer och TV-program på flera språk. Det erbjuder en stor samling av undertextfiler som bidragit från dess gemenskap av användare. Du kan besöka webbplatsen OpenSubtitles (www.opensubtitles.org) för att söka efter och ladda ner undertexter för dina önskade filmer eller TV-serier.

## Filtyper för undertexter

Undertextfiler finns i olika format, alla med sin egen filtyp eller filtillägg. Här är några vanliga undertextfiltyper:

- **SubRip undertextformat (.srt):** Detta är ett av de mest använda undertextformaten. SRT-filer är vanliga textfiler som innehåller undertextposter med tidsstämplar och motsvarande text.
- **SubViewer Subtitle Format (.sub):** SubViewer-filer liknar SRT-filer, innehåller undertextposter med tidsstämplar och text, kan stödja ytterligare funktioner som textformatering och färger.
- **SubStation Alpha (.ssa) och Advanced SubStation Alpha (.ass):** Dessa format stöder avancerade funktioner som textformatering, stil, positionering och animeringseffekter. SSA- och ASS-filer används ofta för anime-undertexter.
- **MicroDVD Subtitle Format (.sub):** MicroDVD-formatet använder .sub-filer och inkluderar tidsinformation och text för varje undertextpost. Det används ofta med mediaspelare och videoredigeringsprogram.
- **DVD-undertexter (.sub och .idx):** DVD-undertexter består vanligtvis av två filer: .sub-filen, som innehåller undertext, och .idx-fil, som innehåller information om tid och format.
- **WebVTT (.vtt):** WebVTT är ett undertextformat som används för webbvideor, som vanligtvis används med HTML5-videospelare och stöder grundläggande formateringsalternativ.
- **MPL2 undertextformat (.mpl):** MPL2-filer används med MPlayer, en mediaspelare för Unix-liknande system, innehåller undertextposter med tidsstämplar och text.
- **iTunes Timed Text (.itt):** iTunes Timed Text-filer används för undertexter i Apples iTunes och andra Apple-plattformar. De stöder funktioner som textstil och positionering.
- **Text-TV-undertextformat (.srt eller .txt):** Text-TV-undertexter används ofta i TV-sändningar. De sparas vanligtvis som vanliga textfiler med tilläggen .srt eller .txt.

## Hur öppnar man filen SUB?

Följande mediaspelare kan öppna SUB-filen som ett undertextspår.

- VideoLAN VLC mediaspelare
- MPlayer

Följ dessa steg för att öppna SUB-filen i VLC-spelaren

- Öppna VLC-spelaren och spela upp din video
- Från VLC Media Player-menyraden, välj **Undertexter > Lägg till undertextfil ....**
- Navigera till SUB-fil och öppna den

Om du behöver redigera SUB-fil kan du öppna den med vilken textredigerare som helst, t.ex. Microsoft Notepad (Windows) eller Apple TextEdit (Mac).

## Referenser
* [MicroDVD](https://en.wikipedia.org/wiki/MicroDVD)

