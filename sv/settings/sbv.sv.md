{
"datum": "2023-03-22",
  "keywords": [
"sbv-fil",
"vad är en sbv-fil",
"hur man öppnar en sbv-fil",
"fil",
"sbv filtillägg",
"förlängning"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "SBV-filformat - YouTube Captions File",
  "description":"Läs mer om SBV-format och API:er som kan skapa och öppna SBV-filer.",
  "linktitle": "SBV",
  "menu": {
    "docs": {
      "identifier": "settings-sbv",
      "parent": "settings"
}
},
"lastmod": "2023-03-22"
}

## Vad är en SBV fil?

En fil med filtillägget .sbv är en undertextfil för SubViewer. SubViewer är ett format för undertexter som används med videofiler som har sitt ursprung i början av 2000-talet. .sbv-filen innehåller textningstexten tillsammans med tidsinformation för när varje undertext ska visas under videouppspelningen.

SubViewer-filer används ofta med YouTube-videor, eftersom YouTube stöder SubViewer-formatet för sina videotexter. SubViewer-filer kan också användas med andra videospelare och programvara som stöder formatet.

För att använda en .sbv-fil med en videofil bör både videofilen och .sbv-filen finnas i samma mapp och ha samma filnamn (förutom filtillägget). Många videospelare kommer automatiskt att ladda .sbv-filen när videon spelas upp om filerna namnges på detta sätt. Det finns olika applikationer för redigering av undertexter som stöder SubViewer-formatet om du behöver generera eller redigera en .sbv-fil. Aegisub, Subtitle Workshop och Subtitle Edit är några av de ofta använda verktygen.

## SBV-filformat – Mer information

SBV-filformatet är ett enkelt textbaserat format som används för att lagra undertexter för videor. SBV står för "SubViewer" eller "SubRip Video", beroende på källan till filen. SBV-filer innehåller undertexter som är synkroniserade med videoinnehållet. Varje underrubrik består av en tidsstämpel som anger start- och sluttider för undertexten, följt av undertextens text. Tidsstämpeln är vanligtvis i formatet "hh:mm:ss, mmm" där "hh" representerar timmar, "mm" representerar minuter, "ss" representerar sekunder och "mmm" representerar millisekunder. Texten i undertexten är vanligtvis i vanlig textformat.

Här är ett exempel på hur en SBV-fil kan se ut:

```
0:00:01.000,0:00:03.000
Hello, and welcome to our video!

0:00:04.000,0:00:06.000
In this video, we will be discussing the SBV file format.

0:00:07.000,0:00:10.000
The SBV format is commonly used for storing subtitles for videos.
```

SBV-filer kan skapas och redigeras med en mängd olika redigeringsprogram för undertexter, såsom Subtitle Workshop, Aegisub eller Subtitle Edit. När undertexterna är klara kan SBV-filen importeras till ett videoredigeringsprogram för att skapa en undertextad video. Sammantaget är SBV-filformatet ett enkelt och allmänt använt format för att lagra undertexter som är kompatibelt med många videoredigeringsprogram och -spelare.

## Hur öppnar man filen SBV?

SBV-filer är textfiler så att du kan öppna dem med vilken textredigerare som helst, t.ex. Notepad eller Notepad++

## Referenser
* [SubViewer](https://wiki.videolan.org/SubViewer/)

