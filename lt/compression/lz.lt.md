{
  "date": "2021-04-08",
  "keywords": [
"lz failą",
"lz failo formatas",
"kas yra lz failas",
"failą",
"lz pavyzdys",
"lz failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZ – Lzip suspausto failo formatas",
  "description": "Sužinokite apie LZ failo formatą ir API, kurios gali kurti ir atidaryti LZ failus.",
  "linktitle": "LZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-l-ltz"
}
},
  "lastmod": "2021-04-19"
}

## Kas yra LZ failas?

Failas su plėtiniu .lz yra suspaustas archyvo failas, sukurtas naudojant Lzip, kuris yra nemokamas komandinės eilutės įrankis glaudinimui. Jis palaiko sujungimą, kad suspaustų palaikymo failus. LZ failai turi medijos tipo programą / lzip ir palaiko didesnį glaudinimo koeficientą nei [BZ2](/compression/bz2/). LZ yra pagrįsti LZMA (Lempel-Ziv-Markov grandinės) algoritmu ir apima 32 bitų CRC kontrolinę sumą ir identifikacinius baitus, skirtus failo vientisumui patikrinti.

## LZMA suspaustas formatas

LZMA suspaustą formatą sudaro suspaustas bitų srautas, užkoduotas naudojant adaptyvų dvejetainio diapazono kodavimo priemonę. Srautas yra padalintas į paketus. Kiekvienas paketas apibūdina vieną baitą arba LZ77 seką. Kiekvieno paketo ilgis ir atstumas yra netiesiogiai arba aiškiai užkoduoti.

Septyni paketų tipai yra tokie ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packed code (bit sequence)	|Packet name	|Packet description|
---|---|---|
|0 + baito kodas| LIT| Vienas baitas, užkoduotas naudojant adaptyvų dvejetainio diapazono koderį.|
|1+0 + len + dist.| MATCH| Tipiška LZ77 seka, apibūdinanti sekos ilgį ir atstumą.|
|1+1+0+0| SHORTREP| Vieno baito LZ77 seka. Atstumas lygus paskutiniam naudotam LZ77 atstumui.|
|1+1+0+1 + len| LONGREP[0]| LZ77 seka. Atstumas lygus paskutiniam naudotam LZ77 atstumui.|
|1+1+1+0 + len| LONGREP[1]| LZ77 seka. Atstumas lygus antram paskutiniam naudotam LZ77 atstumui.|
|1+1+1+1+0 + len| LONGREP[2]| LZ77 seka. Atstumas lygus trečiam paskutiniam naudotam LZ77 atstumui.|
|1+1+1+1+1 + len| LONGREP[3]| LZ77 seka. Atstumas lygus ketvirtam paskutiniam naudotam LZ77 atstumui.|


## Nuorodos

* [LZMA – Vikipedija](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)

* [Lzip](https://en.wikipedia.org/wiki/Lzip)


