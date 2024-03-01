{
  "date": "2021-09-08",
  "keywords": [
"rel tiedosto",
"rel tiedostomuoto",
"mikä on rel-tiedosto",
"tiedosto",
"rel esimerkki",
"rel tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi REL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata REL-tiedostoja.",
  "title": "REL - Siirrettävä moduulitiedosto",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-re-fil"
}
},
  "lastmod": "2021-09-08"
}

## Mikä on REL-tiedosto?
Tiedostoa, jonka pääte on .rel, voidaan käyttää monenlaisiin tarkoituksiin. Siksi pelien luokittelussa se tunnetaan siirrettävänä moduulitiedostona, jota käyttävät jotkut Nintendo Wii -pelit, kuten Brawl, Super Smash Bros ja Mario Kart Wii. Se sisältää pelidatan, mukaan lukien hahmomallit ja vaiheet. REL-tiedostot toimivat samalla tavalla kuin Microsoft Windowsin käyttämät .DLL-tiedostot.

## REL-tiedostomuoto
REL-tiedostomuodossa tiedosto on jaettu useisiin osiin, jotka on ryhmitelty samanlaisilla käyttöoikeuksilla, esim. vain luku -tiedot yhdessä osiossa, kaikki suoritettava koodi sijoitetaan toiseen jne. Tiedosto alkaa otsikko-osalla, jota seuraa:
- Taulukko, joka sisältää osion tiedot.
- Osion tiedot.
- Muuttotiedot.

### Tiedoston otsikko
Tiedosto alkaa otsikolla, jonka koko on enintään 0x4C tavua:
| Offset | Koko | Kentän nimi | Kuvaus |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | seuraava | Osoitin seuraavaan moduuliin, täytetty ajon aikana. |
| 0x08 | 4 | edellinen | Osoitin edelliseen moduuliin, täytetty ajon aikana. |
| 0x0c | 4 | numSections | Tiedoston osioiden lukumäärä. |
| 0x10 | 4 | osioInfoOffset | Siirtymä osiotaulukon alkuun. |
| 0x14 | 4 | nameOffset | Siirtymä ASCII-merkkijonoon, joka sisältää moduulin nimen. Voi olla NULL. Suhteellinen REL-tiedoston alkuun. |
| 0x18 | 4 | nimiKoko | Moduulin nimen koko tavuina. |
| 0x1c | 4 | versio | REL-tiedostomuodon versionumero. |
| 0x20 | 4 | bssSize | .bss-osan koko. |
| 0x24 | 4 | relOffset | Siirretty siirtotaulukkoon. |
| 0x28 | 4 | impOffset | Offset imp-taulukkoon. |
| 0x2c | 4 | impSize | Imp-taulukon koko tavuina. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSection | Indeksoi osataulukkoon, johon bss on suhteellinen. Täytetty ajon aikana! |
| 0x34 | 4 | prolog | Siirto _prolog-funktion määritettyyn osaan. |
| 0x38 | 4 | epilog | Siirto _epilog-funktion määritettyyn osaan. |
| 0x3c | 4 | ratkaisematta | Siirto _unresolved-funktion määritettyyn osioon. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | Vain versio ≥ 3. Jos REL on linkitetty OSLinkFixediin (OSLinkin sijaan), tämän osoitteen jälkeistä tilaa voidaan käyttää muihin tarkoituksiin (kuten BSS). |

### Osion tietotaulukko
Osion tietotaulukko sisältää **numSections** -merkintää, jokainen 0x8 tavua pitkä:
| Offset | Koko | Kuvaus |
-------|------------|-------------|
| 0x0 | 30 bittiä | Siirto REL:n alusta jaksoon. Jos tämä on nolla, osa on alustamaton osa (eli .bss). |
| 0x3,6 | 1 bitti | Tuntematon. |
| 0x3,7 | 1 bitti | Suoritettava lippu; jos tämä on 1, osa on suoritettava. |
| 0x4 | 4 | Osion pituus tavuina. Jos tämä on nolla, tämä merkintä ohitetaan. |
| 0x8 | Seuraava merkintä | Seuraava merkintä |

### Siirtotiedot
Siirtotiedot ovat yksi tai useampia 0x8-tavuisten rakenteiden luetteloita. Kunkin luettelon loppu on merkitty erityisellä tyyppikoodilla 203:
| Offset | Nimi | Koko | Kuvaus |
-------|------------|------------|-----|
| 0x0 | offset | 2 | Poikkeama tavuina edellisestä siirrosta tähän. Jos tämä on osion ensimmäinen siirto, tämä on suhteessa osan alkuun. |
| 0x2 | tyyppi | 1 | Siirron tyyppi. Kuvailtu alla. |
| 0x3 | jakso | 1 | Symbolin osa, jota vastaan siirretään. Erikoissiirtotyypille 202 tämä on sen sijaan tämän tiedoston sen osan numero, jota seuraavat siirtomerkinnät koskevat. |
| 0x4 | lisää | 4 | Siirrettävä symboli tavuina suhteessa sen osan alkuun. Tämä on sen sijaan ehdoton osoite main.dol-sivuston siirroille. |
| 0x8 | Seuraava merkintä | Seuraava merkintä | Seuraava merkintä |


 



## Viitteet 

* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)



