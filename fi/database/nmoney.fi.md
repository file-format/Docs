{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi NMONEY-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NMONEY-tiedostoja.",
  "title": "NMONEY-tiedosto - Denaro-tilin tiedostomuoto",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmone-fiy"
}
},
  "lastmod": "2023-05-17"
}

## Mikä on NMONEY-tiedosto?

NMONEY-tiedosto on taloustietojen tallennustietokantatiedosto, joka sisältää tallenteet rahoitustapahtumista. Sen on kehittänyt Nickvision, ja sitä käytettiin Nickvision Denaro -ohjelmistossa, joka on henkilökohtainen talousohjelmistosovellus. NOMONEY-tiedostoon tallennetut tiedot sisältävät tilin luotto- ja veloitustapahtumat.

NOMONEY-tiedostot voidaan avata [Github](https://github.com/NickvisionApps/Denaro)-sovelluksella.

## Tietoja Denaro Softwaresta

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Denaron tarjoamat ominaisuudet

 * Hallitse useita tilejä samanaikaisesti suosituimmalla ja tutuimmalla välilehtiliittymällä
 * Suodata tapahtumat tyypin, ryhmän tai päivämäärän mukaan
 * Toista tapahtumat, kuten laskut, jotka tapahtuvat joka kuukausi
 * Siirrä rahaa tililtä toiselle
 * Vie tiedot tililtä CSV-tiedostona ja tuo CSV-, OFX- tai QIF-tiedosto tapahtumien lisäämiseksi tilille

## Denaro-tiedostomuoto - lisätietoja

Denaro-tiedostot tallennetaan levylle binääritiedostomuodossa. Taloustiedot tallennetaan tietokantatiedostona **.SQLITE3**-tiedostomuodossa. SQLITE on kevyt SQL-tietokantatiedosto, joka on luotu SQLite-ohjelmistolla. Se tarjoaa itsenäisen tietokantamoottorin, joka pystyy tarjoamaan täysin varustellun ja erittäin luotettavan tietokannan. SQLite-tietokantatiedostoja voidaan käyttää monipuolisen sisällön jakamiseen järjestelmien välillä yksinkertaisesti vaihtamalla nämä tiedostot verkon yli. SQLite-sidoksia on olemassa ohjelmointikielille, kuten C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/) ja monille muille.

## Viitteet

 * [Nickvision](https://nickvision.org/)
 * [NIckVision – Github](https://github.com/NickvisionApps/Denaro)

