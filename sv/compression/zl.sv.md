{
  "date" : "2019-12-09",
  "keywords" :[ "zl fil", "zl filformat", "vad är en zl fil", "fil", "zl exempel", "zl filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZL - ZLIP komprimerat filformat",
  "description":"Läs mer om ZL-filformat och API:er som kan skapa och öppna ZL-filer.",
  "linktitle" : "ZL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-14"
}

## Vad är ZL fil?

En fil med filtillägget .zl är ett ZLIP-komprimerat filformat som använder en variant av DEFLATE-komprimeringsalgoritmen för att komprimera filer. Det är oberoende av CPU-typ, operativsystem, filsystem och teckenuppsättning, och kan därför användas för utbyte av information. Tekniska specifikationer för ZLIP-komprimering finns på [IETF-webbplatsen](https://tools.ietf.org/html/rfc1950) och kan refereras från utvecklarens perspektiv.

## ZL filformat

En zlib-ström har följande struktur:

* `CMF (Compression Method and flags)` - Denna byte är uppdelad i en 4-bitars komprimeringsmetod och ett 4-bitars informationsfält beroende på komprimeringsmetoden.
```
bits 0 to 3  CM     Compression method
bits 4 to 7  CINFO  Compression info
```
* `CM (Kompressionsmetod)` - Den identifierar komprimeringsmetoden som används i filen. Dess värden och motsvarande komprimeringsmetod är som följer.

| CM-värde| Kompression|
|---|---|
|CM = 8|DEFLATE med en fönsterstorlek upp till 32K|
|CM = 15|Reserverad|

* `CINFO (Kompressionsinformation)` - För CM = 8 är CINFO bas-2-logaritmen för LZ77-fönsterstorleken, minus åtta (CINFO=7 indikerar en fönsterstorlek på 32K).

* `FLG (FLaGs)` - Denna flaggbyte är uppdelad enligt följande:
```
  bits 0 to 4  FCHECK  (check bits for CMF and FLG)
  bit  5       FDICT   (preset dictionary)
  bits 6 to 7  FLEVEL  (compression level)
````

## Referenser ##

* [Zlib filformatspecifikationer](https://tools.ietf.org/html/rfc1950)

