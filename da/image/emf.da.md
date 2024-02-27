{
  "date": "2019-10-11",
  "keywords": [
"emf fil",
"emf filformat",
"hvad er en emf fil",
"fil",
"emf eksempel",
"emf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF - Forbedret metafilformat",
  "description": "Lær om EMF filformat og API'er, der kan oprette og åbne EMF filer.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en EMF fil?

**Forbedret metafilformat (EMF)** gemmer grafiske billeder enhedsuafhængigt. Metafiler af EMF består af poster med variabel længde i kronologisk rækkefølge, der kan gengive det lagrede billede efter parsing på enhver outputenhed. Disse registreringer med variabel længde kan være definitioner af lukkede objekter, kommandoer til tegning og grafikegenskaber, der er afgørende for at gengive billedet nøjagtigt. Når en enhed åbner en EMF-metafil ved hjælp af sit eget grafikmiljø, forbliver proportionerne, dimensionerne, farverne og andre grafiske egenskaber af det originale billede de samme uanset åbningsenhedens platform.

## Kort historie ##

I 1990 designede Microsoft et billedfilformat Windows Metafile ([WMF](/image/wmf/)) til Microsoft Windows. Windows-metafiler er 16-bit-format, der kan indeholde nogle bitmap-komponenter. WMF kan bestå af vektorgrafik og er beregnet til at være bærbar mellem forskellige programmer. I 1993 annoncerede Win32/GDI Enhanced Metafile (EMF), en nyere version med forbedret fleksibilitet og skalerbarhed. EMF bruges også som grafiksprogkommandoer til at køre printerdriverne. Microsoft anbefaler nu det forbedrede metafilformat (EMF) over Windows-format (WMF). Da Windows XP blev introduceret, blev versionen Enhanced Metafile Format Plus (EMF+) frigivet. Denne nyere version finder vej ved at serialisere GDI+ API-kald, ligesom WMF/EMF registrerer opkald til GDI. Der findes en gzip-komprimeret version af EMF kendt som EMZ.

## EMF-metafilformat ##

Følgende er de væsentlige elementer i det forbedrede metafil-format:

* En EMR_HEADER (version, størrelse, opløsningen af billedet ved oprettelsen)

* En tabel for GDI-objekter

* En reserveret palette (valgfrit)

* Metafilposter arrangeret i matrixstruktur (egenskabsindstillinger, definerede objekter, tegnekommandoer)

* EMR_EOF-post (sidste post i EMF-metafilen)


## EMF-versioner ##
* **Original**: Den originale version specificerer den registrering, der er nødvendig for at bevare det originale billede og bevare dets enhedsuafhængig. Understøtter desuden posten, der indeholder grafikobjekter og kommandoer til tegning.

* **Version 1**: Den anden version af EMF forbedrede fleksibiliteten og enhedens uafhængighed ved at tilføje posten for pixelformat og levering for at bruge OpenGL-kommandoen.

* **Version 2**: Den tredje version forbedrede nøjagtigheden ved at tilføje det metriske system til at måle enhedens overfladeafstande, hvilket efterlod posten mere skalerbar.


## Forbedrede metafilposter ##

Metafilposter er arrangeret i form af array. Disse poster har ENHMETARECORD-struktur og variabel i længde. ENHMETARECORD specificerer data, der definerer GDI-funktioner for at skabe et billede ved hjælp af forbedret metafilformat. **ENHMETAHEADER** struktur er altid den første post i dette format. Denne EMF-header indeholder følgende information.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

Der skal være mindst én EMF-post i hver metafil. Overførselsinformationen fra én post til en anden er afhængig af EMF-poster, så disse poster skal arrangeres ved siden af hinanden. Ved enhver given post i metafilen undtagen EOF_record, definerer længden af den pågældende post for at flytte til den næste post.

## Forbedret metafiloprettelse ##

Funktionen **CreateEnhMetaFile** bruges til at oprette en forbedret metafil. Denne funktions argumenter bruges til dimensioner og lagring af billede på disk/hukommelse. Desuden kræver denne funktion dimensionen af den enhed, hvor billedet dukkede op først (referenceenhed) og konteksten for referenceenheden (DC). Så argumenterne for at håndtere denne DC skal give, når funktionen **CreateEnhMetaFile** kaldes. Syntaksen for funktion er som følger:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** håndtag til en referenceenhed.

**lptoFilename:** En pegepind til filnavnet.

**lprc:** Pointer til oval struktur angiver billedets dimensioner i mm.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Forbedrede metafiloperationer ##

Følgende er job, der kan udføres ved at bruge håndtaget til en forbedret metafil.

* Vis og rediger for det gemte billede.

* Fremstil forbedrede metafil-kopier.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Rekapituler farverne i paletten.


## Grafikobjekter ##

I tegne- og maleoperationer kan grafiske objekter oprettes ved hjælp af objektoprettelsesposter og kan gemme til videre brug. En `EMR_SELECTOBJECT`-post kan hente disse grafikobjekter ved hjælp af afspilningsenhedskonteksten. Kuglepenne, paletter, pensler, farverum, skrifttyper og lagerobjekter er nogle genanvendelige objekttyper.

## Bytebestilling ##

Little-endian format bruges til at gemme data i metafilposter.

## Version ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Udvidede versioner har mulighed for OpenGL-poster og en valgfri deskriptor for internt pixelformat. En målefacilitet i milliliter tilføjes for viste dimensioner.

## Referencer ##

* [Forbedret-format metafiler | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [Forbedret metafilformat og specifikation](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


