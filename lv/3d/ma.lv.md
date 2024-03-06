{
  "date": "2019-10-11",
  "keywords": [
"ma",
"ma fails",
"ma faila formātā",
"faila formātā",
"3d",
"ma faila lejupielāde",
".ma fails",
".ma"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par MA faila formātu un API, kas var atvērt un izveidot MA failus.",
  "title": "MA faila formāts",
  "linktitle": "MA",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-m-lva"
}
},
  "lastmod": "2021-06-04"
}

## Kas ir MA fails?

Fails ar paplašinājumu .ma ir 3D projekta fails, kas izveidots ar lietojumprogrammu Autodesk Maya. Tajā ir liels teksta komandu saraksts, lai norādītu informāciju par failu. **.ma failu** var atvērt un rediģēt jebkurā teksta redaktorā, lai novērstu jebkādas problēmas ar komandām gadījumā, ja fails tiek bojāts. Šajos failos ir ietverta informācija 3D ainas informācijas definēšanai, piemēram, ģeometrija, apgaismojums, animācija un renderēšana.

## MA faila formāts

MA faili tiek saglabāti diskā ASCII teksta formātā atšķirībā no MB failiem, kas diskā tiek saglabāti binārā faila formātā. Detalizēta atsauce uz MA faila formātu ir pieejama vietnē [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001), un to var skatīt izstrādātāja atsaucei.

### MA faila galvene

MA faila galvene sākas ar komentāru sadaļu, kas sniedz informāciju par faila izveidi un modificēšanas datumu. Maya failu lasītāji ignorē šo bloku, jo tas tiek izmantots tikai informatīviem nolūkiem. Tomēr galvenei jāsākas ar pirmajām sešām rakstzīmēm kā //Maya.

ASCII faila galvene izskatās šādi.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Failu atsauces

.ma faila failu atsauces sadaļā ir informācija par visiem citiem Maya failiem, uz kuriem ir atsauces šajā failā. Katru norādīto failu var nolasīt, izmantojot vienu faila komandu, kas atrodas tajā pašā failā. Faila komandas sintakse, kad to izmanto atsaucēm, ir:

```
file -r -rpr prefixString fileName;
```
vai

```
file -r -ns nameSpace fileName
```
Šeit ir virknes piemērs.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Šis piemērs parāda, ka saules objekts, kas atrodas failā `solar`, būtu pieejams šajā failā, izmantojot nosaukumu solar_sun.

### Prasības

.ma faila prasību sadaļa sastāv no vairākām obligātām komandām, un tajā tiek sniegta informācija par informāciju, piemēram, versija un spraudņa informācija, kas nepieciešama failu lasīšanai. Prasību sadaļas piemērs ir šāds.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Nākamajā sadaļā ir norādītas prasības. Tas sastāv no vairākām nepieciešamajām komandām. Šajā faila sadaļā Maya ir norādīts, kāda programmatūra ir nepieciešama, lai pareizi ielādētu failu. Konkrēti, kāda Maya versija un kādi spraudņi.

## MA faila lejupielāde
Ir nedaudz grūti atrast un lejupielādēt 3D modeļa MA failu. Tādēļ varat lejupielādēt MA faila paraugu no šejienes:

- [Sample.ma](../sample.ma)


## Atsauces

* [Maijas ASCII failu organizēšana — Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)


