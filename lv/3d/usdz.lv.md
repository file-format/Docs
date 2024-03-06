{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"usdz fails",
"usdz faila formāts",
"faila formātā",
"3d",
"usdz faila lejupielāde"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ — universāls ainas apraksta ZIP formāts",
  "description": "Uzziniet par USDZ failu formātu un API, kas var atvērt un izveidot USDZ failus.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-lvz"
}
},
  "lastmod": "2021-02-01"
}

## Kas ir USDZ fails?

Fails ar .usdz ir nesaspiests un nešifrēts ZIP arhīvs [USD](/3d/usd/) (Universal Scene Description) faila formātam, kas satur un nodrošina citu formātu failus (piemēram, tekstūras un animācijas), kas ir iegulti arhīvā un palaiž tos. tieši ar USD izpildlaiku, bez nepieciešamības tos izsaiņot. USDZ faili ir pakotnes, kuru dizains ir balstīts uz jauno paketes Ar līmeņa abstrakciju. Usdz tika reģistrēts IANA, un tam ir modeļa multivides tipa nosaukums un vnd.usd+zip apakštipa nosaukums, un tā informāciju var atrast vietnē [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ faila formāts

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### ZIP ierobežojumi

USDZ faila formātā tiek izmantots ZIP faila formāts bez saspiešanas un šifrēšanas. Tas tika izstrādāts, lai izpildītu divas prasības:

 * Pakotnei, kas jau ir ielādēta atmiņā vai kā atsevišķam failam diskā, API ir pieejams USD, lai piekļūtu attēla datiem.
 * Nevajadzētu izvilkt failus diskā vai piešķirt vairāk kaudzes krātuves

Izmantojot USDZ, abas šīs prasības ir izpildītas, jo lielākā daļa attēlu formātu paši pieļauj iekšējas saspiešanas shēmas, kā rezultātā fails ir kompakts.

### Izkārtojuma prasības

USDZ pakotnēm ir nepieciešams failu izkārtojums pakotnē, lai katra faila datiem būtu jāsākas ar 64 baitiem no pakotnes sākuma. Tomēr pakotnei ir jāsākas ar vietējo [USD](/3d/usd/) failu, ja pakotnei tiek atlasīta vienkārša atsauce. Šādā gadījumā šis pirmais USD fails tiek saukts par noklusējuma slāni. Klienti, kas vēlas nodrošināt straumējamu saturu, var vēlēties apsvērt arī citus izkārtojuma ierobežojumus.

## USDZ faila lejupielāde
Tā kā usdz faili ir pildīti ar citiem augstas kvalitātes attēliem un usd failiem, tie var aizņemt lielāku diska krātuvi. Šeit varat atrast vienkāršu un mazāku USDZ parauga failu lejupielādei:

- [Sample.usdz](../sample.usdz)

## Atsauces

* [USDZ faila formāta specifikācijas](https://openusd.org/release/spec_usdz.html)


