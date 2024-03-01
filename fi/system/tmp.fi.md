{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"laajennus",
"tiedosto",
"muoto",
"järjestelmä",
"TMP-tiedosto",
"TMP-asiakirjat",
"TMP-tiedostot",
"Väliaikainen tiedosto",
"sovellus",
"ohjelmia"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP - Väliaikainen tiedostomuoto",
  "description": "Opi TMP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TMP-tiedostoja.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-fip"
}
},
  "lastmod": "2021-07-15"
}

## Mikä on TMP-tiedosto? ##

TMP-tiedosto viittaa väliaikaiseen varmuuskopioon, tallennustilaan tai muuhun ohjelmiston luomaan tiedostojärjestelmään. Se luodaan toisinaan näkymättömänä tiedostona ja tuhoutuu usein, kun ohjelma suljetaan. TMP-tiedostoja voidaan käyttää myös tietojen väliaikaiseen tallentamiseen uuden tiedoston luomisen aikana.

## TMP-tiedostomuoto ##

TMP-tiedosto koostuu tyypillisesti raakatiedoista, joita käytetään vaiheena materiaalin muuntamisessa tyylistä toiseen. Microsoft Word ja Apple Safari ovat kaksi sovellusta, jotka voivat tuottaa ja käyttää TMP-tiedostomuotoa.

Luodut TMP-asiakirjat pitäisi teoriassa poistaa automaattisesti, kun ohjelma suljetaan tai kone sammutetaan. Käytännössä näin ei aina ole. Seurauksena on, että kun selaat ohjelman asiakirjoja, saatat törmätä ohimeneviin tiedostoihin, joita järjestelmä tai mikään muu ohjelmisto ei käytä aktiivisesti.

### Apumuisti ###

Virtuaalimuistia käytetään käyttöjärjestelmissä, mutta suuria tietomääriä käyttävät ohjelmat saattavat joutua tekemään väliaikaisia asiakirjoja.

### Prosessien välinen viestintä ###

Useimmat käyttöjärjestelmät tarjoavat primitiivit tiedon siirtämiseen ohjelmien välillä, kuten putkien, pistorasioiden tai keskusmuistin, mutta yksinkertaisin tapa on siirtää tiedostot väliaikaiseen tiedostoon ja ilmoittaa vastaanottavalle sovellukselle väliaikaisen tiedoston sijainti.


## Tekniset tiedot ##

Erottuvien väliaikaisten asiakirjojen nimien saaminen tapahtuu yleensä käyttöjärjestelmissä ja ohjelmistoissa.
Väliaikaisia tiedostoja voidaan turvallisesti luoda POSIX-järjestelmissä käyttämällä mkstemp- tai tmpfile-kirjastotoimintoja. Joissakin järjestelmissä on edellinen POSIX (silloin poistunut) mktemp-sovellus. Nämä tiedostot löytyvät yleensä Unix-alustojen tavallisesta väliaikaisesta hakemistosta /TMP:stä tai %TEMP%:sta (se on erityinen sisäänkirjautumiselle) Windows-koneissa.

Kun ohjelma pysähtyy tai asiakirja suljetaan, tmp-tiedoston avulla luotu ohimenevä tiedosto poistetaan automaattisesti. GetTempFileName (Windows) tai tmpnam (POSIX) avulla voidaan luoda väliaikainen tiedostonimi, joka kestää kauemmin kuin sen luonut ohjelma.

## Viite ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
