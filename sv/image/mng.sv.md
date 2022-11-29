{
  "date" : "2019-10-11",
  "keywords" :[ "mng-fil", "mng-filformat", "vad är en mng-fil", "fil", "mng-exempel", "mng-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG File Format - Multiple Image Network Graphics File Format",
  "description":"Läs mer om MNG-filformat och API:er som kan skapa och öppna MNG-filer.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en MNG fil?

En fil med filtillägget .mng är ett nätverksgrafikfilformat med flera bilder som liknar bildformatet [PNG](/sv/image/png/) men stöder animerade bilder. Det utvecklades för att undvika att överbelasta PNG-formatet med ytterligare funktioner för animationer. MNG liknar också [GIF](/sv/image/gif/)-filer men använder mer komprimering och stöder full alfafunktion. Den inofficiella MIME-medietypen för MNG-filer är video/x-mng. MNG-filer kan öppnas i applikationer som ImageMagik och IrfanView.

## MNG filformat

MNG-filformatet liknar det för PNG och använder samma chunk-struktur som definieras i PNG-specifikationerna. En MNG-avkodare måste kunna avkoda PNG-dataströmmarna utan att ange några speciella flaggor för avkodningsinstruktioner. MNG grupperar flera bilder till en "ram", med några bilder som används som sprite för att flytta från en plats till en annan. Mekanismen tillåter återanvändning av bilddata utan att återsända den. [MNG-specifikationerna](http://www.libpng.org/pub/mng/spec/) kan refereras till för utvecklarens referens.

### MNG-signatur

MNG-dataströmmen börjar med en 8-bytesignatur som innehåller:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

Detta liknar det för PNG-signatur men innehåller MNG istället för PNG.

### MNG-ram

En MNG-ram består av tvådimensionell bild av mindre bilder. Varje liten bild kan nås med kombinationen rad- och kolumnindex. Formatet är kapabelt att lagra tredimensionell "voxel"-data som är arrangerad i en serie tvådimensionella plan. Varje plan representeras av en PNG- eller Delta-PNG-dataström. Varje Delta-PNG-dataström definierar en bild som skillnaderna från den överordnade PNG-bilden. Detta ger ett mycket mer kompakt sätt att representera efterföljande bilder än att använda en komplett PNG-dataström för varje.

## Referenser ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG-format v 1.0](http://www.libpng.org/pub/mng/spec/)

