{
  "date": "2021-06-09",
  "keywords": [
"vihje",
"tiedosto",
"laajennus",
"muoto",
"mikä on vihjetiedosto",
"musiikkia",
"cue-tiedostomuoto",
"cue-tiedostomuodon määrittely",
"vihje arkki",
"CDRWIN"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi CUE-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda, muuntaa ja avata CUE-tiedostoja.",
  "title": "CUE - Cue Sheet -tiedosto",
  "linktitle": "CUE",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cu-fie"
}
},
  "lastmod": "2021-07-01"
}

## Mikä on CUE-tiedosto?

Tiedosto, jonka pääte on .cue, joka tunnetaan myös nimellä cue sheet tiedosto, on metatietotiedosto, joka sisältää tietoja CD- tai DVD-levyn raitojen asettelusta. Mediasoittimet ja optisten levyjen luontisovellukset tukevat näitä. Viittatiedosto viittaa CD-levylle tallennettuun tärkeimpään äänidataan sekä kappaleiden pituuden, levyn nimien ja esiintyjien määrittelyihin. Siten jos yksi äänitiedosto sisältää useita raitoja, cue-tiedostoa voidaan käyttää äänen jakamiseen useisiin tiedostoihin tai viittaukseen useisiin raitoihin.

## CUE-tiedostomuoto

CUE- tai cue-arkkitiedostot tallennetaan vain tekstimuodossa, joka on ihmisen luettavissa. Vihjetiedoston tiedot ovat komentoja, joissa on yksi tai useampi parametri. Nämä komennot koskevat joko koko tiedostoa tai yksittäistä raitaa, riippuen tietystä komennosta ja kontekstista. CDRWIN-käyttöoppaassa kuvataan vihjearkin syntaksin ja semantiikan määritykset.

## CUE-arkin välttämättömät komennot

|Komento|Kuvaus|
---|---|
|TIEDOSTO| Viittaa tiedot sisältävään tiedostoon ja sen muotoon, kuten {{HYPERLINKKI}}, {{HYPERLINKKI2}} tai tavallinen binäärilevykuva)|
|RAITA| Määrittää raidan kontekstitiedot, kuten sen numeron ja tyypin tai tilan.|
|INDEKSI| Edustaa sijaintia hakemistona TIEDOSTOssa. Muoto on mm:ss:ff (minuutti-sekunti-ruutu).|
|PREGAP ja POSTGAP|Tämä osoittaa raidan pre- tai jälkivälin, jota ei ole tallennettu mihinkään tiedostoon. Pituus määritetään samassa minuutti-sekuntikehyksen muodossa kuin INDEX.|

### CUE-arkkiesimerkki

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```

## Muut CUE-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cue**-tiedostotunnistetta.

**Levy ja media**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet

* [.cda-tiedosto - Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


