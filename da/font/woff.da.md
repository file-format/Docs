{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - Web Open File Format",
  "description": "En WOFF-fil er et åbent skrifttypeformat, der er oprettet i Web Open Font Format.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-daf"
}
},
  "lastmod": "2020-09-30"
}

## Hvad er WOFF fil?

En fil med filtypen .woff er en webskrifttypefil baseret på Web Open Font Format (WOFF). Den har formatspecifik komprimeret beholder baseret på enten TrueType (.TTF) eller OpenType (.OTT) skrifttypetyper. WOFF blev introduceret med det formål at adskille webskrifttyper fra skrifttyper, der bruges i desktopapplikationer. Derudover er formatet målrettet mod at reducere latensen af skrifttypers overførsel fra server til klients computer over netværket. Adskillige værktøjer er tilgængelige, der kan konvertere WOFF-filer til TTF og andre skrifttypefilformater.

## WOFF filformat

WOFF-skrifttypeformat komprimerer skrifttypedatatabeller af tabelbaserede sfnt-strukturer, der bruges i forskellige skrifttyper såsom TrueType, OpenType og Open Font Format. Det er som en beholder til disse skrifttyper og har også plads til at inkludere fontens metadata og privatbrugsdata, der skal inkluderes i beholderen. Konvertere bruger sfnt-filerne til en WOFF-formateret fil, og brugeragenter gendanner den kodede fil til brug med webdokumentet. Det skal bemærkes, at de gendannede skrifttypedata nøjagtigt matcher inputskrifttypeformatet fra alle aspekter.

WOFF-filværktøjer indeholder ofte yderligere funktioner såsom glyf-underindstilling, validering eller tilføjelse af skrifttypefunktioner, men det er ikke nødvendigt. Både skaberen og brugeren skal sikre, at gyldigheden af de underliggende skrifttypedata bevares.

### WOFF-filstruktur

WOFF-filstrukturen ligner den for sfnt-skrifttyper. Den er baseret på en tabelmappe, der indeholder længder og forskydninger til hver skrifttypedatatabeller. Alle tabeller følges efter denne indledende information. Filen indeholder skrifttypedatabase, der er de samme som i de originale skrifttyper. Rækkefølgen af bordene er også den samme, men hver enkelt kan være komprimeret. WOFF tabel bibliotek erstatter dog den oprindelige tabel mappe.

En WOFF-fil består af følgende:

 * WOFFHeader - Filoverskrift med grundlæggende skrifttype og version, sammen med forskydninger til metadata og private datablokke.
 * TableDirectory - Katalog over skrifttypetabeller, der angiver den originale størrelse, komprimerede størrelse og placering af hver tabel i WOFF-filen.
 * FontTables - Skrifttypedatatabellerne fra input-sfnt-skrifttypen, komprimeret for at reducere båndbreddekravene.
 * ExtendedMetadata - En valgfri blok af udvidede metadata, repræsenteret i XML-format og komprimeret til lagring i WOFF-filen.
 * PrivateData- En valgfri blok af private data, som skrifttypedesigneren, støberiet eller sælgeren kan bruge.

### WOFF Header
WOFF-headeren består af en identificerende signatur, som angiver typen af data, der er inkluderet i filen. WOFF-headeren sammen med dens felter er som følger.

|Type|Feltnavn|Beskrivelse|
---|---|---|
|UInt32|signatur |0x774F4646 'wOFF' |
|UInt32| flavor |sfnt-versionen af inputskrifttypen.|
|UInt32| længde |Samlet størrelse af WOFF-filen.|
|UInt16| numTables |Antal poster i biblioteket med skrifttypetabeller.|
|UInt16| reserveret |Reserveret; sat til nul.|
|UInt32| totalSfntSize |Samlet størrelse påkrævet for de ukomprimerede skrifttypedata, inklusive sfnt-headeren, mappen og skrifttypetabellerne (inklusive udfyldning).|
|UInt16| majorVersion |Større version af WOFF-filen.|
|UInt16| minorVersion |Mindre version af WOFF-filen.|
|UInt32| metaOffset |Offset til metadatablok, fra begyndelsen af WOFF-fil.|
|UInt32| metaLength |Længde af komprimeret metadatablok.|
|UInt32| metaOrigLength |Ukomprimeret størrelse af metadatablok.|
|UInt32| privOffset |Offset til privat datablok, fra begyndelsen af WOFF-fil.|
|UInt32| privLength |Længde på privat datablok.|

## Referencer

 * [w3 WOFF-filformat](https://www.w3.org/TR/WOFF/)

