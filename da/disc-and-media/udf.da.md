{
  "date": "2021-08-17",
  "keywords": [
"udf fil",
"udf filformat",
"hvad er en udf-fil",
"fil",
"udf eksempel",
"udf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om UDF-filformat og API'er, der kan oprette og åbne UDF-filer.",
  "title": "UDF - Universal Disk Format File",
  "linktitle": "UDF",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-ud-daf"
}
},
  "lastmod": "2021-08-17"
}

## Hvad er UDF fil?
Filen med filtypenavnet .udf er et diskbilledformat, der typisk bruges til at gemme filer på optiske medier; kan bruges til at brænde dvd'er, cd'er og andre optiske medier; gemmer en samling af filer ved hjælp af mappestrukturen specificeret i UDF-standarden; tillader filer at blive slettet og ændret på måldisken, selv efter at de er blevet skrevet. Optical Storage Technology Association satte UDF-filsystemet som en standard for at danne et fælles filsystem for alle optiske medier, såsom for genskrivbare optiske medier og skrivebeskyttede medier.

## UDF filformat 
UDF-filformatet er et åbent leverandørneutralt filsystem til lagring af computerdata til en bred vifte af medier. Det har været almindeligt brugt til dvd'er og nyere optiske diskformater. Normalt mestrer softwaren et UDF-filsystem i en batch-proces og skriver det til optiske medier i en enkelt omgang. Men når den skriver pakker til genskrivbare medier, tillader UDF filer at blive oprettet, slettet og ændret på disken svarende til et almindeligt filsystem ville gøre på flytbare medier som flashdrev eller disketter.
### UDF-specifikationer
UDF-standarden definerer følgende tre filsystemvariationer:

- **Almindelig bygning**: Dette er det originale format, der understøttes i alle UDF-revisioner. Det blev introduceret i den første version af standarden, dette format kan bruges på enhver type disk, der muliggør tilfældig læse- eller skriveadgang, såsom DVD+RW, harddiske og DVD-RAM-medier.
- **VAT build**: Used specifically for writing to write-once media. The VAT is an additional structure on the disc that allows packet writing; that is, remapping physical blocks when files or other data on the disc are modified or deleted. For write-once media, the entire disc is virtualized, making the write-once nature transparent for the user; the disc can be treated the same way one would treat a rewritable disc.
- **Spared (RW) build**: Bruges specifikt til at skrive til genskrivbare medier. Det tilføjer en ekstra sparetabel til at håndtere de fejl, der i sidste ende vil opstå på dele af disken, der er blevet omskrevet flere gange. Denne tabel gemmer spor af slidte sektorer og omformer dem til arbejdende. Defektstyringen af UDF gælder ikke for systemer, der allerede implementerer en anden form for defektstyring, såsom Mount Rainier (MRW) til optiske diske eller en diskcontroller til en harddisk.
 



## Referencer 

* [Windows Imaging Format - af Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)



