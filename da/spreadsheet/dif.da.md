{
  "date": "2019-12-10",
  "keywords": [
"DIF",
"fil",
"udvidelse",
"filformat",
"Dataudvekslingsfil",
"Regneark"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Din filformatguide for at vide, hvad en DIF filtypenavn og API'er er, der kan oprette og åbne DIF-filer.",
  "title": "DIF - Data Interchange File Format",
  "linktitle": "DIF",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-di-daf"
}
},
  "lastmod": "2019-12-10"
}

## Hvad er en DIF fil?

DIF står for Data Interchange Format, der bruges til at importere/eksportere regnearksdata mellem forskellige applikationer. Disse omfatter Microsoft Excel, OpenOffice Calc, StarCalc og mange andre. Det gemmer data indeholdt i et enkelt regneark, hvilket er den eneste begrænsning af dette filformat.

## Kort historie om DIF-filformat ##

DIF-filformatet blev udviklet af Software Arts, Inc. i begyndelsen af 1980'erne. Filformatspecifikationerne for DIF var inkluderet i VisiCalc, som var det første regnearksprogram til personlige computere. Disse specifikationer var ophavsretligt beskyttet i 1981 og var et registreret varemærke tilhørende Software Arts Products Corp.

## DIF-filformat ##

DIF gemmer regnearksindhold i ASCII-tekstfil, der gør det muligt at se og redigere det med en teksteditor. Formatet ejer sin plads på listen over dataserialiseringsformater for dets karakteristika for dataudveksling. En DIF-fil består af 2 sektioner; en overskrift og data.

Alt i DIF er repræsenteret af en 2- eller 3-linjers chunk. Overskrifter får en 3-linjers chunk; data, 2.

* Overskriftsstykker starter med en tekstidentifikator, der består af store bogstaver, kun alfabetiske tegn og mindre end 32 bogstaver. Den følgende linje skal være et par tal, og den tredje linje skal være en citationsstreng.

* Datastykker starter med et talpar, og den næste linje er en citationsstreng eller et nøgleord.


### Værdier ###

En værdi optager to linjer, den første et par tal og den anden enten en streng eller et nøgleord. Det første tal i parret angiver typen:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT – begyndelsen af tuple (start af række)
** EOD – slutningen af data
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – gyldig
** NA – ikke tilgængelig
** FEJL – fejl
** TRUE – ægte boolesk værdi
** FALSK – falsk boolesk værdi
* 1 – strengtype, det andet tal ignoreres, den følgende linje er strengen i dobbelte anførselstegn


### DIF Header chunk ###

Header-delen af en DIF-fil består af en identifikationslinje efterfulgt af de to linjer i en værdi. De numeriske værdier i overskriftsstykker bruger kun en tom streng i stedet for gyldighedsnøgleordene. Detaljerne for disse overskriftsstykker er som følger.

* TABEL - en numerisk værdi følger af versionen, den udgåede anden linje af værdien indeholder en generatorkommentar

* VEKTORER - antallet af kolonner følger som en numerisk værdi

* TUPLER - antallet af rækker følger som en numerisk værdi

* DATA - efter en dummy 0 numerisk værdi følger dataene for tabellen, hver række efterfulgt af en BOT-værdi, hele tabellen afsluttet med en EOD-værdi


### DIF-eksempel ###

Følgende eksempel viser indholdet af et simpelt regneark og dets tilsvarende DIF-repræsentation.


|Navn|Alder
---|---|
|Bob|34
|Sheet|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## Referencer ##

* [ DIF - Af Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)


