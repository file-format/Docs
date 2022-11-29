{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Komprimerad", "Fil", "Extension", "Filformat", "Lempel-Ziv", "Haruyasu", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZH filformat",
  "description":"Läs mer om LZH-filformat och API:er som kan skapa och öppna LZH-filer.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## Vad är LZH fil? ##

En fil med filändelsen .lzh och .lha relaterar vanligtvis till filformatet för arkivkomprimering. Detta filformat är detsamma som andra filkomprimeringsformat som [ZIP](/sv/compression/zip/), [RAR](/sv/compression/rar/), etc. Huvudsyftet med dessa filformat är att minska storleken på format för att enkelt skicka samt för att hålla dem samman i komprimerad form. AS jämför med andra västerländska företag LZH-filer är mycket populära i Japan och används vanligtvis för att komprimera data från videospel. LZH-tillägget för Windows 7 är inbyggt i den japanska versionen av Windows 7. Microsoft släppte först Microsoft Compressed (LZH) Folder Add-on för den japanska versionen av Windows XP. Detta filformat är implementerat med komprimeringsbestämmelser och funktioner som används av Lempel-Ziv och Haruyasu algoritmer

## LZH-specifikation ##

Komprimeringsmetoden för ett LZH-arkiv visas som en fem-byte textsträng, såsom -lz1-. Dessa är den tredje till sjunde byten i den komprimerade filen.

|Specifikation|Beskrivning|
---|---|
|Tillägg | .lzh, .lha|
|Medietyp| applikation/x-lzh-komprimerad|
|Skriv kod| "LHA_" (LHA-SPACE)|
|UTI| public.archive.lha|
|Utvecklad av| Haruyasu Yoshizaki (Yoshi)|
|Skriv| Kompression|
|Utökad från| Larc|

## Problem med att öppna en LZH-fil ##

Följande är några problem som kan orsaka dåligt fungerande LZH-filformat:
  

* Filen kan vara korrupt. För att lösa det här problemet, ladda ner filen igen eller be avsändaren att skicka om filen igen
* Den andra orsaken är en infekterad fil i det här fallet skanna filen ordentligt
* Felaktiga länkar till LZH-filen
* Borttagning av beskrivningen av LZH
* Inte tillräckligt med hårdvaruresurser
* Föråldrade drivrutiner för utrustningen

## Referenser ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
