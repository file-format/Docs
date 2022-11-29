{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Nuvo Medias Rocket eBook-enhet", "fil", "tillägg", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om RB-filformat för Nuvo Medias Rocket eBook-enhet och API:er som kan skapa och öppna RB-filer.",
  "title" :"RB - Rocket eBook File",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Vad är en RB fil?

Filen med tillägget .rb innehåller Rocket eBook-innehållet. The Rocket eBook är faktiskt en enhet gjord av Nuvo Media; de släppte den här enheten 1998. Även om Rocket eBook kan visa bilder, men bara i svartvitt. Den har en skärm på 106 dpi eller 480 x 320 pixlar på en 4,5 x 3-tums pekskärm. Rocket eBook ansluts till en dator via en seriell portanslutning för att ladda ner e-böcker i RB-filformat. RB-filerna kan använda DRM men denna teknik används inte i moderna e-böcker. RB-filen innehåller vanligtvis en HTML-fil med bilderna och en pseudo-OPF-fil med all metadata (.info).

## Teknisk specifikation för RB-filformat ##

Ett magiskt tal (i hex) visas i filens första 4 byte: B0 0C B0 0C.

Det verkar som att de nästa två byten är ett versionsnummer, som "02 00", som står för huvudversion 2 och mindre version 0.

De nästa fyra byten innehåller texten "NUVO", följt av 4 byte av 00h.

Nästa 4-byte är det datum då boken skapades, kodad som en int16. Detta placerar oss på offset 0Eh. ORocketLibrarys gamla version kodade årets fulla värde (dvs 1999 var "CF 07", 2000 var "D0 07"). I den senaste versionen lagras tm_year ordagrant, dvs 100 för år 2000 ("64 00"). Efter året kommer en int8 som representerar 1-relativ månadsnummer och en int8 som representerar dagen i månaden.

Nästa 6 byte är 00h. För tidsinställning kan dessa reserveras.

Den absoluta offseten för "Innehållsförteckningen" finns i en int32 vid offset 18h.

Efter detta är en int32 som innehåller längden på .rb-filen. Detta används för att avgöra om filerna är kompletta eller inte.

Hela den här biten av byte (20h till 128h) verkar bara behövas av en titel som är krypterad. I icke-krypterade titlar är de alltid noll.

I de flesta fall följer innehållsförteckningen (vid offset 128). Det börjar med en int32-räkning av antalet "page"-poster (.rb-filsektioner) i innehållsförteckningen. Varje post består av ett namn (nollutfyllt till 32 byte), följt av 3 int32s: längden på datasegmentet, positionen i .rb-filen och en flagga för denna post. Från och med idag är de kända värdena: 1 (krypterad), 2 (informationssida) och 8 (deflaterad). Namnen är alla skräddarsydda efter behov för att säkerställa att de alla är unika.

## Referenser

* [E-Reader - By MobileRead](https://en.wikipedia.org/wiki/E-reader)

