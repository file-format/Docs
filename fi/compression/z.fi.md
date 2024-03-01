{
  "date": "2021-06-22",
  "keywords": [
"Z",
"Pakattu",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"UNIX",
"Kartz"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "Z Pakattu tiedostomuoto",
  "description": "Opi Z-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata Z-tiedostoja.",
  "linktitle": "Z",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression--fiz"
}
},
  "lastmod": "2021-06-22"
}

## Mikä on Z-tiedosto? ##

AZ-tiedosto on tiedostoluokka, joka kuuluu UNIX-pakattuihin datatiedostoihin. Pakatut Unix-tiedostot ovat Z-tiedoston suosituin ja laajimmin käytetty laajennustyyppi. Z-tiedosto helpottaa tiedostojen muotoilua, suorittamista ja avaamista, koska niitä käytetään luomaan pieniä tietokonetiedostoja, joita voidaan helposti käyttää Linux/Unix-käyttöjärjestelmissä. Se on hyödyllinen käyttäjille, jotka haluavat säästää levytilaa, koska pakkaamalla suuria tiedostoja yhdeksi Z-tiedostoksi käyttäjät voivat säästää paljon tallennustilaa ja tehdä tiedostoistaan järjestäytyneempiä. Nämä pakatut Z-tiedostot voidaan helposti purkaa Unix-järjestelmässä käyttämällä yksinkertaista komentoa uncompress abc.z tiedostolle nimeltä abc.


## Lyhyt historia ##

Z-tiedosto luotiin nopean arkistoinnin horjumattoman kysynnän seurauksena 80-luvun lopulla ja 90-luvun alussa. Koska Internet ei ollut tuolloin kovin suosittu ja saatavilla, käyttäjien oli vaikea jakaa perustiedostoja ja päästäkseen Internetiin. Yksi tapa, jolla käyttäjät siirsivät tiedostoja, oli arkistointi. Phil Katz esitteli Z-tiedoston nopeampana ja tukevampana Archiver-muotona, jonka kautta valtavia tiedostoja voitiin pakata yhdeksi ja siirtää. Kartzin lopullinen versio esiteltiin vuonna 1989 oikeudellisen taistelun jälkeen, ja se oli omistettu julkisuuteen, kuten Kartz ilmoitti.


## Tekniset tiedot ##

Z-tiedosto on tiedosto, joka tukee arkistotiedostomuotoa. Se on yksi ensimmäisistä tiedostotyypeistä, jotka tarjoavat nopean ja häviöttömän tiedon pakkaamisen ja purkamisen Unix- ja Linux-käyttöjärjestelmissä. Joissakin käyttöjärjestelmissä tiedostotunniste, jossa on pieni kirjain Z (.z), edustaa GNU-pakattua tiedostoa, kun taas tiedosto, jossa on isot kirjaimet Z (.Z), edustaa pakattua tiedostoa. Z-tiedostolla on useita sen tukemia versioita, kuten 2.0, 2.1, 4.5, 4.6. Eri Z-tiedostoversioissa on useita algoritmeja, joista suosituin on DEFLATE.




