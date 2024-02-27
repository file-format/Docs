{
  "date": "2020-08-20",
  "keywords": [
"ttf filen",
"ttf filformat",
"hvad er en ttf-fil",
"fil",
"ttf eksempel",
"ttf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TTF - TrueType Font File Format",
  "description": "TrueType-skrifttyper (TTF) er baseret på specifikationer for digital skrifttypeteknologi, som oprindeligt er designet af Apple, Inc. Både Apple og Microsoft brugte TTF på Mac- og Windows-operativsystemer.",
  "linktitle": "TTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-daf"
}
},
  "lastmod": "2020-09-21"
}

## Hvad er TTF fil?

En fil med filtypenavnet .ttf repræsenterer skrifttypefiler baseret på TrueType-specifikationernes skrifttypeteknologi. Det blev oprindeligt designet og lanceret af Apple Computer, Inc til Mac OS og blev senere adopteret af Microsoft til Windows OS. TrueType-skrifttyper giver visning af højeste kvalitet på computerskærme og printere uden nogen afhængighed af opløsning. Alle moderne applikationer, der bruger skrifttyper, er i stand til at arbejde med TTF-filer. TTF-skrifttypefiler er frit tilgængelige over internettet og kan også konverteres til andre skrifttypefilformater såsom OTF og WOFF.

## Kort historie

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. Designmålet bag TTF-skrifttyper var effektivitet i lagring og behandling og udvidelsesmuligheder. Baseret på denne udvidelsesmulighed kan eksisterende skrifttyper konverteres til TrueType-format.

Microsoft brugte først TrueType-skrifttyperne i Windows 3.1 i april 1992, efter at Apple indvilligede i at licensere TrueType til Microsoft. Det forbedrede rasteriseringsmekanismen og forbedrede dens effektivitet og ydeevne.

## True Type filformatspecifikationer

En TrueType-skrifttypefil er en binær fil, der består af en sekvens af sammenkædede tabeller. Hver tabel er en sekvens af ord og har et navn kendt som Tag. Hvert tag er af uint32-datatypen og består af fire tegn. Den første tabel i filen er fontmappe, der giver adgang til andre tabeller i fontfilen. Skrifttypedata er indeholdt i andre tabeller efterfulgt af skrifttypekatalogtabellen. Da hver tabel er tilgængelig via dens tag, kan tabellerne vises i en hvilken som helst rækkefølge i filen.

De påkrævede tabeller og deres tagnavne er vist i følgende tabel.

|**Tag**|**Tabel**|
---|---|
|'cmap'| tegn til glyph mapping|
|'glyf'| glyfdata|
|'hoved'| skrifttypeoverskrift|
|'hhea'| vandret overskrift|
|'hmtx'| vandrette metrikker|
|'loca'| indeks til placering|
|'maxp'| maksimal profil|
|'navn'| navngivning|
|'indlæg'| PostScript|

### Datatyper
TrueType-skrifttyper bruger standard heltal og yderligere datatyper som angivet i følgende tabel.

|**Datatype** | **Beskrivelse** |
---|---|
|shortFrac| 16-bit fortegnet brøk|
|Fixet| 16,16-bit signeret fikspunktnummer|
|FWord| 16-bit fortegnet heltal, der beskriver en mængde i FUnits, den mindste målbare afstand i em rum.|
|uFWord| 16-bit heltal uden fortegn, der beskriver en mængde i FUnits, den mindste målbare afstand i em rum.|
|F2Punkt14| 16-bit fortegnet fast tal med de lave 14 bits repræsenterende brøk.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Font Directory

Den første tabel i TrueType-skrifttypen er den skrifttypemappe, der giver adgang til de oplysninger, der kræves for at få adgang til data i andre tabeller. Den består yderligere af:

 * `Offset subtable` - registrerer tabellerne i skrifttypen og giver offset information for at få adgang til hver tabel i mappen
 * `Table Directory` - Indeholder indgange for hver tabel i skrifttypen

#### Offset undertabel
Offset-undertabellen er vist nedenfor.

|**Type**|**Navn**|**Beskrivelse**|
---|---|---|
|uint32| scaler type| Et tag til at angive den OFA-skalering, der skal bruges til at rasterisere denne skrifttype; se bemærkningen om scaler-typen nedenfor for mere information.|
|uint16| antal Tabeller| antal borde|
|uint16| søgeområde| (maksimal potens af 2 <= antal Tabeller)*16|
|uint16| entrySelector| log2(maksimal potens af 2 <= antal Tabeller)|
|uint16| rangeShift| antal Tabeller*16-søgeområde|

#### Tabelmappe
Tabelbiblioteket kommer lige efter offset-undertabellen. Dens struktur er som vist i følgende tabel.

|**Type**|**Navn**|**Beskrivelse**|
---|---|---|
|uint32| tag| 4-byte identifikator|
|uint32| checkSum| kontrolsum for denne tabel|
|uint32| offset| forskydning fra begyndelsen af sfnt|
|uint32| længde| længden af denne tabel i byte (faktisk længde ikke polstret længde)|

Hver tabel i en skrifttypefil skal have sin egen tabelmappeindgang. Indgange i en tabel skal sorteres i stigende rækkefølge efter tag.


## Referencer
 * [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [TrueType Oversigt](https://learn.microsoft.com/en-us/typography/truetype/)

