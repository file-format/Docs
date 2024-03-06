{
  "date": "2021-04-08",
  "keywords": [
"lzma fails",
"lzma faila formātā",
"kas ir lzma fails",
"failu",
"lzma piemērs",
"lzma faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZMA - LZMA saspiestā faila formāts",
  "description": "Kas ir LZMA fails un API, kas var izveidot un atvērt LZMA failus.",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzm-lva"
}
},
  "lastmod": "2021-04-18"
}

## Kas ir LZMA fails?

Fails ar paplašinājumu .lzma ir saspiests arhīva fails, kas izveidots, izmantojot LZMA (Lempel-Ziv-Markov chain Algorithm) saspiešanas metodi. Tie galvenokārt tiek atrasti/izmantoti operētājsistēmā Unix un ir līdzīgi citiem saspiešanas algoritmiem, piemēram, [ZIP](/compression/zip/), lai samazinātu faila lielumu. LZMA ir mantots faila formāts, kas tiek vai ir aizstāts ar .xz formātu. .lzma formāta MIME tips ir \`application/x-lzma'. Šo faila formātu izmantošanai LZMA SDK izstrādāja Igors Pavlovs.

## LZMA faila formāts

LZMA fails sastāv no divām galvenajām daļām:

 1. Virsraksts
 1. Saspiesti dati


### LZMA Header

LZMA failiem ir 13 baitu galvene, kurai seko LZMA saspiestie dati. LZMA galvene sastāv no:

 * Īpašības
 * Vārdnīcas izmērs
 * Nesaspiests izmērs

#### LZMA galvenes īpašības

Laukā Rekvizīti ir trīs rekvizīti. Iekavās ir norādīts saīsinājums, kam seko rekvizīta vērtību diapazons. Lauks sastāv no

1) literālā konteksta bitu skaits (lc, [0, 8]);
2) literālās pozīcijas bitu skaits (lp, [0, 4]); un
3) pozīcijas bitu skaits (pb, [0, 4]).

#### LZMA vārdnīcas izmērs

Tas tiek saglabāts kā neparakstīts 32 bitu mazs endian vesels skaitlis ar vērtībām no 2^n un 2^n + 2^(n-1). LZMA Utils var atspiest failus ar jebkuru vārdnīcas izmēru.

#### Nesaspiests izmērs
Nesaspiestais lielums tiek saglabāts kā neparakstīts 64 bitu mazs endian vesels skaitlis. Īpaša vērtība 0xFFFF_FFFF_FFFF_FFFF norāda, ka nesaspiestais izmērs nav zināms. Vērtību attēlo lietderīgās slodzes beigu marķieris (\*) tad un tikai tad, ja nesaspiestais izmērs nav zināms.

## Atsauces
* [Lempel–Ziv–Markova ķēdes algoritms](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)
