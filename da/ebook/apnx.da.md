{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"Amazon sidetalsindeks",
"udvidelse",
"fil",
"format",
"e-bog",
"Amazon Kindle"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om Amazon APNX-filformat og API'er, der kan oprette og åbne APNX-filer.",
  "title": "APNX - Amazon Sidetal Index",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-dax"
}
},
  "lastmod": "2021-05-28"
}

## Hvad er APNX fil? ##

Amazon Page Number Index-filen, som bruger filtypen .apnx, er en e-bogsfiltype; brugt af Amazon Kindle. Disse filer er faktisk kendt som pagineringsfiler, der bruges af Kindle-enheder. Så APNX-filerne er typisk oprettet for at markere siderne i Kindle eBooks. Pagineringsfunktionen er startet på Amazon Kindle-enheder siden dens 3.1 firmware. Den ser i APNX-filen for sideindekser og kortlægger den derefter med sidetallene i den originale trykte bog. Disse filer gemmes på Kindle-enheder sammen med Amazon eBooks-filer. Du kan ikke åbne eller redigere APNX-filerne.

## APNX filformatspecifikationer ##

### Layout

|bytes| indhold| kommentarer|
---|---|---|
|4 |00010001 | Formater identifikator. Værdi af 65537 little-endian.|
|4 |start af næste | Forskydningen efter slutplaceringen af den første sidehoved. Starter en ny sekvens af header info|
|4 |længde| Længde af første overskrift|
|N |første overskrift | Streng, der indeholder indholdsoverskrift. Det starter næste sekvens|
|2 |ukendt | Altid 1|
|2 |længde | Længde af anden sidehoved|
|2 |sideantal | Samlet antal bytes efter anden sidehoved, der repræsenterer sider. Denne sum inkluderer bytes, der ignoreres af pageMap.|
|2 |ukendt | Altid 32|
|N |anden sidehoved | Streng, der indeholder sidemapping-headeren|
|4*N |polstring | Det første tal angivet i sidemapping-headeren angiver antallet af 0 bytes.|
|4*N |sideliste ||

### Indholdsoverskrift

Indholdsoverskriften består af en streng omsluttet af {}, der indeholder nøgleværdipar:

|indhold| kommentarer|
---|---|
|contentGuid| Vejl.|
|asin | Amazon-id for Kindle-versionen af bogen.|
|cdeType | MOBI cdeType. Bør altid være EBOK for e-bøger.|
|filRevisionId | Revision af denne fil.|

#### Eksempel
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Side Mapping Header
Sidetilknytningshovedet består af en streng omsluttet af {}, der indeholder nøgleværdipar.

|indhold | kommentarer|
---|---|
|asin | ISBN 10 for papirbogen siderne svarer til|
|sideKort| Tupel med tre værdier. Ser ud som: (N,N,N)\
1) Antal bytes efter sidehoved, der starter sidenummereringssekvensen\
2) ukendt\
3) ukendt\|
#### Eksempel
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Sideliste

Sidelisten er en sekvens af forskydninger i den rå HTML. Hver
værdi er starten på en ny side. Hver post er en 4 byte stor endian
int.



## Referencer

* [Amazon APNX-filformat](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX - af MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)


