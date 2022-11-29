{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE File - HTML5 Cache Manifest File Format",
  "description" :"Läs mer om vad en APPCACHE-fil är och API:er som kan skapa och öppna APPCACHE-filer.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Vad är en APPCACHE-fil?

En APPCACHE-fil är en textfil som innehåller listan över resurser som ska cachelagras av webbläsare för offlineåtkomst till webbapplikationerna. Detta är användbart när det inte finns någon internetanslutning. I en sådan situation använder webbläsaren offlinecache-resurserna för att ge tillgång till webbinnehållet. APPCACHE-filen innehåller webbresurser som bilder (till exempel **[PNG](/sv/image/png/)**, **[WEBP](/sv/image/webp/)**, etc.), stilmallar **([ CSS])(/sv/web/css/)** och skriptfiler (som Javascript **[JS](/sv/web/js/)**-filer).

Applikationer som kan **öppna APPCACHE-filer** inkluderar webbläsare som Google Chrome, Safari och Firefox.

## APPCACHE-filformat - Mer information

APPCACHE-filer är enkla textfiler som ger offlineåtkomst till webbsidor för att köras utan internetanslutning. Närvaron av APPCACHE anger en sida som tillgänglig offline.

### Hur refererar man till en APPCACHE-fil?

På din HTML-sida hänvisas till en APPCACHE-fil enligt följande.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struktur för en APPCACHE-manifestfil

En enkel APPCACHE-manifestfil ser ut som följer.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Detta är ett enklaste exempel och det kan också finnas mer komplexa strukturer.

## Fördelar med APPCACHE Manifest

Användningen av cache-gränssnitt ger webbapplikationer följande fördelar.

1. Offlinesurfning – cachegränssnittet ger slutanvändarna möjlighet att surfa på hela din webbplats när de är offline
1. Hastighet - cache möjliggör höghastighetsåtkomst till offlineinnehåll direkt från skivan
1. Tillgänglighet hela tiden - Om din webbplats går ner kommer användarna fortfarande att ha tillgång till webbinnehållet och kommer att kunna få offlineupplevelsen

## Referenser

* [En nybörjarguide till AppCache-manifest](https://web.dev/appcache-beginner/)

