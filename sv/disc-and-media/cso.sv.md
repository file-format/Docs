{
  "date" : "2021-08-09",
  "keywords" :[ "cso-fil", "cso-filformat", "vad är en cso-fil", "fil", "cso-exempel", "cso-filtillägg", "tillägg", "format", "iso", "DAX-komprimering " ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Läs mer om CSO-filformat och API:er som kan skapa och öppna CSO-filer.",
  "title" :"CSO - komprimerad ISO-diskavbildning",
  "linktitle" : "CSO",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-09"
}

## Vad är CSO fil?

En fil med filtillägget .cso är en komprimerad ISO-bildfil. CSO är ett alternativ till DAX-komprimeringsmetoden; även känd som CISO; var den första metoden att komprimera [ISO](/sv/compression/iso/)-filerna och är vanligtvis en föredragen metod för att arkivera PlayStation Portable-saker. Det här formatet använder Deflate-komprimering, som kan inkludera upp till nio komprimeringslager. Programvara som Prometheus och YACC används för att skapa bilderna.

## CSO filformat

CSO-filformatet var den första komprimeringsmetoden för ISO för att spara mer minnesutrymme. Förbättringarna gjordes då och då för bättre komprimering. CSO:n använder Deflate-komprimering med nio nivåer av förinställningar, vanligtvis kan varje nivå hantera 2 KiB-block individuellt. Medan de högsta nivåerna av komprimering kan långsamma och långa laddningstider i programvara som är starkt beroende av skivströmning, kan även de lägre nivåerna utföra betydande komprimering.

### CSO-filstruktur

CSO-filformatet innehåller en 24-byte header, datablock och en indextabell. Little-endian antas för fält större än en byte. Arkitekturen i PlayStation Portable ges nedan.

#### Rubrik

| Offset (byte) | Namn | Storlek (byte) | Syfte |
----------|----------|--------------|---------|
| 0x0 | Magi | 4 | Alltid CISO, eller 0x4F534943 när det läses som ett 32-bitars heltal. Detta fält används för att identifiera en CSO-fil. Observera att detta fält kan vara annorlunda för de andra derivaten av CSO, till exempel använde ZSO den magiska koden ZISO. |
| 0x4 | Rubrikstorlek | 4 | För det ursprungliga CSO "v1"-filformatet ignoreras detta fält och behöver därför inte vara korrekt. Men formatet "v2" och ZSO kräver att detta fält alltid är 0x18 (24 byte). |
| 0x8 | Okomprimerad storlek | 8 | Storleken på den ursprungliga okomprimerade ISO i byte. |
| 0x10 | Blockstorlek | 4 | Storleken på varje datablock i byte före komprimering. Vanligtvis 2048 byte, samma som storleken på varje ISO 9660-sektor. |
| 0x14 | Version | 1 | Den version av filformatet som används. För formatet "v1" kan värdet vara antingen 0 eller 1. För formatet "v2" måste detta vara 2. Dessutom kräver ZSO-formatet att detta är 1. |
| 0x15 | Indexjustering | 1 | Justeringen av varje indexpost, specificerad i bitar. |
| 0x16 | Reserverad | 2 | Detta fält är oanvänt. I formatet "v1" ignoreras detta fält och kan innehålla godtyckliga värden. I formatet "v2" måste detta fält vara noll. |

#### Indextabell

Indextabellen innehåller flera 4-byte-poster, som indikerar positionen för varje datablock, och ytterligare en sista post som pekar mot slutet av filen.
Innehållet i varje inlägg är som följer:
| Bit | Längd | Mask | Namn | Syfte |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFFF | Position | Detta fält, när det flyttas åt vänster av indexjusteringen som ges i rubriken, avger positionen där datablocket startar. |
| 31 | 1 | 0x80000000 | Kompressionstyp | ZSO-formatet har liknande semantik, bara att 0 representerar LZ4 istället för Deflate. I formatet "v2". Blocket anses implicit vara okomprimerat om blockstorleken är lika med eller större än blockstorleken som anges i filhuvudet. |

#### Datablock

Datablocken består av okomprimerad eller komprimerad data. Storleken på ett block beräknas genom att få dess position och sedan subtrahera det från positionen för det följande blocket. Om indexinriktningen är större än noll är det troligt att blockstorleken är större än den data som den innehåller.


## Referenser

* [CSO - av Wikipedia](https://en.wikipedia.org/wiki/.CSO)


