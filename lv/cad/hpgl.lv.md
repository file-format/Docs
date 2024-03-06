{
  "date": "2020-07-28",
  "keywords": [
"HPGL",
"Faila formāts",
"Atvērt",
"Lasīt",
"Izveidot",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par HPGL failu formātu un API, kas var izveidot un atvērt HPGL failus.",
  "title": "HPGL faila formāts — mācieties no failu formātu ekspertiem!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpg-lvl"
}
},
  "lastmod": "2020-07-28"
}

## Kas ir HPGL fails?

HPGFL (Hewlett-Packard Graphics Language) failā ir HP izstrādāta instrukciju kopa plotera vadībai. HP ploteri izmanto šo failu, lai uz papīra zīmētu un drukātu vektoru un rastra saturu.

### HPGL komanda

HPGL komanda sastāv no tālāk minētā.
 * Divu rakstzīmju alfabēta komandu sadaļa
 * Parametru sadaļa
 * Terminatora sadaļa

Katrs faila parametrs ir jāatdala ar atdalītāju, ja ir vairāki parametri.

### HPGL komandas piemērs

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Koordinātu sistēma

Koordinātu sistēmas sastāv no 2-dimensiju mērījumu indikatoriem, lai noteiktu jebkuru konkrētu vietu. Šim nolūkam HPGL izmanto gan Plotera koordinātu, gan lietotāja koordinātu sistēmu.

#### Plotera koordinātu sistēma

Šo koordinātu sistēmu izmanto, lai attēlotu zīmējumus, pamatojoties uz plotera kustību. Tipiska minimālās plotera kustības XY vienība ir 0,025 mm. Iespējamais zīmējumu diapazons mainās atkarībā no plotera veidiem.

#### Lietotāja koordinātu sistēma

Lietotāja norādīto koordinātu sistēmu var iestatīt, izmantojot mērogu un izcelsmi. Tās tiek pārveidotas par plotera koordinātām, izmantojot komandu IP un komandu SC. Ja šī pārveidošana netiek veikta, pēc noklusējuma tiek izmantotas plotera sistēmas koordinātas.

## HPGL faila formāts
HPGL faili ir ASCII (teksta faila) formātā un sākas ar dažām iestatīšanas komandām. Tas iestata noteiktus parametrus ploterim zīmēšanai. Tipisks HPGL fails izskatās šādi.

|Komanda|Nozīme
---|---|
|IN;|inicializēt, sākt zīmēšanas darbu|
|IP;|iestatiet mērogošanas punktus (P1 un P2) to noklusējuma pozīcijās|
|SP1;|izvēlieties pildspalvu 1|
|PU0,0;|paceliet pildspalvu uz augšu un pārejiet uz nākamās darbības sākumpunktu|
|PD100,0,100,100,0,100,0,0;|nolieciet pildspalvu un pārvietojiet uz tālāk norādītajām vietām (apzīmējiet lodziņu ap lapu)|
|PU50,50;|Pildspalva uz augšu un pāriet uz X,Y koordinātām 50,50|
|CI25;|uzzīmējiet apli ar rādiusu 25|
|SS;|atlasiet standarta rakstzīmju kopu|
|DT*,1;|iestatiet teksta atdalītāju uz zvaigznīti un nedrukājiet tos (1, kas nozīmē patiess)|
|PU20,80;|paceliet pildspalvu un pārejiet uz 20,80|
|LBHello World*;|uzzīmē etiķeti|

## Atsauces
 * [HPGL, Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
 * [HPGL uzziņu rokasgrāmata](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

