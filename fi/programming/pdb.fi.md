{
  "date": "2019-10-11",
  "keywords": [
"pdb-tiedosto",
"pdb",
"laajennus",
"muoto",
"Mikä on pdb-tiedosto",
"pdb-tiedostomuoto",
"ATE:n metatiedot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDB-tiedostomuoto - Ohjelmatietokantatiedosto",
  "description": "Opi PDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PDB-tiedostoja.",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pd-fib"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on PDB-tiedosto?

Tiedosto, jonka tunniste on .pdb, on ohjelmatietokantatiedosto, joka sisältää käännetyn suoritettavan tiedoston (EXE/DLL) virheenkorjaustiedot. Microsoft Compilers luo PDB-tiedostot, kun sovellusohjelma käännetään virheenkorjaustilassa. PDB-tiedoston läsnäolo voi auttaa suoritettavan tiedoston käänteisessä suunnittelussa, koska se sisältää merkittävää tietoa kaikista moduulien symboleista. Tästä syystä nämä tiedostot pidetään erillään lopullisesta suoritettavasta tiedostosta. Microsoftin [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) voi avata PDB-tiedoston saadakseen tietoja, kuten julkisia ja vientitietoja, globaaleja symboleja, paikallisia symboleja, tyyppitietoja, lähdetiedostoja ja rivinumeroita.

## PDB-tiedostomuoto

PDB on Microsoftin oma tiedostomuoto, eikä sitä ole vielä virallisesti dokumentoitu missään. Aloitusdokumentaatio on kuitenkin saatavilla {{HYPERLINKKI}}, ja siihen voi viitata.

### ATE-virrat

PDB-tiedostot koostuvat useista virroista, joissa jokainen virta toimii virtuaalisena yksittäisenä tiedostona ja sisältää tietoja. PDB-tiedostojen kirjoittajat voivat kirjoittaa näihin tiedostoihin ja tiedosto viimeistellään vasta, kun nimenomainen sitoumus on annettu. Kääntäjä voi jatkaa kirjoittamista PDB-tiedostoon, mutta sitoutuu vain, jos kaikki käyttäjäkoodi käännetään onnistuneesti. PDB-tiedosto koostuu seuraavista virroista:

|Stream nro |Sisältö |Lyhyt kuvaus|
---|---|---|
|1| Pdb (otsikko) |Versiotiedot ja tiedot tämän ATE:n liittämiseksi EXE-tiedostoon|
|2| Tpi (Type Manager) |Kaikki suoritettavassa tiedostossa käytetyt tyypit.|
|3| Dbi (virheenkorjaustiedot) |Säilyttää osion lisäykset ja luettelon 'Modit'|
|4| Nimikartta| Sisältää tiivistetyn merkkijonotaulukon|
|4-(n+4)| n Mod's (Moduulitiedot)| Jokainen Mod-virta sisältää symboleja ja rivinumeroita yhdelle käännökselle|
|n+4| Globaali symboli hash| Hakemisto, joka mahdollistaa haun maailmanlaajuisista symboleista nimellä|
|n+5| Julkinen symboli hash| Hakemisto, joka mahdollistaa haun julkisista symboleista osoitteiden mukaan|
|n+6| Symbolitietueet| Globaalien ja julkisten symbolien todelliset symbolit|
|n+7| Kirjoita hash| TPI-virran käyttämä tiiviste.|

Jokainen PDB-tiedoston virta koostuu useista sivuista, joita ei välttämättä numeroida peräkkäin.

### ATE:n otsikko

PDB-tiedostossa on otsikko, joka koostuu allekirjoituksesta tietyn muodon tunnistamiseksi ja vahvistamiseksi. Allekirjoituksen pituus riippuu ATE-muodosta. Otsikko voi olla pidempi kuin yksi sivu.

### ATE:n metatiedot
The PDB metadata is responsible to recognize all of the component streams, giving the length, and sequence of pages for each stream. Orders are given to streams consecutively; starting with 0. Siellä on myös järjestämätön juurivirta, joka sisältää osan metatiedoista.

## Viitteet
 * [PDB – Wikipedia](https://en.wikipedia.org/wiki/Program_database)
 * [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

