{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi ACCDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ACCDB-tiedostoja.",
  "title": "ACCDB-tiedostomuoto - Microsoft Access 2007 -tietokantatiedosto",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-fib"
}
},
  "lastmod": "2020-11-12"
}

## Mikä on ACCDB-tiedosto?

Tiedosto, jonka pääte on .accdb, on Microsoft Access 2007 -tietokantatiedosto, joka tallentaa käyttäjien tiedot taulukoihin. Se tukee varastointia
mukautetut lomakkeet, SQL-kyselyt ja muut tiedot. ACCDB-tiedostot korvasivat [MDB](/database/mdb/)-tiedostot Microsoftin siirtyessä käyttämään XML-pohjaista tiedostorakennetta. ACCDB-tiedostot voidaan edelleen muuntaa MDB: ksi vanhalla yhteensopivuudella. ACCDB on kuitenkin nykyään laajalti käytetty Access-tietokantatiedostomuoto. Microsoft tuki myös lisäominaisuuksia ACCDB-muodossa, kuten mahdollisuutta tallentaa liitetiedostoja, binaaridataa ja moniarvoista kenttätukea.

## ACCDB tiedostomuoto

Kuten MDB, ACCDB-tiedostomuodolle ei ole saatavilla julkisia määrityksiä. Microsoft tukee näiden tiedostojen ohjelmointia Open Database Connectivity (ODBC) -standardin ja Visual Basic for Applications (VBA) -standardin kautta.

### Oivallus

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. ACCDB-tiedostoissa tämä ilmaisin näyttää heijastavan tiedoston yhteensopivuutta eikä sen luomiseen käytetyn ACE-moottorin versiota.

## Viitteet

* [Access 2016 -tiedot](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [Mitä Access-tiedostomuotoa minun pitäisi käyttää?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


