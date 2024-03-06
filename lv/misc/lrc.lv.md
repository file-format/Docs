{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LRC faila formāts — kas ir LRC fails?",
  "description": "Uzziniet par LRC Lyric failu un API, kas var izveidot un atvērt LRC failus.",
  "linktitle": "LRC",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-lr-lvc"
}
},
  "lastmod": "2022-01-26"
}

## Kas ir LRC fails?

LRC fails ir uz tekstu balstīts dziesmu tekstu fails, kas satur audio dziesmas vārdus. Kad audio dziesma tiek atskaņota ar mūzikas atskaņotāju vai audio atskaņotāja programmatūru datorā, LRC fails tiek lasīts paralēli un parādīts ar laiku. LRC faili satur norādes punktus dziesmu vārdu parādīšanai, kad dziesma tiek atskaņota. Parasti LRC failiem ir tāds pats nosaukums kā atbilstošajam audio failam, piemēram, audio.mp3 un audio.lrc. LRC faili ir līdzīgi subtitru failiem, piemēram, [SRT](/video/srt/).

## LRC faila formāts — vairāk informācijas

LRC liriskā formāta faili tiek saglabāti kā vienkārša teksta faili, un tos var atvērt un rediģēt teksta failā. LRC faila saturs satur krāsu informāciju dziesmu teksta parādīšanai.

## LRC formāti

Laika gaitā ir izstrādāti vairāki LRC failu formāti. Šie

### Vienkāršs LRC formāts

Līnijas laika atzīmes ir formātā [mm:ss.xx], kur mm ir minūtes, ss ir sekundes un xx ir sekundes simtdaļas.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Vienkāršs formāts paplašināts

Tas ietver iespēju mainīt un norādīt dziesmu vārdu dzimumu, izmantojot M: Vīrietis, F: Sieviete, D: Duets.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Uzlabots LRC formāts

Uzlabotais LRC formāts ir Simple LRC formāta paplašināta versija. Tas pievieno Word laika tagu formātā `<mm:ss.xx> ` iepriekšējā vārda beigās.

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

## Atsauces

* [LRC dziesmu tekstu faila formāts — Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))


