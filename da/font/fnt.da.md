{
  "date": "2020-08-20",
  "keywords": [
"fnt-fil",
"fnt filformat",
"hvad er en fnt-fil",
"fil",
"fnt eksempel",
"fnt filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FNT - Windows-skrifttypefil",
  "description": "Lær om FNT-filformater og API'er, der kan oprette og åbne FNT-filer.",
  "linktitle": "FNT",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-fn-dat"
}
},
  "lastmod": "2020-10-30"
}

## Hvad er en FNT fil?

En fil med filtypenavnet .fnt er en skrifttypefil, der gemmer generiske skrifttypeoplysninger på Windows-operativsystemer. FNT-filer er for det meste blevet erstattet af filformaterne TrueType (.TTF) og OpenType (.OTF), og er et forældet skrifttypefilformat fra nu af. Disse filer kan gemme en enkelt rater eller vektorskrifttype. Alle enhedsdrivere understøtter Windows 2.x-skrifttyperne. Dog ikke alle enhedsdrivere
understøtter Windows 3.0-versionen.

## FNT filformat

FNT-filer er i stand til at gemme en enkelt raster- eller vektorskrifttype. Vektorformaterne bruges oftere af GDI sammenlignet med rasteret, hvor hvert charters glyph er defineret ved hjælp af en lille bitmap. Den åbenlyse årsag til udskiftningen af .fnt med .ttf og .otf er dets rasterformat.

### Skrifttypefiloverskrift
Starten af både raster- og vektorskrifttypefiler er fælles, efterfulgt af forskellige oplysninger for hver filtype. Skrifttype-filens overskrift inkluderer til Windows 3.0 inkluderer seks nye felter som følger, som er sat til nul for at sikre kompatibilitet med fremtidige versioner af Windows.

 * dFlag
 * dfAspace
 * dfBspace
 * dfCspace
 * dfColorPointer
 * dfReserveret1

Besøg [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/) for detaljerede oplysninger om overskrifterne til Windows 3.0 og 2.0.

## Referencer
 * [Skriftfilformat](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
 * [Sådan installerer eller fjerner du en skrifttype i Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8- 7613-c76f-88d043b334b8)

