{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF2-fil - Web Open Font Format 2.0-fil",
  "description": "Lær om, hvad en WOFF2-fil og API'er er, der kan oprette og åbne WOFF2-fil.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-da2"
}
},
  "lastmod": "2023-01-10"
}

## Hvad er WOFF2 fil?

WOFF2 er et skrifttypefilformat, der er en mere komprimeret version af Web Open Font Format (WOFF). Det blev udviklet som en måde at reducere filstørrelsen på webskrifttyper, så de kan indlæses hurtigere og bruge mindre båndbredde. WOFF2 bruger en komprimeringsalgoritme kaldet Brotli til at komprimere skrifttypedataene, hvilket kan resultere i filstørrelser, der er væsentligt mindre end tilsvarende [WOFF](/font/woff/) skrifttyper. Dette format understøttes af de fleste moderne webbrowsere inklusive Chrome, Firefox, Safari, Opera og Edge (version 14 og frem).

## WOFF2 filformat - flere oplysninger

Den interne filstruktur af en WOFF2-skrifttypefil er sammensat af flere forskellige dele, herunder en header, metadata, en tabelmappe og selve skrifttypedataene.

 1. Headeren indeholder information om filens overordnede format, herunder versionsnummeret og antallet af tabeller, der er til stede i filen.

 1. Metadatasektionen indeholder oplysninger såsom skrifttypenavn, copyright og andre skrifttyperelaterede oplysninger.

 1. Tabelbiblioteket indeholder information om de forskellige tabeller, der udgør skrifttypen, inklusive deres placering i filen og deres længde.

 1. Selve skrifttypedataene er opdelt i flere forskellige tabeller, som hver indeholder specifikke oplysninger om skrifttypen, såsom dens tegn og deres tilsvarende glyffer. Disse tabeller kan omfatte:

 * Glyf'-tabellen indeholder de faktiske skrifttyper, inklusive formen og størrelsen af hvert tegn.
 * Hoved'-tabellen indeholder generelle oplysninger om skrifttypen, såsom dens versionsnummer, designstørrelse og så videre.
 * hmtx'-tabellen indeholder oplysninger om metrikken for skrifttypen, herunder tegnernes bredder og positioner.
 * Hver tabel komprimeres og gemmes i WOFF2-filformat, efter at den har fuldført kodningsprocessen.

Strukturen er generelt designet til at give mulighed for hurtig parsing og afkodning, så webbrowsere hurtigt og effektivt kan indlæse og vise skrifttypen på et websted.

### WOFF2 Header
WOFF-headeren består af en identificerende signatur, som angiver typen af data, der er inkluderet i filen. WOFF-headeren sammen med dens felter er som følger.

|Type|Feltnavn|Beskrivelse|
---|---|---|
|UInt32|signatur |0x774F4632 'wOF2' |
|UInt32| flavor |sfnt-versionen af inputskrifttypen.|
|UInt32| længde |Samlet størrelse af WOFF-filen.|
|UInt16| numTables |Antal poster i biblioteket med skrifttypetabeller.|
|UInt16| reserveret |Reserveret; sat til nul.|
|UInt32| totalSfntSize |Samlet størrelse påkrævet for de ukomprimerede skrifttypedata, inklusive sfnt-headeren, mappen og skrifttypetabellerne (inklusive udfyldning).|
|UInt32| totalCompressedSize Samlet længde af den komprimerede datablok.|
|UInt16| majorVersion |Større version af WOFF-filen.|
|UInt16| minorVersion |Mindre version af WOFF-filen.|
|UInt32| metaOffset |Offset til metadatablok, fra begyndelsen af WOFF-fil.|
|UInt32| metaLength |Længde af komprimeret metadatablok.|
|UInt32| metaOrigLength |Ukomprimeret størrelse af metadatablok.|
|UInt32| privOffset |Offset til privat datablok, fra begyndelsen af WOFF-fil.|
|UInt32| privLength |Længde på privat datablok.|


## Referencer
 * [w3 WOFF2 filformat](https://www.w3.org/TR/WOFF2/)

