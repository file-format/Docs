{
  "date": "2021-06-09",
  "keywords": [
"cda",
"tiedosto",
"laajennus",
"muoto",
"mikä on cda-tiedosto",
"musiikkia",
"cda tiedostomuoto",
"cda-tiedostomuodon määrittely"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi CDA-tiedostomuodosta ja API-liittymistä, jotka voivat luoda, muuntaa ja avata CDA-tiedostoja.",
  "title": "CDA - CD-ääniraidan pikakuvaketiedosto",
  "linktitle": "CDA",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-cda"
}
},
  "lastmod": "2021-06-09"
}

## Mikä on CDA-tiedosto?

Tiedosto, jonka pääte on .cda, on pieni tynkätiedosto, jonka Microsoft Windows luo jokaiselle ääni-CD:n ääniraidalle. Nämä tiedostot sisältävät tyypillisiä tietoja, kuten raitaajat ja Windowsin pikakuvakkeen, jonka avulla käyttäjät voivat käyttää tiettyjä ääniraitoja. CDA-tiedostot eivät ole musiikkia, mutta ne osoittavat jossain tallennustilassa olevaan musiikkitiedostoon. Voimme sanoa sen CD-levyllä olevan äänitiedoston pikakuvakkeena.

## CDA tiedostomuoto

CDA-tiedostomuotoa käytetään kertomaan tietokoneelle, mikä äänitiedosto CD-levyllä toistetaan. Joten CDA-tiedostot tulevat hyödyttömiksi erotettuina edustamasta CD-levystä. CDA-tiedostoja pidetään yleisesti RIFF-resursseina. .cda-tiedoston nykyisessä versiossa on vain yksi kappale, jonka nimi on CDDA ja joka sisältää vain yhden tietolohkon nimeltä FMT. Tämä lohko on 24 tavua pitkä. Windows 95:een ja Windows 98:aan liittyvä CD-asema käyttää Windowsin luomaa tunnistetta, eikä sen soitin voi muodostaa yhteyttä FreeDB:hen tai CDDB:hen. Jotta se voi näyttää kappaleen nimen ja esittäjän nimen, sinun on syötettävä nämä tiedot manuaalisesti cdplayer.ini-tiedostoon.

### CDA-tiedoston järjestäminen

Seuraavassa taulukossa on tietoja tyypillisistä poikkeamista:
| offset | pituus | sisältö |
---|---|---|
| 0x00 | 4 | 4 ASCII-merkkiä RIFF |
| 0x04 | 4 | seuraavan osan koko: aina 36 (44 - 8), 4 tavua (Intel-järjestys) |
| 0x08 | 4 | chunk identifier: the 4 ASCII characters "CDDA"-fi |
| 0x0C | 4 | 3 ASCII-merkkiä fmt, jota seuraa välilyönti |
| 0x10 | 4 | kappaleen pituus: aina 24, 4 tavua (Intel-järjestys) |
| 0x14 | 2 | version of the CD format, on 2 bytes (Intel order). In May 2006, always equal to 1. |
| 0x016 | 2 | number of the range, on 2 bytes (Intel order). The first track has the number 1. |
| 0x18 | 4 | Windowsin laskema tunniste cdplayer.exe-tiedostolle. |
| 0x1c | 4 | alueen siirtymä, kehysten lukumääränä (Intel-järjestys) |
| 0x20 | 4 | raidan kesto, kehysten kokonaismäärä (Intel-tilaus) |
| 0x24 | 1 | alueen sijainti: kehykset |
| 0x25 | 1 | alueen sijainti: sekuntia |
| 0x26 | 1 | kantaman sijainti: minuuttia |
| 0x27 | 1 | nollatavu (binääriarvo 0) |
| 0x28 | 1 | kappaleen kesto: kehyksiä |
| 0x29 | 1 | kappaleen kesto: sekuntia |
| 0x2a | 1 | kappaleen kesto: minuuttia |
| 0x2b | 1 | nollatavu (binääriarvo 0) |

## Viitteet

* [.cda-tiedosto - Wikipedia](https://en.wikipedia.org/wiki/.cda_file)


