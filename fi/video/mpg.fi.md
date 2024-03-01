{
  "date": "2021-04-15",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "MPG tiedostomuoto",
  "keywords": [
"MPG",
"tiedosto",
"laajennus",
"muoto",
"videomuoto",
"mikä on mpg-tiedostomuoto",
"mpg tiedostomuoto",
"mpg tiedostosoitin",
"mpeg pakkaus",
"video",
"MPEG",
"MPEG-1",
"MPEG-2"
],
  "description": "Opi MPG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja näyttää, kuinka MPG-tiedostoja avataan.",
  "linktitle": "MPG",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mp-fig"
}
},
  "lastmod": "2021-07-26"
}

## Mikä on MPG-tiedostomuoto? ##

The file with a .mpg extension belongs to the group of file extensions for MPEG-1 or MPEG-2 audio and video compression. MPEG-1 Part 2 video is not easily available, and this extension (MPG file format) typically points to a MPEG program stream which is defined in MPEG-1 and MPEG-2, or an MPEG transport stream which is defined in MPEG-2. Myös muita laajennuksia, kuten .m2ts, on olemassa, jotka määrittävät tarkan säilön, tässä tapauksessa MPEG-2 TS, mutta tällä ei ole juurikaan merkitystä MPEG-1-medialle. [.mp3](/audio/mp3/) on yleisin MP3-ääntä sisältävien tiedostojen laajennus. MP3-tiedosto on tyypillinen raakaäänen virta; perinteinen tapa merkitä MP3-tiedostoja on kirjoittaa stream-dataa jokaisen kehyksen roskasegmentteihin, jotka tallentavat mediatiedot, mutta **mpg-tiedostosoitin** hylkäävät ne. Tämä on samanlainen tekniikka, jota käytetään AAC-tiedostojen merkitsemiseen, mutta sitä tuetaan nykyään vähemmän.

## MPEG-pakkaus ##

Nimi MPEG tulee sanoista Moving Pictures Experts Group. MPEG on työkalu videoiden pakkaamiseen, joka sisältää kuvien ja äänen pakkaamisen sekä näiden kahden synkronoinnin.
Tällä hetkellä on olemassa useita MPEG-standardeja.

- MPEG-1:tä ehdotetaan keskitason datanopeuksille, luokkaa 1,5 Mbit/s.
- MPEG-2:ta suositellaan korkeille tiedonsiirtonopeuksille, vähintään 10 Mbit/s.
- MPEG-3:a ehdotettiin HDTV-pakkaukseksi, mutta sen todettiin olevan tarpeeton ja se yhdistettiin MPEG-2:een.
- MPEG-4:ää suositellaan erittäin alhaisille tiedonsiirtonopeuksille, alle 64 kbit/s.


## Ohjelmavirta MPG-tiedostomuodossa ##

Ohjelmavirta on säiliö digitaalisen äänen, videon ja muun multipleksointiin. Ohjelmavirran muoto on määritetty MPEG-1:n ensimmäisessä osassa (ISO/IEC 11172-1) ja MPEG-2:n ensimmäisessä osassa Systems (ISO/IEC-standardi 13818-1/ITU-T H.222.0). MPEG-2 Program Stream on analoginen ja samanlainen kuin ISO/IEC 11172 Systems -taso ja eteenpäin yhteensopiva.

### Koodaustiedot ###

Tässä ovat osittaisen MPEG-2 Program Stream -paketin otsikkomuodon koodaustiedot:

| Nimi | Bittien määrä | Kuvaus |
---|---|---|
| synkronoida tavua | 32 | 0x000001BA |
| merkkipalat | 2 | 01b MPEG-2-versiolle. MPEG-1-version merkkibitit ovat 4 bittiä, joiden arvo on 0010b. |
| Järjestelmän kello [32..30] | 3 | System Clock Reference (SCR) -bitit 32 - 30 |
| merkkiterä | 1 | 1 bitti aina asetettu. |
| Järjestelmän kello [29..15] | 15 | Järjestelmän kellon bitit 29 - 15 |
| merkkiterä | 1 | 1 bitti aina asetettu. |
| Järjestelmän kello [14..0] | 15 | Järjestelmän kellon bitit 14 - 0 |
| merkkiterä | 1 | 1 bitti aina asetettu. |
| SCR-laajennus | 9 | |
| merkkiterä | 1 | 1 bitti aina asetettu. |
| bittinopeus | 22 | Yksiköissä 50 tavua sekunnissa. |
| merkkipalat | 2 | 11 bittiä aina asetettu. |
| varattu | 5 | varattu tulevaa käyttöä varten |
| täytteen pituus | 3 | |
| täytetavut | 8* täytepituus | |
| järjestelmän otsikko (valinnainen) | 0 tai enemmän | jos järjestelmän otsikon aloituskoodi seuraa: 0x000001BB |

Seuraava taulukko näyttää osittaisen järjestelmän otsikon muodon:

| Nimi | Tavujen määrä | Kuvaus |
---|---|---|
| synkronoida tavua | 4 | 0x000001BB |
| otsikon pituus | 2 | |
| nopeus sidottu ja merkkibitit | 3 | |
| audio sidottu ja liput | 1 | |
| liput, merkkibitti ja videosidottu | 1 | |
| Pakettinopeuden rajoitus ja varattu tavu | 1 | |


## Viitteet ##

- {{HYPERLINKKI1}}



