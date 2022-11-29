{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SIFZ-filformat - Synfig Studio komprimerad projektfil",
  "description":"Läs mer om SIFZ-filformat och API:er som kan skapa och öppna SIFZ-filer.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## Vad är SIFZ fil?

En SIFZ-fil är en gzip-komprimerad SIF-fil skapad av applikationen för att skapa 2d-animationer med öppen källkod **Synfig Studio**. Den innehåller flera grafiska element som utgör animeringen. Det övergripande animationsinnehållet är byggt med en kombination av en duk som är fylld med former, pensel- eller penndrag och text. Alla dessa är arrangerade i sina egna positioner, radie, tangent, vinkel, vertex och breddhandtag. SIFZ-filer kan öppnas med [Synfig Studio](https://www.synfig.org/).

## SIFZ filformat

SIFZ-filer är komprimerade [ZIP](/sv/compression/zip/)-filer som paketeras med gzip-komprimeringsmetoden. Synfig används för att skapa animationer av filmkvalitet med hjälp av vektor- och bitmappskonstverk. Till skillnad från den gamla metoden för att skapa bildruta-för-bildruta-animationer, låter den dig producera 2D-animationer av högre kvalitet med färre resurser.

SIFZ-filer, som komprimeras, är mindre än de okomprimerade SIF-filerna. Detta gör det också enkelt att överföra via internetanslutningar med låg bandbredd.

## Referenser

* [Synfig Open Source - Github](https://github.com/synfig/synfig/)
* [Synfig-dokumentation](https://synfig.readthedocs.io/en/latest/index.html)

