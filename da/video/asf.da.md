{
  "date": "2021-02-15",
  "keywords": [
"asf-fil",
"asf filformat",
"hvad er en asf-fil",
"fil",
"asf eksempel",
"asf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF - Advanced Systems File Format",
  "description": "Lær om ASF-filformat og API'er, der kan oprette og åbne ASF-filer.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-daf"
}
},
  "lastmod": "2021-02-16"
}

## Hvad er en ASF fil?

En fil med filtypenavnet .asf er et multimediefilformat til lagring og afspilning af digitale mediestreams over netværket. Det er et containerfilformat, der kan have både video- og lydindhold til streaming online. Du vil sjældent finde ASF-filer, og flere vil sandsynligvis støde på Windows Media Audio ([WMA](/audio/wma/)) og Windows Media Video ([WMV](/video/wmv/)), som begge specificerer ASF-filer med indhold kodet med respektive codecs. Windows mediefiler kan oprettes og læses ved hjælp af Windows Media Format SDK.

## ASF filformat

En ASF-fil kan omfatte flere uafhængige eller afhængige strømme. Dette kan omfatte flere lydstreams til flerkanalslyd eller videostreams med flere bithastigheder. De mange bithastigheder gør strømmene velegnede til transmission over forskellige båndbredder. Desuden kan streams i en ASF-fil være i komprimeret eller ukomprimeret format. Den bedste komprimering opnås med Microsoft Windows Media Audio og Video 9 Series codecs. Komplette specifikationer for ASF-filformat er tilgængelige på [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF-filstruktur på topniveau

ASF-filer indeholder logisk set tre typer objekter på øverste niveau:

* "Header Object" - obligatorisk og skal placeres i begyndelsen af hver ASF-fil

* `Data Object` - obligatorisk og skal følge header-objektet

* `Indeksobjekt(er)` - valgfrit, men nyttigt til at give tidsbaseret tilfældig adgang til ASF-filer


Følgende billede viser filstrukturen på øverste niveau af ASF-filer.

![ASF File Structure](../asf.png "ASF File Structure")

#### ASF Top-Level Header Object

Header-objektet giver en velkendt bytesekvens i begyndelsen af ASF-filerne og kan eventuelt indeholde metadata såsom bibliografisk information. Den indeholder alle de oplysninger, der er nødvendige for at fortolke oplysningerne i dataobjektet korrekt. Header-objektet kan omfatte flere standardobjekter, herunder, men ikke begrænset til:

 * Filegenskabsobjekt - Indeholder globale filattributter.
 * Stream Properties Object - Definerer en digital mediestrøm og dens karakteristika.
 * Header Extension Object - Giver mulighed for at tilføje yderligere funktionalitet til en ASF-fil, samtidig med at den bibeholder bagudkompatibilitet.
 * Indhold Beskrivelse Objekt - Indeholder bibliografisk information.
 * Script Command Object - Indeholder kommandoer, der kan udføres på afspilningstidslinjen.
 * Markørobjekt - Giver navngivne springpunkter i en fil.

Header-objektet er repræsenteret ved hjælp af følgende struktur:

|Feltnavn |Felttype |Størrelse (bits)|
---|---|---|
|Objekt ID| GUID| 128|
|Objektstørrelse| QWORD| 64|
|Antal overskriftsobjekter| DWORD| 32|
|Reserveret1| BYTE| 8|
|Reserveret2| BYTE| 8|

#### ASF Top-Level Data Object

Alle digitale mediedata for en ASF-fil er indeholdt i dataobjektet og gemmes i form af ASF-datapakker. Hver datapakke har en fast længde og indeholder data for en eller flere digitale mediestrømme.

#### ASF Top-Level Index Objekter

ASF-indeksobjekter på øverste niveau har følgende to typer:

 * `Simple Index Object` - Indeholder et tidsbaseret indeks over videodataene i en ASF-fil. Tidsintervallet mellem indeksindtastninger er konstant og gemmes i Simple Index Object.
 * `Indeksobjekt` - Refererer til indeksobjektet, medieobjektindeksobjektet og tidskodeindeksobjektet, hvis formater ligner hinanden. Ligesom Simple Index Object indekserer Index Object efter tid med et fast tidsinterval, men er ikke begrænset til videostreams.

## Referencer

* [ASF-filformat - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [QuickTime-filformat - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


