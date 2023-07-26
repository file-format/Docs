{
  "date" : "2021-04-08",
  "keywords" :[ "lz fil", "lz filformat", "vad är en lz fil", "fil", "lz exempel", "lz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip komprimerat filformat",
  "description":"Läs mer om LZ-filformat och API:er som kan skapa och öppna LZ-filer.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Vad är LZ fil?

En fil med filtillägget .lz är en komprimerad arkivfil skapad med Lzip, som är ett gratis kommandoradsverktyg för komprimering. Den stöder sammanlänkning för att komprimera stödfiler. LZ-filer har mediatyp application/lzip och stöder högre komprimeringskvoter än [BZ2](/sv/compression/bz2/). LZ är baserade på LZMA-algoritmen (Lempel-Ziv-Markov-kedjan) och inkluderar en 32-bitars CRC-kontrollsumma och identifieringsbytes för att kontrollera filens integritet.

## LZMA komprimerat format

Det komprimerade LZMA-formatet består av en komprimerad ström av bitar som kodas med hjälp av adaptiv binär intervallkodare. Strömmen är uppdelad i paket. Varje paket beskriver antingen en enda byte eller en LZ77-sekvens. Längden och avståndet för varje paket är implicit eller explicit kodat.

De sju typerna av paket är följande ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|Packad kod (bitsekvens) |Paketnamn |Paketbeskrivning|
---|---|---|
|0 + byteCode| LIT| En enda byte kodad med en adaptiv binär intervallkodare.|
|1+0 + len + dist| MATCH| En typisk LZ77-sekvens som beskriver sekvenslängd och avstånd.|
|1+1+0+0| SHORTREP| En en-byte LZ77-sekvens. Avståndet är lika med det senast använda LZ77-avståndet.|
|1+1+0+1 + len| LONGREP[0]| En LZ77-sekvens. Avståndet är lika med det senast använda LZ77-avståndet.|
|1+1+1+0 + len| LONGREP[1]| En LZ77-sekvens. Avståndet är lika med det näst sist använda LZ77-avståndet.|
|1+1+1+1+0 + len| LONGREP[2]| En LZ77-sekvens. Avståndet är lika med det tredje sist använda LZ77-avståndet.|
|1+1+1+1+1 + len| LONGREP[3]| En LZ77-sekvens. Avståndet är lika med det fjärde sist använda LZ77-avståndet.|


## Referenser

* [LZMA - Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

