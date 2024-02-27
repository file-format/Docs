{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LRC-filformat - Hvad er en LRC-fil?",
  "description": "Lær om LRC Lyric-filen og API'er, der kan oprette og åbne LRC-filer.",
  "linktitle": "LRC",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-lr-dac"
}
},
  "lastmod": "2022-01-26"
}

## Hvad er en LRC fil?

En LRC-fil er en tekstbaseret tekstfil, der indeholder teksten til en lydsang. Når lydsangen afspilles med en musikafspiller eller lydafspillersoftware på en computer, læses LRC-filen parallelt og vises med tiden. LRC-filer indeholder cue-punkter til visning af tekster, når sangen afspilles. Generelt har LRC-filerne samme navn som den tilsvarende lydfil såsom audio.mp3 og audio.lrc. LRC-filer ligner undertekstfiler såsom [SRT](/video/srt/).

## LRC-filformat - flere oplysninger

Filer i LRC-lyrisk format gemmes som almindelige tekstfiler og kan åbnes og redigeres i en tekstfil. Indholdet af en LRC-fil indeholder farveinformation til visning af sangtekst.

## LRC-formater

Der er flere formater af LRC-filer, der er blevet udviklet over tid. Disse

### Simpelt LRC-format

Linjetidsmærkerne er i formatet [mm:ss.xx], hvor mm er minutter, ss er sekunder og xx er hundrededele af et sekund.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Simple Format Extended

Det inkluderer evnen til at ændre og specificere sangteksternes køn ved at bruge M: Mand, F: Kvinde, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Forbedret LRC-format

Det forbedrede LRC-format er en udvidet version af Simple LRC-formatet. Den tilføjer et Word-tidstag i formatet `<mm:ss.xx> ` i slutningen af det forrige ord.

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

## Referencer

* [LRC Lyrics File Format - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))


