{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC-bestandsindeling - Wat is een LRC-bestand?",
  "description":"Meer informatie over het LRC Lyric-bestand en API's die LRC-bestanden kunnen maken en openen.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Wat is een LRC-bestand?

Een LRC-bestand is een op tekst gebaseerd songtekstbestand dat de songtekst van een audiosong bevat. Wanneer het audionummer wordt afgespeeld met een muziekspeler of audiospelersoftware op een computer, wordt het LRC-bestand parallel gelezen en met de tijd weergegeven. LRC-bestanden bevatten cue-punten voor het weergeven van songteksten wanneer het nummer wordt afgespeeld. Over het algemeen hebben de LRC-bestanden dezelfde naam als het bijbehorende audiobestand, zoals audio.mp3 en audio.lrc. LRC-bestanden zijn vergelijkbaar met ondertitelbestanden zoals [SRT](/nl/video/srt/).

## LRC-bestandsindeling - Meer informatie

LRC-bestanden in songtekstformaat worden opgeslagen als platte tekstbestanden en kunnen worden geopend en bewerkt in een tekstbestand. De inhoud van een LRC-bestand bevat kleurinformatie voor de weergave van songteksten.

## LRC-indelingen

Er zijn meerdere formaten van LRC-bestanden die in de loop van de tijd zijn ontwikkeld. Deze

### Eenvoudig LRC-formaat

De lijntijdlabels hebben de indeling `[mm:ss.xx]` waarbij mm minuten is, ss seconden en xx honderdsten van een seconde.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Eenvoudig formaat uitgebreid

Het bevat de mogelijkheid om het geslacht van de songtekst te wijzigen en te specificeren door M: Male, F: Female, D: Duet te gebruiken.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Verbeterd LRC-formaat

Het verbeterde LRC-formaat is een uitgebreide versie van het Simple LRC-formaat. Het voegt een Word Time Tag toe in het formaat`<mm:ss.xx>` aan het einde van het vorige woord.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Referenties

* [LRC Lyrics-bestandsindeling - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

