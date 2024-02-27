{
  "date": "2019-10-11",
  "keywords": [
"exif-fil",
"exif filformat",
"hvad er en exif-fil",
"fil",
"exif eksempel",
"exif filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EXIF",
  "description": "Lær om EXIF-filformat og API'er, der kan oprette og åbne EXIF-filer.",
  "linktitle": "EXIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-exi-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en EXIF fil?
EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. Standarden administreres af Japan Electronics and Information Technology Industries Association (JEITA) fra og med i dag. EXIF er en standard for specifikationer for billed- og lydformater, der hovedsageligt anvendes af digitale kameraer og scannere.

EXIF-standarden inkluderer tagging og metadataoplysninger med billedfilen. Metadata kan indeholde oplysninger som kameramodel, lukkertid, dato og tid, blænde, producent, eksponeringstid, X-opløsning, Y-opløsning osv. Normalt er EXIF-data skjult som standard. For at se EXIF-dataene skal man vælge visningsegenskaberne i billedvisningsapplikationen. Exif-metadata kan også omfatte thumbnails sammen med tekniske og primære billeddata i en enkelt billedfil.

## Historik og versioner ##

* I oktober 1995 etablerede JEIDA version 1. I denne version definerede JEIDA strukturen, som består af billeddataformat og attributoplysninger og grundlæggende tags.

* Nov 1997, version 1.1 blev introduceret med de fleste tags fra version 1, men tilføjede også bestemmelser for valgfri attributinformation og formatoperation.

* Juni 1998, version 2 med sRGB-farverum, komprimerede thumbnails og lydfiler.

* December 1998, version 2.1 med forbedret lagring og attributoplysninger.

* Februar 2002, version 2.2, forbedret version 2.1 med tilføjelse af efterbehandling af print.

* September 2003, version 2.21 med valgfrit farverum kendt som adobe RGB.


## EXIF filformat

EXIF bruger følgende filformater med tilføjelse af specifikke metadata.

1. [JPEG](/image/jpeg/) - diskret cosinustransformation (DCT) for komprimerede billedfiler.
1. [TIFF](/image/tiff/) Rev. 6.0 (RGB eller YCbCr) til ukomprimerede billedfiler.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) til lydfiler (Lineær [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) eller ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM til ukomprimerede lyddata, og [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) for komprimerede lyddata).

### Markør brugt af EXIF ###

Markøren 0xFFE0~~0xFFEF er Application Marker, der bruges af brugerapplikationen. For eksempel bruger ældre digi-kameraer JFIF (JPEG File Interchange Format) til lagring af billeder. JFIF bruger APP0 (0xFFE0) Marker til at indsætte digi cam-konfigurationsdata og miniaturebillede. Ydermere bruger EXIF også en Application Marker til at indsætte data, men EXIF bruger APP1 (0xFFE1) Marker for at undgå en konflikt med JFIF-formatet. Alle EXIF-filformater starter fra dette format.


|SOI Marker|APP1 Marker|APP1 Data|Anden Markør
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Det starter fra SOI (0xFFD8) Marker, så det er en JPEG-fil. Så følger APP1 Marker med det samme. Alle data fra EXIF er gemt i dette APP1-dataområde. Den del af SSSS i den øverste tabel betyder størrelsen af APP1 dataområde (EXIF dataområde). Bemærk venligst, at størrelsen SSSS også inkluderer størrelsen på selve beskrivelsen. Efter SSSS starter APP1-data. Den første del er en speciel data til identifikation om EXIF eller ej, ASCII-tegn EXIF og 2 bytes på 0x00 bruges. Efter APP1 Marker området følger de andre JPEG Markers.

### Exif-datastruktur ###

En grov struktur af EXIF-data (APP1) er vist som nedenfor. Som diskuteret ovenfor starter EXIF-data fra ASCII-tegn EXIF og 2 bytes på 0x00, derefter følger EXIF-data. EXIF bruger TIFF-format til at gemme data.


|FFE1|APP1 Markør
---|---|
|SSSS|APP1 Data|APP1 Datastørrelse
|45786966 0000|Exif Header
|49492A00 08000000|TIFF-hoved
|XXXX. . . .|IFD0 (hovedbillede)|Bibliotek
|LLLLLLLL|Link til IFD1
|XXXX. . . .|Dataområde for IFD0
|XXXX. . . .|Exif SubIFD|Directory
|00000000|Slut på link
|XXXX. . . .|Dataområde i Exif SubIFD
|XXXX. . . .|IFD1(miniaturebillede)|Mappe
|00000000|Slut på link
|XXXX. . . .|Dataområde for IFD1
|FFD8XXXX. . . XXXXFFD9|Miniaturbillede

#### TIFF Header ####

den 8-byte [TIFF](/image/tiff/) filoverskrift indeholder følgende information:

`Bytes 0-1:` Byte-rækkefølgen brugt i filen. Lovmæssige værdier er:II(4949.H)MM (4D4D.H).

I II-formatet er byte-rækkefølgen altid fra den mindst signifikante byte til den mest signifikante byte, for både 16-bit og 32-bit heltal. Dette kaldes little-endian byte-rækkefølge. I MM-formatet er byterækkefølgen altid fra mest signifikant til mindst signifikant, for både 16-bit og 32-bit heltal. Dette kaldes big-endian byte-rækkefølge.

`Bytes 2-3:` Et vilkårligt, men omhyggeligt valgt tal (42), der yderligere identificerer filen som en TIFF-fil. Byterækkefølgen afhænger af værdien af bytes 0-1.

`Bytes 4-7:` Forskydningen (i bytes) af den første IFD. Biblioteket kan være et hvilket som helst sted i filen efter overskriften, men skal begynde på en ordgrænse. Især kan en billedfilkatalog følge de billeddata, den beskriver. Læsere skal følge pegepindene, hvor end de måtte føre. Udtrykket byte offset bruges altid i dette dokument til at henvise til en placering i forhold til begyndelsen af TIFF-filen. Den første byte af filen har en offset på 0.

#### Billedfilkatalog ####

En IFD indeholder information om billedet samt pointere til de faktiske billeddata. Den består af en 2-byte tælling af antallet af adressebogsposter (dvs. antallet af felter), efterfulgt af en sekvens af 12-byte feltindgange , efterfulgt af en 4-byte offset af den næste IFD (eller 0, hvis ingen). Der skal være mindst 1 IFD i en TIFF-fil, og hver IFD skal have mindst én post.

##### IFD Entry #####

Hver 12-byte IFD-indgang er i følgende format.


|Bytes|Beskrivelse
---|---|
|0-1|Tag, der identificerer feltet
|2-3|Felttypen
|4-7|Optælling af den angivne type
|8-11|Værdiforskydningen, filforskydningen (i bytes) af værdien for feltet. Værdien forventes at begynde på en ordgrænse; den tilsvarende Værdiforskydning vil således være et lige tal. Denne filforskydning kan pege et vilkårligt sted i filen, selv efter billeddataene

Et TIFF-felt er en logisk enhed, der består af TIFF-tag og dets værdi. Dette logiske koncept er implementeret som en IFD-indgang, plus den faktiske værdi, hvis den ikke passer ind i værdi/offset-delen, de sidste 4 bytes af IFD-indgangen. Begreberne TIFF-felt og IFD-indtastning er udskiftelige i de fleste sammenhænge.

#### Miniaturebillede ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. Der er 3 formater til thumbnails; JPEG-format (JPEG bruger YCbCr), RGB TIFF-format, YCbCr TIFF-format.

##### JPEG-format miniature #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. Det ser ud til, at JPEG-format og 160 x 120 pixel i størrelse er anbefalet thumbnail-format til Exif2.1 eller nyere.

##### TIFF-format miniaturebillede #####

Hvis værdien af Compression(0x0103) Tag i IFD1 er '1', er thumbnail-billedformatet ingen komprimering (kaldet TIFF-billede). Startpunktet for thumbnaildata er StripOffset(0x0111) Tag, størrelsen af thumbnail er summen afStripByteCounts(0x0117) Tag.

## Referencer ##

* [EXIF - af Wikipedia](https://en.wikipedia.org/wiki/Exif)

* [EXIF-filformat](https://www.media.mit.edu/pia/Research/deepview/exif.html)


