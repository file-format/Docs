{
  "date" : "2020-08-20",
  "keywords" :[ "cff-fil", "cff-filformat", "vad är en cff-fil", "fil", "cff-exempel", "cff-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - Compact Font File Format",
  "description":"Läs mer om CFF-filformat och API:er för att skapa och öppna CFF-filer.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Vad är en CFF fil?

En fil med filtillägget .cff är ett kompakt teckensnittsformat och kallas även för PostScript Type 1 eller CIDFont. CFF fungerar som en behållare för att lagra flera teckensnitt tillsammans i en enda enhet känd som en FontSet. Utformningen av CFF-teckensnitt tillåter inbäddning av PostScript-språkkod som tillåter ytterligare flexibilitet och utvidgning av formatet för användning med skrivarmiljöer. CFF-teckensnittsfiler kan öppnas och konverteras med API:er som [Aspose.Font](https://products.aspose.com/font).

## CFF filformat

CFF-filer är binära filer som innehåller en strukturerad datalayout, har definierade datatyper, en rubrik, glyph-organisation och tabellordböcker. Mer information om dessa finns i [specifikationerna för kompakta teckensnittsformat](https://learn.microsoft.com/en-us/typography/opentype/spec/cff).

### Datalayout
Datalayouten för CFF-filformatet är som visas nedan.

|Entry|Kommentarer|
---|---|
|Rubrik|–|
|NamnINDEX|–|
|Topp DICT INDEX|–|
|Sträng INDEX|–|
|Global Subr INDEX|–|
|Kodningar–Teckenuppsättningar|–|
|FDSelect|Endast CIDFonts|
|CharStrings INDEX|per teckensnitt|
|Teckensnitt DICT INDEX|per teckensnitt, endast CIDFonts|
|Privat DICT|per teckensnitt|
|Local Subr INDEX|per teckensnitt eller per privat DICT för CIDFonts|
|Upphovsrätt och varumärken|–|

### Datatyper

CFF-datatyperna är som visas i följande tabell.

|Namn|Omfång|Beskrivning|
---|---|---|
|Kort8|0 –255|1-byte osignerat nummer|
|Kort16|0 – 65535|2-byte osignerat nummer|
|Offset|varierar|1, 2, 3 eller 4 byte offset (anges av fältet OffSize)|
|OffSize|1–4|1-byte osignerat nummer anger storleken på ett eller flera förskjutningsfält|
|SID|0 – 64999|2-byte strängidentifierare|

### Rubrik

Den binära datan börjar med en rubrik med formatet som visas i följande tabell.

|Typ|Namn|Beskrivning|
---|---|---|
|Card8|major|Formatera större version (börjar på 1)|
|Card8|minor|Formatera mindre version (börjar på 0)|
|Kort8|hdrSize| Rubrikstorlek (byte)|
|OffSize|offSize|Absolut offset (0) storlek|

## Referenser

* [Compact Font Format Table](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF-filformat](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 Chartset](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

