{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"Amazon lappušu numuru indekss",
"pagarinājumu",
"failu",
"formātā",
"e-grāmata",
"Amazon Kindle"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par Amazon APNX faila formātu un API, kas var izveidot un atvērt APNX failus.",
  "title": "APNX — Amazon lappušu numuru indekss",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-lvx"
}
},
  "lastmod": "2021-05-28"
}

## Kas ir APNX fails? ##

Amazon lappušu numura indeksa fails, kurā tiek izmantots .apnx paplašinājums, ir e-grāmatas faila tips; izmanto Amazon Kindle. Šie faili faktiski ir pazīstami kā lappušu faili, ko izmanto Kindle ierīces. Tātad APNX faili parasti tiek izveidoti, lai atzīmētu Kindle e-grāmatu lapas. Lapu pārslēgšanas funkcija Amazon Kindle ierīcēs ir sākta kopš tās 3.1 programmaparatūras. Tas meklē lappušu indeksus APNX failā un pēc tam kartē to ar lappušu numuriem oriģinālajā drukas grāmatā. Šie faili tiek saglabāti Kindle ierīcēs kopā ar Amazon eBooks failiem. Jūs nevarat atvērt vai rediģēt APNX failus.

## APNX faila formāta specifikācijas ##

### Izkārtojums

|baiti| saturs| komentāri|
---|---|---|
|4 |00010001 | Formāta identifikators. Vērtība 65537 little-endian.|
|4 |nākamā sākums | Nobīde pēc pirmās galvenes atrašanās vietas beigām. Sāk jaunu virsraksta informācijas secību|
|4 |garums| Pirmās galvenes garums|
|N |pirmā galvene | Virkne, kas satur satura galveni. Tas sāk nākamo secību|
|2 |nezināms | Vienmēr 1|
|2 |garums | Otrās galvenes garums|
|2 |lappušu skaits | Kopējais baitu skaits pēc otrās galvenes, kas apzīmē lapas. Šajā summā ir iekļauti baiti, kurus lapas karte ignorē.|
|2 |nezināms | Vienmēr 32|
|N |otrā galvene | Virkne, kas satur lapas kartēšanas galveni|
|4*N |polsterējums | Pirmais cipars, kas norādīts lapas kartēšanas galvenē, norāda 0 baitu skaitu.|
|4*N |lapu saraksts ||

### Satura galvene

Satura galvene sastāv no virknes, kas ir ietverta {} un satur atslēgu, vērtību pārus:

|saturs| komentāri|
---|---|
|contentGuid| Ceļvedis.|
|asin | Amazon identifikators grāmatas Kindle versijai.|
|cdeType | MOBI cdeType. E-grāmatām vienmēr jābūt EBOK.|
|fileRevisionId | Šī faila pārskatīšana.|

#### Piemērs
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Lapas kartēšanas galvene
Lapas kartēšanas galvene sastāv no virknes, kas ir ietverta {} un satur atslēgu, vērtību pārus.

|saturs | komentāri|
---|---|
|asin | ISBN 10 papīra grāmatai, kurai lapas atbilst|
|lapas karte| Trīs vērtību kortežs. Izskatās šādi: (N,N,N)\
1) baitu skaits pēc galvenes, kas sāk lappušu numerācijas secību\
2) nezināms\
3) nezināms\|
#### Piemērs
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Lapu saraksts

Lapu saraksts ir nobīdes secība neapstrādātā HTML. Katrs
vērtība ir jaunas lapas sākums. Katrs ieraksts ir 4 baitu lielais endians
starpt.



## Atsauces

* [Amazon APNX faila formāts](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX — MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)


