{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE-bestand - HTML5-cachemanifestbestandsindeling",
  "description" :"Meer informatie over wat een APPCACHE-bestand is en API's die APPCACHE-bestanden kunnen maken en openen.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Wat is een APPCACHE-bestand?

Een APPCACHE-bestand is een tekstbestand dat de lijst met bronnen bevat die door browsers in de cache moeten worden opgeslagen voor offline toegang tot de webapplicaties. Dit is handig als er geen internetverbinding is. In een dergelijke situatie gebruikt de browser de offline cachebronnen om toegang te bieden tot de webinhoud. APPCACHE-bestand bevat webbronnen zoals afbeeldingen (bijvoorbeeld **[PNG](/nl/image/png/)**, **[WEBP](/nl/image/webp/)**, enz.), stylesheets **([ CSS])(/nl/web/css/)** en scriptbestanden (zoals Javascript **[JS](/nl/web/js/)**-bestanden).

Toepassingen die **APPCACHE-bestanden** kunnen openen, zijn onder meer webbrowsers zoals Google Chrome, Safari en Firefox.

## APPCACHE-bestandsindeling - Meer informatie

APPCACHE-bestanden zijn eenvoudige tekstbestanden die offline toegang bieden tot webpagina's voor gebruik zonder internetverbinding. De aanwezigheid van APPCACHE duidt een pagina aan als offline beschikbaar.

### Hoe te verwijzen naar een APPCACHE-bestand?

Op uw HTML-pagina wordt als volgt naar een APPCACHE-bestand verwezen.

```
<html manifest="example.appcache">
  ...
</html>
```

## Structuur van een APPCACHE-manifestbestand

Een eenvoudig APPCACHE-manifestbestand ziet er als volgt uit.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Dit is een eenvoudig voorbeeld en er kunnen ook meer complexe structuren aanwezig zijn.

## Voordelen van APPCACHE Manifest

Het gebruik van de cache-interface geeft webapplicaties de volgende voordelen.

1. Offline browsen - De cache-interface geeft de eindgebruikers de mogelijkheid om door uw volledige site te bladeren wanneer ze offline zijn
1. Snelheid - cache maakt snelle toegang tot offline inhoud direct vanaf schijf mogelijk
1. Altijd toegankelijkheid - Als uw site uitvalt, hebben gebruikers nog steeds toegang tot de webinhoud en kunnen ze de offline-ervaring krijgen

## Referenties

* [Een beginnershandleiding voor AppCache-manifest](https://web.dev/appcache-beginner/)

