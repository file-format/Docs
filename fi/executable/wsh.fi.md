{
  "date": "2021-08-27",
  "keywords": [
"wsh-tiedosto",
"wsh-tiedostomuoto",
"mikä on wsh-tiedosto",
"tiedosto",
"wsh esimerkki",
"wsh tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi WSH-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WSH-tiedostoja.",
  "title": "WSH - Windowsin komentosarjatiedosto",
  "linktitle": "WSH",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ws-fih"
}
},
  "lastmod": "2021-08-27"
}

## Mikä on WSH-tiedosto?
Tiedosto, jonka pääte on .wsh, sisältää ominaisuuksia ja parametreja tietylle ohjelmointikielen skriptille, kuten VB tai VBS jne. WSH:n varsinainen tarve on käyttää niitä tiettyjen komentosarjojen suorituksen mukauttamiseen. WScript tai CScript vaaditaan suorittamiseen, ja molemmat sisältyvät Windows-käyttöjärjestelmään. WSH-tiedostot toimitettiin alun perin Windows 95:ssä asennuslevyillä valinnaisena konfiguroitavana ja asennettavana Ohjauspaneelia varten ja sitten Windows 98:n oletuskomponenttina.

## WSH tiedostomuoto
WSH:ta (Windows Script Host) voidaan käyttää useisiin tarkoituksiin, mukaan lukien hallintaan, kirjautumiskomentosarjaan ja yleiseen automaatioon. WSH luo ympäristön skriptien suorittamista varten. se kutsuu sopivan komentosarjamoottorin ja varaa joukon palveluita ja objekteja skriptille. Näitä komentosarjoja voidaan ajaa GUI-tilassa COM-objektista tai komentorivitilassa, mikä tarjoaa käyttäjälle joustavuutta sekä interaktiivisille että ei-vuorovaikutteisille komentosarjoille.

### Esimerkkejä
Tässä on hyvin yksinkertainen esimerkki, joka näyttää jonkin VBScriptin, joka käyttää juuri WSH COM -objektia WScript näyttääkseen viestin OK-painikkeella. Kun tämä komentosarja käynnistetään, CScript- tai WScript-moottori kutsutaan ja ajonaikainen ympäristö perustetaan.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Viitteet 

* [Windows Script Host - Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)




