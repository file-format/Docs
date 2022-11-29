{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Cross-platform Installer Package File",
  "description":"Läs mer om XPI-filformat och API:er som kan skapa och öppna XPI-filer.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Vad är en XPI fil?

En XPI-fil är ett installationsarkiv som komprimeras för att minska storleken på filen. Det används av Mozilla-applikationer för installation av plugins och tilläggsfiler. Den innehåller ett installationsskript eller ett manifest i roten av filen tillsammans med ett antal datafiler. En XPI-fil kan innehålla teman, verktygslåda eller Firefox-plugin-program som användaren kan installera för att bli en del av webbläsaren Firefox, Thunderbird eller SeaMonkey.

## XPI-filformat - Mer information

XPI-filer sparas på skiva som [ZIP](/sv/compression/zip/)-arkiv som kombinerar flera filer till en enda komprimerad fil. Filerna i en XPI-fil kan innehålla installationsskriptfiler som JS och webbfiler som [CSS](/sv/web/css/), [HTML](/sv/web/html/) och [JSON](/sv/web/json/ ). Ibland kan den också innehålla [PNG](/sv/image/png/) bildfiler som ska användas som ikoner av tillägg.

### Hur ser man XPI-filens innehåll?

En XPI-fil är praktiskt taget ett ZIP-arkiv vars innehåll kan ses med följande steg.

* Ändra filtillägget från XPI till ZIP
* Extrahera innehållet i filen med valfritt standardverktyg för dekomprimering som WinZip (Windows, Mac), 7-Zip (Windows) eller Apple Archive Utility (Mac).

### Installera XPI-fil på Firefox Android

Oftast är människor nyfikna på att veta om XPI-filer kan installeras i Firefox på Android-enheter. På Android kan du installera tillägg från en XPI-fil genom att hitta filen och öppna den med Firefox.

## Referenser

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Hur kan jag öppna ett XPI-filtillägg?](https://support.mozilla.org/en-US/questions/1009049)

