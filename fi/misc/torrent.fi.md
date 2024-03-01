{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Torrent-tiedostomuoto - BitTorrent-tiedosto",
  "description":"Opi TORRENT-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata TORRENT-tiedostoja.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent-fi",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Mikä on TORRENT-tiedosto?

TORRENT-tiedosto on tekstitiedosto, jota BitTorrent ja muut P2P (peer-to-peer) -ohjelmat käyttävät sisällön lataamiseen ja vaihtamiseen. Ladattava sisältö voi sisältää asiakirjoja, videoita, pelejä, elokuvia ja muuta Internetissä saatavilla olevaa mediaa. Se sisältää metatiedot ladattavan median sisällöstä ja sijainnista. Ohjelmistot, kuten BitTorrent, käyttävät tämän tiedoston tietoja, kuten nimeä, tiedostokokoa ja kansiorakennetta tietojen lataamiseen. Torrent-tiedostoja voidaan muuntaa muihin tiedostomuotoihin, kuten [PDF](/pdf/) verkossa.

## Mikä on torrentointi? TORRENT-tiedostomuoto tiedonvaihtoa varten

Torrentointi on käsite datatiedostojen vaihtamisesta (lataamisesta ja lataamisesta) BitTorrent-verkon avulla. Toisin kuin perinteiset palvelimet, joille tiedot ladataan muiden pääsyä ja lataamista varten, torrent-tiedostot haetaan ja lähetetään torrent-verkon kautta. Kun käyttäjä avaa .torrent-tiedoston sovelluksissa, kuten BitTorrent, ohjelmisto alkaa ladata tiedoston sisältöä bittikohtaisesti. Jos useilla käyttäjillä on sama tiedosto, BitTorrent jakaa lataukset kaikkien käyttäjien kesken latausprosessin nopeuttamiseksi. Samalla tiedoston lataavan käyttäjän tietokoneesta tulee myös tiedoston lähde, jolla se lähetetään muille käyttäjille, jotka myös lataavat samaa tiedostoa.

### TORRENT-tiedoston rakenne

Torrent-tiedosto on yhdistelmä tiedostoluettelosta ja metatietotiedoista kaikista ladattavista tiedoston osista. Se sisältää seuraavat tiedot avainten muodossa.

- `announce` - Seuraajan URL-osoite, joka ilmoitetaan muille vertaisversioille tiedoston saatavuudesta ilmoittamiseksi
- info - Tämä yhdistää sanakirjaan, jonka avaimet riippuvat siitä, jaetaanko yksi vai useampi tiedosto:
  - "tiedostot — luettelo sanakirjoista, joista jokainen vastaa tiedostoa (vain silloin, kun useita tiedostoja jaetaan). Jokaisessa sanakirjassa on seuraavat avaimet:"
- `length` — tiedoston koko tavuina.
- `polku` — luettelo alihakemistojen nimiä vastaavista merkkijonoista, joista viimeinen on todellinen tiedoston nimi
- `length` — tiedoston koko tavuina (vain kun yksi tiedosto on jaettu)
- `nimi` — tiedoston nimi, johon tiedosto tallennetaan
- kappaleen pituus — tavujen määrä kappaletta kohti. Tämä on yleensä 28 KiB = 256 KiB = 262 144 B.
- palat — hash-luettelo, joka on ketjutus kunkin palan SHA-1-tiivisteestä.

## Onko torrentointi turvallista ja laillista?

Torrenting-protokolla tiedonvaihtoon P2P-käyttäjien välillä on turvallinen, koska se on vain tapa jakaa minkä tahansa tyyppisiä tiedostoja. Siten protokolla itsessään ei ole vaarallinen tai laiton. Verkon kautta jaettu sisältö voi kuitenkin sisältää tiedostoja tai mediaa, jotka voivat loukata jaettujen asiakirjojen laillista asemaa. Tällaisessa tapauksessa tällaisten tietojen vaihto voi aiheuttaa oikeustoimia tällaisten tiedostojen julkiseen jakamiseen osallistuvia osapuolia vastaan.

## Viitteet

* [TORRENT-tiedosto - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)


