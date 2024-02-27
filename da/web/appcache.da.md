{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPCACHE-fil - HTML5 Cache-manifest-filformat",
  "description": "Lær om, hvad en APPCACHE-fil og API'er er, der kan oprette og åbne APPCACHE-filer.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcach-dae"
}
},
  "lastmod": "2022-08-05"
}

## Hvad er en APPCACHE fil?

En APPCACHE-fil er en tekstfil, der indeholder listen over ressourcer, der skal cachelagres af browsere for offlineadgang til webapplikationerne. Dette er nyttigt, når der ikke er nogen internetforbindelse. I en sådan situation bruger browseren de offline cache-ressourcer til at give adgang til webindholdet. APPCACHE-filen indeholder webressourcer såsom billeder (f.eks. **[PNG](/image/png/)**, **[WEBP](/image/webp/)** osv.), typografiark **([CSS])(/web/css/ )** og scriptfiler (såsom Javascript **[JS](/web/js/)**-filer).

Programmer, der kan **åbne APPCACHE-filer**, omfatter webbrowsere såsom Google Chrome, Safari og Firefox.

## APPCACHE-filformat - flere oplysninger

APPCACHE-filer er simple tekstfiler, der giver offline adgang til websider, så de kan køre uden internetforbindelse. Tilstedeværelsen af APPCACHE angiver en side som tilgængelig offline.

### Hvordan henvises til en APPCACHE-fil?

På din HTML-side henvises der til en APPCACHE-fil som følger.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struktur af en APPCACHE Manifest fil

En simpel APPCACHE-manifestfil ser ud som følger.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Dette er et simpleste eksempel, og der kan også være mere komplekse strukturer til stede.

## Fordele ved APPCACHE Manifest

Brugen af cache-grænseflade giver webapplikationer følgende fordele.

 1. Offline browsing - Cache-grænsefladen giver slutbrugerne mulighed for at gennemse hele dit websted, når de er offline
 1. Speed - cache giver højhastighedsadgang til offline indhold direkte fra disken
 1. Tilgængelighed hele tiden - Hvis dit websted går ned, vil brugerne stadig have adgang til webindholdet og vil være i stand til at få offline-oplevelsen

## Referencer

 * [En begyndervejledning til AppCache-manifest](https://web.dev/appcache-beginner/)

