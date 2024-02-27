{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "XPI - Cross-platform Installer Package File",
  "description":"Lær om XPI-filformat og API'er, der kan oprette og åbne XPI-filer.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi-da",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Hvad er en XPI fil?

En XPI-fil er et installationsarkiv, der er komprimeret for at reducere størrelsen af filen. Det bruges af Mozilla-applikationer til installation af plugins og tilføjelsesfiler. Den indeholder et installationsscript eller et manifest i roden af filen sammen med en række datafiler. En XPI-fil kan indeholde temaer, værktøjssæt eller Firefox-plugins, som brugeren kan installere for at blive en del af Firefox-browseren, Thunderbird eller SeaMonkey.

## XPI-filformat - flere oplysninger

XPI-filer gemmes på disken som [ZIP](/compression/zip/)-arkiver, der kombinerer flere filer til en enkelt komprimeret fil. Filerne i en XPI-fil kan indeholde installationsscriptfiler såsom JS og webfiler såsom [CSS](/web/css/), [HTML](/web/html/) og [JSON](/web/json/). Nogle gange kan den også indeholde [PNG](/image/png/) billedfiler, der skal bruges som ikoner af tilføjelse.

### Hvordan får man vist XPI-filens indhold?

En XPI-fil er praktisk talt et ZIP-arkiv, hvis indhold kan ses ved hjælp af følgende trin.

 * Skift filtypenavnet fra XPI til ZIP
 * Udpak indholdet af filen ved hjælp af et hvilket som helst standard dekomprimeringsværktøj, såsom WinZip (Windows, Mac), 7-Zip (Windows) eller Apple Archive Utility (Mac).

### Installer XPI-fil på Firefox Android

For det meste er folk nysgerrige efter at vide, om XPI-filer kan installeres i Firefox på Android-enheder. På Android kan du installere tilføjelse fra en XPI-fil ved at finde filen og åbne den med Firefox.

## Referencer

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)

* [Hvordan kan jeg åbne en XPI-filudvidelse?](https://support.mozilla.org/en-US/questions/1009049)


