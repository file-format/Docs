{
  "date": "2021-07-12",
  "keywords": [
"cmd tiedosto",
"mikä on cmd-tiedosto",
"tiedosto",
"cmd esimerkki",
"cmd tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi CMD-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CMD-tiedostoja.",
  "title": "CMD - Windowsin komentotiedostomuoto",
  "linktitle": "CMD",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cm-fid"
}
},
  "lastmod": "2021-07-12"
}

## Mikä on CMD-tiedosto?
CMD-tiedosto koostuu komentosarjasta, joka sisältää yhden tai useita komentoja pelkkänä tekstinä, jotka suoritetaan eri tehtävien suorittamiseksi. Se on samanlainen kuin [BAT](/executable/bat/)-tiedosto, jota käytetään yleensä myös suoritettavien komentojen erän tallentamiseen. CMD-tiedostoja käytetään laajalti Microsoft Windows -käyttöjärjestelmässä. Nämä tiedostot esiteltiin melkein 90-luvulla, mutta niitä käytettiin edelleen uusimmassa Windows-käyttöjärjestelmässä. Nämä tiedostot on yleensä kirjoitettu suorittamaan useampi kuin yksi komento peräkkäin.

## CMD-tiedostomuoto
CMD on tiedostomuoto, jota käyttävät CP/M-tyyliset suoritettavat ohjelmat. Se on yleensä verrattavissa [COM](/executable/com/):aan CP/M-80:ssa ja [EXE](/executable/exe/):ään DOS:ssa. CMD-tiedosto sisältää 1–8 koodi- tai dataryhmää ja 128-tavun otsikon. Jokainen ryhmä voi olla kooltaan enintään 1 mb. CMD-tiedostot voivat sisältää myös siirtotietoja ja RSX:itä (Resident System Extensions) sen myöhemmissä versioissa. CMD on uusi tulokas verrattuna tiedostoon [BAT](/executable/bat/); käytetty MS-DOS:ssa ennen ikkunoiden julkaisua MS-DOSissa. Vaikka voit edelleen tallentaa tiedostoja .bat-tunnisteella, monet käyttävät .cmd-tunnistetta suoritettavien komentosarjojen tallentamiseen.

### CMD-muodon erittely

Otsikon alku sisältää luettelon tiedostossa olevista ryhmistä ja niiden tyypeistä. Jokaista tyyppiä voidaan käyttää enintään kerran. Nämä tyypit ovat:

- Koodi
- Dataa
- Ylimääräistä
- Pinoa
- Käyttäjä 1
- Käyttäjä 2
- Käyttäjä 3
- Käyttäjä 4
- Jaettu koodi

Samoin Ohjelmasegmentin etuliite DOS:ssa, tietoryhmän ensimmäiset 256 tavua ovat nollia. Ne täytetään CP/M-86:lla nollasivulla. Jos tietoryhmää ei ole, käytetään koodiryhmän ensimmäisiä 256 tavua.
## Esimerkki CMD-tiedostosta
Seuraavassa on esimerkki CMD-komentosarjasta järjestelmätietojen näyttämiseksi.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Viitteet 

* [CMD-skriptin kirjoittaminen](https://smallbusiness.chron.com/write-cmd-script-53226.html)

* [CMD-tiedosto (CP/M) - Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))


