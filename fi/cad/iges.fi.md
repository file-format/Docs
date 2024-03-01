{
  "date": "2020-03-16",
  "keywords": [
"IGES tiedosto",
"Tiedosto muoto",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi IGES-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata IGES-tiedostoja.",
  "title": "IGES-tiedostomuoto",
  "linktitle": "IGES",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-ige-fis"
}
},
  "lastmod": "2020-07-28"
}

## Mikä on IGES-tiedosto?

Tiedostoa, jonka pääte on .iges, käytetään suunnittelutietojen vaihtamiseen tietokoneavusteisten suunnittelusovellusten (CAD) välillä. IGES tulee sanoista Initial Graphics Exchange Specifications. IGES:n avulla vaihdettu tieto sisältää piirikaavion, rautalankakehyksen, vapaamuotoisen pinnan tai solid-mallinnusesitykset. IGES löytää sovelluksensa perinteisissä suunnittelupiirustuksissa, mallien analysoinnissa ja valmistustoiminnoissa. Formaatti voi vaihtaa sekä 2D- että 3D-suunnittelutietoja CAD-ohjelmien välillä. IGES-tiedostoja voidaan avata useilla CAD-sovelluksilla, kuten Autodesk ja CADSoftTools ABViewer. Saatavilla on myös useita sovellusliittymiä IGES-tiedostojen ohjelmalliseen avaamiseen ja muuntamiseen.

## IGES-tiedostomuoto

IGES-tiedostot ovat ASCII-tekstimuodossa, ja ne voidaan avata missä tahansa tekstieditorissa tiedoston sisällön tarkastelemiseksi. IGES-tiedoston tekstitiedot esitetään Hollerith-muodossa. Yleinen IGES-tiedosto voi sisältää tuhansia rivejä edustamaan 2D- tai 3D-tietoja, jotka voidaan vaihtaa tässä muodossa. IGES-tiedosto on jaettu viiteen osaan, jotka on merkitty erityisellä isolla kirjaimella 73. sarakkeessa. Nämä osiot ovat Aloita (S), Global (G), Data Entry (D), Parameter Data (P) ja Lopeta (T) -osiot. Tiedonsyöttö- ja parametritiedot-osista käytetään yleensä lyhennettä DE ja PD.

### IGES-tiedoston otsikko

Aloitus- ja Global-osiot sisältävät perustietoja seuraavista asioista:
 * Tiedoston nimi ja sen lähde
 * Parametritiedot -osion erottimet
 * Tiedoston tekijä ja muita yleisiä tietoja.

Aloitus- ja Global-osiot Wikipedian esimerkkidokumentista ovat seuraavat.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Tietojen syöttö (DE) ja parametritiedot (PD) -osio

#### Tietojen syöttö -osio
IGES-tiedosto koostuu useista kokonaisuuksista, jotka sisältävät tiedot IGES-tiedostomuodon perustiedoista. Entiteetti sisältää tietoa IGES-tietomuodon eri elementeistä ja sitä käytetään piirtämiseen. Yleisimmin käytettyjä kokonaisuuksia ovat:
 * Pyöreä kaari
 * Komposiittikäyrä
 * Kartiokaari
 * Lentokone
 * Linja

Nämä ovat vain muutamia, ja IGES:ssä on noin 150 erilaista kokonaisuutta. Jokainen entiteetti tunnistetaan tyyppinumerolla, kuten:
 * PYÖRÄKaari (tyyppi 100)
 * LINE (tyyppi 110)

##### Kokonaisuuden ominaisuudet

Jokaisella ilmoitetulla entiteetillä on seuraavat ominaisuudet.

|Kentän nimi|Kuvaus|
---|---|
|Entity Type |Tämä on kuvattavan kokonaisuuden tyyppi. Esimerkiksi 116 kuvaa pisteentiteettiä.|
|PD-osoitin |Tämä antaa tämän kokonaisuuden tietojen sijainnin Parametritiedot-osiossa. Tämä sijainti on yksinkertaisesti rivinumero PD-osion sisällä, jossa on tämän entiteettitietojen ensimmäinen rivi.|
|Rakenne |Nolla tai osoitin määritelmäkokonaisuuteen. Ei sovellu useimpiin kokonaisuuksiin|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 Ei kuviota määritetty (oletus) * 1 Tasainen * 2 Katkoviiva * 3 Phantom * 4 Keskiviiva * 5 Pisteviiva|
|Taso| Määrittää tähän entiteettiin yhdistettävät tasot. Sallii kokonaisuuden esiintymisen useammalla kuin yhdellä tasolla|
|Näytä| Määrittää katseluasetukset. Nämä ovat: 0 Ilmaisee yhtäläistä näkyvyyttä ja ominaisuuksia kaikissa näkymissä. Oletusosoitin näkymä-olioon (tyyppi 410), jota voidaan tarkastella Viittaus näkymän näkyvään assosiaatioolioon (tyyppi 402, lomake 3)
|Transformaatiomatriisiosoitin| Viittaa muunnosmatriisiolioon (tyyppi 124) tai on oletuksena nolla (ei muunnosa)|
|Label Display Associativity| Viittaa tarranäytön assosiatiivisuuteen (tyyppi 402, lomake 5), joka määrittää, kuinka entiteettitunniste näkyy.|
|Tilanumero| Sisältää neljä kahden numeron osaa. 1-2: Tyhjä tila. Joko 00 normaalille tai 01 tyhjälle. 3-4: Alayksikön kytkin: on 00 riippumattomalle, 01 fyysiselle riippuvaiselle, 02 loogiselle riippuvaiselle ja 03 molemmille. 5-6: Entity Use -lippu: on joko 00 geometrialle, 01 huomautukselle, 02 määritelmälle, 03 muulle, 04 loogiselle, 05 2D-parametrille ja 06 rakennusgeometrialle. Lopuksi 7-8 on hierarkia, jossa 00 tarkoittaa globaalia ylhäältä alaspäin (käytä tämän entiteetin ominaisuuksia), 01 on globaali lykkäys (älä käytä tämän entiteetin ominaisuuksia) ja 02 on käytä hierarkia -ominaisuutta (käytä hierarkiakokonaisuutta (tyyppi 406, muoto). 10)hierarkkisen ryhmittelyn ominaisuuksien määrittämiseksi).|
|Järjestysnumero| Määrittää D#, jossa # on tämän osan rivinumero (ei tiedoston yläosasta). Tätä käytetään myös osoittamaan tähän tiedonsyöttöyksikköön.|
|Entiteettityyppi| se määritetään kahdesti yksikkölistausta kohden|
|Line Weight Number| Määrittää paksuuden, kun kokonaisuutta näytetään. Pienin on 1, 0 on oletusarvo|
|Värinumero| Määrittää kokonaisuuden värin. Sallitut kokonaislukuarvot ovat: 0 Ei väriä (oletus) 1 Musta 2 Punainen 3 Vihreä 4 Sininen 5 Keltainen 6 Magenta 7 Syaani 8 Valkoinen|
|Parametri Line Count Number| Määrittää rivien määrän, jonka tämä entiteetti ottaa Parametritieto-osiossa|
|Lomakenumero| Ilmaisee tämän kokonaisuuden muodon tai esityksen. Muuttaa tapaa, jolla parametritiedot tulkitaan. Oletusarvo on 0|
|Varattu kenttä| Ei käytetty|
|Varattu kenttä| Ei käytetty|
|Entity Label| Sovellusmääritelty tunniste-oikeus perusteltu|
|Alaindeksinumero| Kokonaisuuden tunnisteen numeerinen tarkenne. Molemmat yhdessä muodostavat yksilöllisen tunnisteen kokonaisuudelle|
|Sekvenssinumero Katso yllä. |Tämä on D#+1, koska jokainen entiteetti on määritelty kahdella rivillä.|

#### Parametrin tietoosio
Tietojen syötteet -osaa seuraa Parametritiedot-osio. Se luettelee kunkin merkinnän tiedot ja luetteloi entiteetin parametrit Global-osiossa määritettyjen erottimien perusteella (yleensä pilkuilla parametrien erottamiseksi ja puolipisteellä listauksen lopettamiseksi).


## Viitteet
 * [IGES by WikiPedia](https://en.wikipedia.org/wiki/IGES)

