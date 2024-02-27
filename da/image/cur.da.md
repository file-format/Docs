{
  "date": "2021-06-29",
  "keywords": [
"CUR",
"udvidelse",
"fil",
"format",
"billede",
"Enhedsuafhængig bitmap",
"Markør filformat",
"cursoren",
"Windows",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CUR - Markørfilformat",
  "description": "Lær om CUR filformat og API'er, der kan oprette og åbne CUR filer.",
  "linktitle": "CUR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-cu-dar"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er CUR fil? ##

En CUR-fil er et statisk Microsoft Windows-markørfilformat. Grundlæggende er de stationære billeder, der er identiske med ICO-filer (ikon) på alle måder undtagen udvidelsen. Både CUR og [ICO](/image/ico/) er etableret på basis af Device-Independent Bitmap [DIB](/image/dib/) (Device-Independent Bitmap) specifikation. Standard, såvel som brugerdefineret markør, såsom Windows-musemarkør til Windows-operativsystemet, er gemt i CUR-filer. Det kan være en pil til normal brug, et snurrende timeglas til at demonstrere venteperioder eller en I-bar til tekstredigering. CUR-filer kommer sammen med installationspakken til de brugerdefinerede skrivebordstemaer for at sikre, at Windows-markøren matcher det brugerdefinerede skrivebordstema.

## Teknisk specifikation ##

CUR filer er binære systemfiler, der kan findes på enheder, der fungerer på Microsoft Windows-operativsystemet. CUR-markørbilleder kommer i forskellige standardstørrelser som 16×16, 32×32 osv. CUR-filer minder meget om ICO-filerne; begge består af små stationære billeder. Kun udvidelsen af CUR- og ICO-filer er forskellige. Ydermere er forklaringen på et hotspot i headeren af CUR-filen forskellig fra ICO-filen. Hotspottet fortolker pixelforskydningen fra øverste venstre hjørne til det sted, hvor du peger med musen. Windows-systemer bruger stadig CUR-filerne, men nu har de animerede markører normalt filtypenavnet ANI i stedet for CUR.

## Kort historie ##

CUR-filen er lavet ud fra ICO-filen. Det første CUR-filformat blev indarbejdet i Microsofts Windows 1.0-operativsystem i 1981 for at udjævne kommerciel brug. Snart blev mere interaktive markører introduceret, så brugerne kunne ændre deres markørpræferencer fra de forhåndsinstallerede muligheder. Det er dog nemt at redigere en CUR-fil på egen hånd, selvom du ikke har tilstrækkelig teknisk viden.


## CUR eksempel ##

CUR-filerne kan findes på *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="CUR filformat" >}}

