{
  "date": "2020-11-11",
  "keywords": [
"ACCDB",
"pratęsimas",
"failą",
"Dokumento formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"Duomenų bazės failai"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie ACCDB failo formatą ir API, kurios gali kurti ir atidaryti ACCDB failus.",
  "title": "ACCDB failo formatas – „Microsoft Access 2007“ duomenų bazės failas",
  "linktitle": "ACCDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-accd-ltb"
}
},
  "lastmod": "2020-11-12"
}

## Kas yra ACCDB failas?

Failas su plėtiniu .accdb yra Microsoft Access 2007 duomenų bazės failas, kuriame saugomi vartotojų duomenys lentelėse. Tai palaiko saugojimą
pasirinktines formas, SQL užklausas ir kitus duomenis. Microsoft perėjus prie XML pagrįstos failų struktūros, ACCDB failai pakeitė [MDB](/database/mdb/) failus. ACCDB failus vis tiek galima konvertuoti į MDB su senu suderinamumu. Tačiau ACCDB dabar yra plačiai naudojamas Access duomenų bazės failo formatas. Microsoft taip pat palaikė papildomas ACCDB formato funkcijas, tokias kaip galimybė saugoti failų priedus, dvejetainius duomenis ir daugiareikšmio lauko palaikymą.

## ACCDB failo formatas

Kaip ir MDB, ACCDB failo formatui nėra viešų specifikacijų. Microsoft palaiko prieigą prie šių failų programiškai naudojant Open Database Connectivity (ODBC) standartą ir Visual Basic for Applications (VBA).

### Įžvalga

A hex dump of a simple ACCDB file suggests that there are general similarities in structure to the latest versions of the predecessor MDB Format Family. Both file formats use fixed page sizes of 4096 bytes. Another similarity between ACCDB and MDB is the form of the magic number, which includes the string "Standard ACE DB" for ACCDB. A version or compatibility code is in the same location in both formats. The mdbtools | HACKING file states "Offset 0x14 contains the Jet version of this database" and The unofficial MDB Guide concurs. The information in these sources, combined with Wikipedia entry for [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine), suggests that a value of 0x02 indicates ACE 12 (Access 2007) and 0x03 indicates ACE 14 (Access 2010). However, a minimal database created in Access 2010 and a similar one created in Access 2016 both have 0x02 in this location. A minimal database created in Access 2016, but defining a column with the newly introduced "large integer" data type, had a value of 0x05. ACCDB failuose šis indikatorius rodo failo suderinamumą, o ne ACE variklio, naudoto jam sukurti, versiją.

## Nuorodos

* [2016 m. prieigos specifikacijos] (https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)

* [Microsoft Jet Database Engine](https://en.wikipedia.org/wiki/Microsoft_Jet_Database_Engine)

* [Kokį Access failo formatą turėčiau naudoti?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617- be66f9070b41)


