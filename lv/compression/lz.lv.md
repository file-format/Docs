{
  "date": "2021-04-08",
  "keywords": [
"lz failu",
"lz faila formātā",
"kas ir lz fails",
"failu",
"lz piemērs",
"lz faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ — Lzip saspiestā faila formāts",
  "description": "Uzziniet par LZ failu formātu un API, kas var izveidot un atvērt LZ failus.",
  "linktitle": "LZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-l-lvz"
}
},
  "lastmod": "2021-04-19"
}

## Kas ir LZ fails?

Fails ar paplašinājumu .lz ir saspiests arhīva fails, kas izveidots ar Lzip, kas ir bezmaksas komandrindas rīks saspiešanai. Tā atbalsta savienošanu, lai saspiestu atbalsta failus. LZ failiem ir multivides tipa lietojumprogramma/lzip, un tie atbalsta lielāku saspiešanas pakāpi nekā [BZ2](/compression/bz2/). LZ pamatā ir LZMA (Lempel-Ziv-Markov ķēde) algoritms un ietver 32 bitu CRC kontrolsummu un identiskus baitus faila integritātes pārbaudei.

## LZMA saspiestais formāts

LZMA saspiestais formāts sastāv no saspiestas bitu straumes, kas tiek kodēta, izmantojot adaptīvo bināro diapazonu kodētāju. Straume ir sadalīta paketēs. Katra pakete apraksta vai nu vienu baitu, vai LZ77 secību. Katras paketes garums un attālums ir netieši vai tieši kodēts.

Septiņi pakešu veidi ir šādi ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + baita kods| LIT| Viens baits, kas kodēts, izmantojot adaptīvu binārā diapazona kodētāju.|
|1+0 + len + dist| MATCH| Tipiska LZ77 secība, kas apraksta secības garumu un attālumu.|
|1+1+0+0| SHORTREP| Viena baita LZ77 secība. Attālums ir vienāds ar pēdējo izmantoto LZ77 attālumu.|
|1+1+0+1 + len| LONGREP[0]| LZ77 secība. Attālums ir vienāds ar pēdējo izmantoto LZ77 attālumu.|
|1+1+1+0 + len| LONGREP[1]| LZ77 secība. Attālums ir vienāds ar otro pēdējo izmantoto LZ77 attālumu.|
|1+1+1+1+0 + len| LONGREP[2]| LZ77 secība. Attālums ir vienāds ar trešo pēdējo izmantoto LZ77 attālumu.|
|1+1+1+1+1 + len| LONGREP[3]| LZ77 secība. Attālums ir vienāds ar ceturto pēdējo izmantoto LZ77 attālumu.|


## Atsauces

* [LZMA — Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)

* [Lzip](https://en.wikipedia.org/wiki/Lzip)


