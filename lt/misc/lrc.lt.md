{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LRC failo formatas – kas yra LRC failas?",
  "description": "Sužinokite apie LRC Lyric failą ir API, kurios gali kurti ir atidaryti LRC failus.",
  "linktitle": "LRC",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-lr-ltc"
}
},
  "lastmod": "2022-01-26"
}

## Kas yra LRC failas?

LRC failas yra tekstinis dainų tekstas, kuriame yra garso dainos žodžiai. Kai garso daina grojama naudojant muzikos grotuvą arba garso grotuvo programinę įrangą kompiuteryje, LRC failas skaitomas lygiagrečiai ir rodomas kartu su laiku. LRC failuose yra užuominos taškų, skirtų dainai grojant rodyti dainų žodžius. Paprastai LRC failai turi tokį patį pavadinimą kaip ir atitinkamas garso failas, pvz., audio.mp3 ir audio.lrc. LRC failai yra panašūs į subtitrų failus, pvz., [SRT](/video/srt/).

## LRC failo formatas – daugiau informacijos

LRC dainų formato failai išsaugomi kaip paprasto teksto failai ir gali būti atidaryti bei redaguoti tekstiniame faile. LRC failo turinys turi spalvų informaciją, skirtą dainų žodžių tekstui rodyti.

## LRC formatai

Laikui bėgant buvo sukurti keli LRC failų formatai. Šie

### Paprastas LRC formatas

Linijos laiko žymos yra formatu [mm:ss.xx], kur mm yra minutės, ss yra sekundės ir xx yra šimtosios sekundės dalys.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Išplėstinis paprastas formatas

Tai apima galimybę keisti ir nurodyti dainų žodžių lytį naudojant M: Vyras, F: Moteris, D: Duetas.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Patobulintas LRC formatas

Patobulintas LRC formatas yra išplėstinė Simple LRC formato versija. Ji prideda Word laiko žymą formatu <mm:ss.xx> ` ankstesnio žodžio pabaigoje.

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

## Nuorodos

* [LRC dainų žodžių failo formatas – Vikipedija](https://en.wikipedia.org/wiki/LRC_(file_format))


