{
  "date": "2021-06-16",
  "keywords": [
"LZO",
"Komprimeret",
"Fil",
"Udvidelse",
"Filformat",
"Lempel-Ziv-Oberhume"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "LZO filformat",
  "description": "Lær om LZO filformat og API'er, der kan oprette og åbne LZO filer.",
  "linktitle": "LZO",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lz-dao"
}
},
  "lastmod": "2021-06-16"
}

## Hvad er en LZO fil? ##

En fil med filtypenavnet .lzo kombineres med filarkiveringsfunktioner, der kan reducere alle filstørrelser i den komprimerede fil. Alle de komprimerede filer kan omfatte en eller flere filer eller endda grupper af bindemidler med flere filer af forskellig art og dimensioner. Størrelsen af en komprimeret fil er mindre sammenlignet med den fælles størrelse af alle filer og mapper, der er gemt i en LZO-komprimeret fil. Alle LZO-komprimerede filer gemmes i LZO-formatet og udføres eksplicit med komprimeringsfunktioner, der bruges af LZOP-filkomprimerings- og dekomprimeringssoftwaren. Alle komprimeringsspecifikationerne er kombineret i dette filkomprimerings- og dekomprimeringsprogram, der stammer fra Lempel-Ziv-Oberhume-filkomprimeringsbiblioteket. Hurtigere dekompressionshastighed og udviklede kompressionsforhold kombineres også i disse LZO-filer.

## LZO-specifikation ##

Markus Franz Xaver Johannes Oberhumer developed the original "lzop" algorithm, based on earlier algorithms by Abraham Lempel and Jacob Ziv, in 1996. Dette bibliotek implementerer en række algoritmer med følgende egenskaber:

* Hurtigere komprimering end DEFLATE

* Hurtig dekompression

* Yderligere buffere, der er nødvendige under komprimering (på 8KB eller 64KB størrelse, afhængig af komprimeringsniveau)

* Kilde- og destinationsbufferne er al den hukommelse, der kræves til dekomprimering

* Giver kontrol over både kompressionsforhold og kompressionshastighed


Som en blokkomprimeringsalgoritme udfører LZO overlappende komprimering såvel som in-place dekompression. For at opnå overlappende komprimering skal blokstørrelsen af både komprimering og dekompression matche. LZO-komprimeringsalgoritmen opdeler inputdataene i match (en glidende ordbog) og bogstaver, der ikke stemmer overens, hvilket giver gode resultater med meget overflødige data og acceptable resultater med ikke-komprimerbare data, hvilket kun øger inkomprimerbare data med 1/64 af originalen størrelse.

## Problemer med at åbne en LZO-fil ##

Følgende er de få problemer, der kan forårsage dårlig funktion af LZO-filformat:
  
* Filen kan være korrupt. For at løse dette problem skal du downloade filen igen eller bede afsenderen om at sende filen igen
* Den anden grund er inficeret fil i dette tilfælde scan filen korrekt
* Ukorrekte links til LZO-filen
  *	 Removal of the description of the LZO 
* Ikke nok hardwareressourcer
* Forældede drivere til udstyret
  
## Referencer ##

* [LZO - Af Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Oberhumer)


