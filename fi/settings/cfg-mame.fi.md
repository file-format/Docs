{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg-tiedosto",
"cfg mame -määritystiedosto",
"mikä on cfg-tiedosto",
"kuinka avata cfg-tiedosto",
"tiedosto",
"cfg tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-tiedostomuoto - MAME-määritystiedosto",
  "description": "Opi CFG MAME -määritystiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CFG-tiedostoja.",
  "linktitle": "CFG MAME",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-mame-fi",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Mikä on CFG-tiedosto?

CFG-tiedosto on MAME-arcade-videopeliemulaattorien käyttämä XML-näppäimistön määritystiedosto. Se on tärkeä osa näppäimistön säätimien ja pikanäppäimien mukauttamista pelaajan mieltymysten mukaan. Nämä tiedostot tallentavat kartoituksia ja asetuksia, jotka määrittävät näppäimistön ja emulaattorin vuorovaikutuksen pelin aikana. Muokkaamalla tätä tiedostoa käyttäjät voivat räätälöidä pelikokemustaan määrittämällä tiettyjä näppäimistön näppäimiä pelin sisäisiin toimintoihin, kuten kolikoiden asettamiseen, aloitukseen, siirtoon ja moniin muihin toimintoihin.

## MAME-määritystiedosto

MAME, joka tarkoittaa **Multiple Arcade Machine Emulator**, on ohjelmistosovellus, jonka avulla voit emuloida ja pelata arcade-pelejä tietokoneellasi. MAME käyttää konfiguraatiotiedostoja mukauttaakseen toimintaansa ja asetuksiaan. Nämä asetustiedostot sijaitsevat tavallisesti MAME-hakemistosi cfg-kansiossa.

Tässä ovat tärkeimmät määritystiedostot, joita saatat kohdata MAME:n asennuksen ja määrityksen yhteydessä:

1. **mame.ini:** Tämä on MAME:n pääasetustiedosto. Se sisältää globaaleja asetuksia, jotka koskevat kaikkia pelejä. Löydät tämän tiedoston MAME-asennuksesi juurihakemistosta.

1. **default.cfg:** Tämä tiedosto tallentaa oletusasetukset kaikille peleille, joilla ei ole omia asetustiedostoja. Sitä käytetään pelikohtaisten asetusten varana.

1. **game-specific.cfg:** Näitä tiedostoja käytetään yksittäisten pelien asetusten tallentamiseen. Ne on tyypillisesti nimetty ROM-tiedoston mukaan niiden vastaavien pelien mukaan. Jos sinulla on esimerkiksi peli nimeltä pacman.zip, sen asetustiedosto olisi pacman.cfg.

Tässä on joitain yleisiä asetuksia, jotka saatat löytää MAME-määritystiedostosta.

1. **rompath:** Määrittää hakemiston, jossa arcade-pelisi ROM-levyt sijaitsevat.

1. **cfg_directory:** Määrittää hakemiston, johon pelikohtaiset asetustiedostot tallennetaan.

1. **nvram_hakemisto:** Määrittää hakemiston, johon haihtumattomat RAM-tiedostot (NVRAM) tallennetaan. NVRAM tallentaa huipputuloksia ja muita pelikohtaisia tietoja.

1. **artwork_directory:** Määrittää hakemiston, johon kuvitustiedostot (kuten kehykset, telttakatokset ja lentolehtiset) tallennetaan.

1. **samplepath:** Määrittää hakemiston, jossa näyteäänitiedostot sijaitsevat.

1. **cheatpath:** Määrittää hakemiston, jossa huijaustiedostot sijaitsevat.

Voit myös määrittää useita muita asetuksia, kuten video- ja ääniasetuksia, säätimiä ja syöttölaitteita. Voit muokata näitä asetuksia avaamalla asetustiedoston tekstieditorissa ja tekemällä tarvittavat muutokset.

## MAME

MAME, joka tarkoittaa **Multiple Arcade Machine Emulator** on ohjelmistosovellus, joka on suunniteltu jäljittelemään ja kopioimaan vanhojen pelihallien ja arcade-pelikonsolien laitteistoa. Sen avulla käyttäjät voivat pelata laajaa kirjastoa klassisia arcade-pelejä nykyaikaisilla tietokoneilla ja muilla yhteensopivilla laitteilla. MAME on avoimen lähdekoodin projekti, ja siitä on tullut suosittu emulaattori pelihallipelien rikkaan historian säilyttämiseen ja nauttimiseen.

1. **Emulointi:** MAME:n ensisijainen tarkoitus on emuloida tarkasti pelihallien laitteistoa, mukaan lukien niiden keskusyksiköt (CPU:t), äänisirut, grafiikkasirut ja syöttölaitteet. Tämä tarkkuustaso varmistaa, että pelit toimivat mahdollisimman lähellä alkuperäistä arcade-kokemusta.

1. **Compatibility:** MAME supports wide range of arcade game ROMs, making it one of most comprehensive arcade emulators available. It can run games from various arcade platforms including classic games from '70s, '80s, '90s, and even some more recent arcade titles.

1. **Säilytys:** Yksi MAME:n tärkeimmistä tehtävistä on säilyttää pelihallipelien historia. Emuloimalla tarkasti pelihallilaitteistoa MAME auttaa estämään klassisten pelien katoamisen ja varmistaa, että tulevat sukupolvet voivat kokea ne alun perin tarkoitetulla tavalla.

1. **Käyttöliittymät:** Monet käyttäjät käyttävät käyttöliittymäsovelluksia, jotka tarjoavat graafisen käyttöliittymän pelien hallintaan ja käynnistämiseen MAME:n kautta. Nämä käyttöliittymät helpottavat navigointia MAME:n laajassa pelikirjastossa.

## Kuinka avata CFG -tiedosto?

Ohjelmat, jotka avaavat CFG-tiedostoja tai viittaavat niihin

- MAME (ilmainen) (Windows)
- ExtraMAME (kokeilu)
- MacMAME (MAC)

## Muut CFG-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cfg**-tiedostotunnistetta.

**Asetukset**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Peli**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Järjestelmä ja muut**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet
* [MAME](https://en.wikipedia.org/wiki/MAME)


