{
  "date": "2019-12-10",
  "keywords": [
"DIF",
"failu",
"pagarinājumu",
"faila formātā",
"Datu apmaiņas fails",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir DIF faila paplašinājums un API, kas var izveidot un atvērt DIF failus.",
  "title": "DIF - datu apmaiņas faila formāts",
  "linktitle": "DIF",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-di-lvf"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir DIF fails?

DIF apzīmē datu apmaiņas formātu, ko izmanto izklājlapu datu importēšanai/eksportēšanai starp dažādām lietojumprogrammām. Tajos ietilpst Microsoft Excel, OpenOffice Calc, StarCalc un daudzi citi. Tas saglabā datus vienā izklājlapā, kas ir vienīgais šī faila formāta ierobežojums.

## Īsa DIF faila formāta vēsture ##

DIF faila formātu astoņdesmito gadu sākumā izstrādāja Software Arts, Inc. DIF faila formāta specifikācijas tika iekļautas VisiCalc, kas bija pirmā izklājlapu programma personālajiem datoriem. Šīs specifikācijas tika aizsargātas ar autortiesībām 1981. gadā, un tās bija Software Arts Products Corp. reģistrēta preču zīme.

## DIF faila formāts ##

DIF uzglabā izklājlapas saturu ASCII teksta failā, kas ļauj to skatīt un rediģēt ar teksta redaktoru. Formātam ir sava vieta datu serializācijas formātu sarakstā, ņemot vērā datu apmaiņas raksturlielumus. DIF fails sastāv no 2 sadaļām; galvene un dati.

Viss DIF ir attēlots ar 2 vai 3 rindu daļu. Galvenes iegūst 3 rindu daļu; dati, 2.

* Virsrakstu daļas sākas ar teksta identifikatoru, kurā ir tikai lielie burti, tikai alfabēta rakstzīmes un mazāk nekā 32 burti. Nākamajai rindai ir jābūt skaitļu pārim, bet trešajai rindai jābūt pēdiņās.

* Datu gabali sākas ar skaitļu pāri, un nākamā rinda ir virkne pēdiņās vai atslēgvārds.


### Vērtības ###

Vērtība aizņem divas rindas, no kurām pirmā ir skaitļu pāris, bet otrā ir virkne vai atslēgvārds. Pirmais pāra cipars norāda veidu:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT — rindas sākums (rindas sākums)
** EOD – datu beigas
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – derīgs
** NA – nav pieejams
** ERROR – kļūda
** TRUE — patiesa Būla vērtība
** FALSE — viltus Būla vērtība
* 1 – virknes tips, otrais cipars tiek ignorēts, nākamā rinda ir virkne dubultpēdiņās


### DIF galvenes daļa ###

DIF faila galvenes daļa sastāv no identifikatora rindas, kam seko divas vērtības rindas. Skaitliskajās vērtībās galvenes daļās tiek izmantota tikai tukša virkne, nevis derīguma atslēgvārdi. Sīkāka informācija par šiem galvenes gabaliem ir šāda.

* TABULA - versijai seko skaitliska vērtība, vērtības otrajā rindā ir ģeneratora komentārs.

* VEKTORI - kolonnu skaits seko kā skaitliska vērtība

* TUPLES - rindu skaits seko kā skaitliska vērtība

* DATA — pēc fiktīvas skaitliskās vērtības 0, seko tabulas dati, katrai rindai priekšā ir BOT vērtība, visa tabula beidzas ar EOD vērtību.


### DIF piemērs ###

Nākamajā piemērā ir parādīts vienkāršas darblapas saturs un tai līdzvērtīgs DIF attēlojums.


|Vārds|Vecums
---|---|
|Bobs|34
|Loksne|22

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

## Atsauces Nr.

* [ DIF — Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)


