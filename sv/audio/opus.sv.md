{
  "date" : "2021-02-26",
  "keywords" :[ "OPUS", "fil", "tillägg", "format", "Ljudkodning"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om OPUS-filformat och API:er som kan skapa och öppna OPUS-filer.",
  "title" :"OPUS",
  "linktitle" : "OPUS",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-02-26"
}

## Vad är OPUS fil?

Opus är ett ljudfilformat skapat av Xiph.Org Foundation och som senare standardiserats av IETF (Internet Engineering Task Force). Den har utvecklats främst för internetströmning, Voice over IP (VOIP), videokonferenser och chatt i spelet, det är därför den är designad för att behålla låg latens samtidigt som den upprätthåller interaktiv kommunikation i realtid. För att behålla ljudkvaliteten på en Opus-fil har många blindlyssningstester markerat Opus som ljudformat av hög kvalitet än något annat ljudformat vid en given bithastighet.

## OPUS filformatspecifikationer

Opus-formatet använder både SILK (används av Skype) och Xiph.Org-codec och stöder variabla bithastigheter från 6 kb/s till 510 kb/s. Opus extension använder den talorienterade LPC-baserade SILK-algoritmen och den MDCT-baserade CELT-algoritmen med lägre latens, ibland växlar mellan båda eller ibland genom att kombinera båda algoritmerna för att ge maximal effektivitet. Filer i Opus-format har filtillägget .opus. Till skillnad från Vorbis filformat krävs inte stora kodböcker av Opus för varje enskild fil, det är anledningen till att detta format är jämförelsevis effektivt.

## Referenser ##

* [OPUS - av Wikipedia](https://en.wikipedia.org/wiki/Opus_(audio_format))

