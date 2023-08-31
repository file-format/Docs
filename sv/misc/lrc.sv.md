{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC-filformat - Vad är en LRC-fil?",
  "description":"Läs mer om LRC Lyric-filen och API:er som kan skapa och öppna LRC-filer.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Vad är en LRC fil?

En LRC-fil är en textbaserad textfil som innehåller texten till en ljudlåt. När ljudlåten spelas med en musikspelare eller ljudspelarprogramvara på en dator läses LRC-filen parallellt och visas med tiden. LRC-filer innehåller referenspunkter för visning av texter när låten spelas. I allmänhet har LRC-filerna samma namn som motsvarande ljudfil som audio.mp3 och audio.lrc. LRC-filer liknar undertextfiler som [SRT](/sv/video/srt/).

## LRC-filformat - Mer information

LRC-filer i lyric-format sparas som vanliga textfiler och kan öppnas och redigeras i en textfil. Innehållet i en LRC-fil innehåller färginformation för visning av sångtext.

## LRC-format

Det finns flera format av LRC-filer som har utvecklats över tiden. Dessa

### Enkelt LRC-format

Linjetidstaggarna har formatet `[mm:ss.xx]` där mm är minuter, ss är sekunder och xx är hundradelar av en sekund.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Enkelt format utökat

Det inkluderar möjligheten att ändra och specificera könet på texterna genom att använda M: Man, F: Female, D: Duett.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Förbättrat LRC-format

Det förbättrade LRC-formatet är en utökad version av Simple LRC-formatet. Den lägger till en Word Time Tag i formatet`<mm:ss.xx>` i slutet av föregående ord.

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

## Referenser

* [LRC Lyrics File Format - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))

