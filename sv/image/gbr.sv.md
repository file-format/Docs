{
  "date" : "2019-10-11",
  "keywords" :[ "gbr-fil", "gbr-filformat", "vad är en gbr-fil", "fil", "gbr-exempel", "gbr-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR-filformat - Gerber-filformat för PCB",
  "description":"Läs mer om GBR-filformat och API:er som kan skapa och öppna GBR-filer.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är GBR fil?

En fil med filtillägget .gbr är ett Gerber-bildfilformat för utbyte av designdataöverföring för tryckta kretskort (PCB). Det utvecklades av Ucamco. PCB-designdata är huvudkomponenten som krävs av tillverkningsindustrin för hantering. En GRB-fil innehåller PCB-data som kopparlager, lödmask, förklaring och borr- och ruttdata. Den kan användas för att överföra data såsom PCB-tillverkningsegenskaper inklusive tjocklek eller finish i ett standardiserat format. Alla PCB-designsystem matar ut Gerber-filer som kan hanteras av PCB-tillverkningssystem. GBR-filer har nu blivit de facto-standarden för överföring av designdata för tryckta kretskort (PCB). Ucamco har tillhandahållit en [gratis onlinevisare](https://gerber-viewer.ucamco.com/) för att öppna och visa GBR-filformat.

## GBR filformat

GBR är ett UTF-8-format som kan läsas av människor som bara består av 27 kommandon. På grund av denna korta lista med kommandon och dess kompakthet är GBR lätt att felsöka. Gerbers kärna är ett öppet vektorformat för binära 2D-bilder. Metainformation överförs med bilderna via Attributes. En enda GRB-fil specificerar en enda bild och kräver inga medföljande filer eller externa parametrar för att tolkas. En bild behöver bara en fil. Den använder 7-bitars ASCII-tecken för alla kommandon och namn som definieras i specifikationen som är utskrivbara. Detta täcker fullständigt bildgenerering.

### Exempel GBR-fil

Följande är ett exempel på Gerber-fil som skapar en cirkel med 1,5 mm diameter centrerad på ursprunget. Det finns ett kommando per rad.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referenser

* [Gerber-format](https://www.ucamco.com/en/gerber)

