{
  "date" : "2021-26-08",
  "keywords" :[ "ecw-fil", "ecw-filformat", "vad är en ecw-fil", "fil", "ecw-exempel", "ecw-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ECW - Enhanced Compression Wavelet Image File",
  "description":"Läs mer om ECW-filformat och API:er som kan skapa och öppna ECW-filer.",
  "linktitle" : "ECW",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-26-08"
}

## Vad är en ECW fil? ##
En ECW-fil består av en bild utformad för användning med geospatiala data. Den innehållande bilden är faktiskt en komprimerad bild skapad i formatet Enhanced Compression Wavelet. ECW-filer används vanligtvis för att lagra satellitkartprojektion och flygbilder. För att stödja geospatiala applikationer kan kartprojektionsinformation bäddas in i ECW-filerna.

## ECW filformat
ECW är ett proprietärt bildformat baserat på wavelet-komprimering; optimerad för satellitbilder och flygfotografering. Detta format ägs nu av Intergraph, en del av Hexagon AB, men i grunden har det utvecklats av Earth Resource Mapping. ECW är ett förlustformat komprimering som komprimerar stora bilder med fin alternerande kontrast samtidigt som den behåller sin visuella kvalitet.
 

### Egenskaper
Här är några typiska egenskaper för ECW-format:
- Kartprojektionsinformation kan läggas till i ECW-filformatet för att stödja geospatiala applikationer.
- Bilddata på upp till 65 535 band inklusive lager eller färger kan komprimeras till ECW-filformatet med en hastighet på över 25 MB per sekund.
- ECWP-protokollet är ett effektivt strömningsprotokoll som används för att överföra ECW- och JPEG2000-bilder över nätverk.
- En snabb SDK som stöder ECW och JPEG2000 är tillgänglig utan kostnad för desktopimplementering för Linux, Windows och MacOSX



## Referenser ##

* [ECW (filformat) - av Wikipedia](https://en.wikipedia.org/wiki/ECW_(file_format))


