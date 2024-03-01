{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LRC-tiedostomuoto - Mikä on LRC-tiedosto?",
  "description": "Opi LRC Lyric -tiedostosta ja sovellusliittymistä, jotka voivat luoda ja avata LRC-tiedostoja.",
  "linktitle": "LRC",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-lr-fic"
}
},
  "lastmod": "2022-01-26"
}

## Mikä on LRC-tiedosto?

LRC-tiedosto on tekstipohjainen sanoitustiedosto, joka sisältää äänikappaleen sanat. Kun äänikappaletta toistetaan tietokoneessa olevalla musiikkisoittimella tai äänisoitinohjelmistolla, LRC-tiedosto luetaan rinnakkain ja näytetään ajan myötä. LRC-tiedostot sisältävät vihjepisteitä sanoitusten näyttämiseksi kappaleen soidessa. Yleensä LRC-tiedostoilla on sama nimi kuin vastaavilla äänitiedostoilla, kuten audio.mp3 ja audio.lrc. LRC-tiedostot ovat samanlaisia kuin tekstitystiedostoja, kuten [SRT](/video/srt/).

## LRC-tiedostomuoto - lisätietoja

LRC-lyriikat tiedostot tallennetaan pelkkänä tekstitiedostoina ja niitä voidaan avata ja muokata tekstitiedostossa. LRC-tiedoston sisältö sisältää väritietoja sanoitustekstin näyttämistä varten.

## LRC-muodot

LRC-tiedostoilla on useita muotoja, joita on kehitetty ajan myötä. Nämä

### Yksinkertainen LRC-muoto

Linjan aikatunnisteet ovat muodossa [mm:ss.xx], jossa mm on minuuttia, ss on sekuntia ja xx on sekunnin sadasosa.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Yksinkertainen muoto, laajennettu

Se sisältää mahdollisuuden muuttaa ja määrittää sanoitusten sukupuolta käyttämällä M: Mies, F: Nainen, D: Duetti.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Parannettu LRC-muoto

Parannettu LRC-muoto on laajennettu versio Simple LRC -formaatista. Se lisää Wordin aikatunnisteen muodossa `<mm:ss.xx> ` edellisen sanan lopussa.

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

## Viitteet

* [LRC Lyrics File Format - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))


