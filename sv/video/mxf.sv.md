{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Material Exchange Format",
  "keywords" :[ "MXF", "matroska video", "mkv-format", "hur man spelar MXF-filer", "SMPTE", "multimedia", "video" ],
  "description":"Läs mer om MXF-filformat och API:er som kan skapa och öppna MXF-filer.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Vad är en MXF-fil?

En fil med filtillägget .mxf är ett multimediacontainerformat som innehåller digitala video- och ljudmedia tillsammans med metadatainformation om filen. Den följer SMPTE-standarden (Society of Motion Picture and Television Engineers) som är en global sammanslutning av yrkesverksamma från ingenjörer, teknik och chefer som arbetar inom media- och underhållningsbranschen. MXF-filer kan konverteras till andra filformat som [AVI](/sv/video/avi/) eller [MOV](/sv/video/mov/).

## MXF filformat

MXF-filer är i själva verket binära filer som består av en sekvens av byte i ett bestämt format. Avkodningsapplikationer måste vara kompatibla med detta format för att förstå det och extrahera information från det. Formatet tillåter att lägga till nya objekt utan att bryta bakåtkompatibiliteten med hjälp av KLV-kodningen som beskrivs nedan.

* Nyckel – elementets identifierare, en SMPTE Universal Label (UL)
* Längd – längden på data som är kodningen med variabel längd som används för att minska mängden utrymme som krävs för detta objekt
* Värde – det faktiska värdet på elementet.

### SMPTE-formatspecifikationer

MXF-filformatet har definierats av följande SMPTE-specifikationer.

* SMPTE ST 377-1:2011. Television — Material Exchange Format (MXF) — Filformatspecifikation
* SMPTE ST 377-2 (arbete pågår från och med januari 2012). KLV-kodad tilläggssyntax för MXF.
* SMPTE ST 378:2004 (arkiverad 2010). TV — Material Exchange Format (MXF) — Driftsmönster 1a (enkel artikel, enstaka paket)
* SMPTE ST 379-1:2009. Material Exchange Format (MXF) — MXF Generic Container
* SMPTE ST 379-2:2010. Material Exchange Format (MXF) -- MXF Constrained Generic Container
* SMPTE ST 380:2004. Television — Material Exchange Format (MXF) — Descriptive Metadata Scheme-1 (Standard, Dynamic)
* SMPTE ST 381-1:2005. Television — Material Exchange Format (MXF) — Mappa MPEG-strömmar till MXF Generic Container (Dynamisk)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) — Mappning av MPEG-strömmar till MXF Constrained Generic Container
* SMPTE ST 382:2007. Material Exchange Format (MXF) — Mappning av AES3-strömmar och Broadcast Wave Audio till MXF Generic Container
* SMPTE ST 383:2008. Television — Material Exchange Format (MXF) — Mappning av DV-DIF-data till MXF Generic Container
* SMPTE ST 384:2005. Television — Material Exchange Format (MXF) — Kartläggning av okomprimerade bilder i MXF Generic Container
* SMPTE ST 385:2004. Television — Material Exchange Format (MXF) — Kartläggning av SDTI-CP Essence och metadata i MXF Generic Container
* SMPTE ST 386:2004 (arkiverad 2010). Television — Material Exchange Format (MXF) — Mapping Type D-10 Essence Data till MXF Generic Container
* SMPTE ST 387:2004 (arkiverad 2010). Television — Material Exchange Format (MXF) — Mappa typ D-11 Essence Data till MXF Generic Container
* SMPTE ST 388:2004 (arkiverad 2010). Television — Material Exchange Format (MXF) — Mappning av A-law Coded Audio till MXF Generic Container
* SMPTE ST 389:2005. Television — Material Exchange Format (MXF) — MXF Generic Container Reverse Play System Element
* SMPTE ST 390:2011. Television — Material Exchange Format (MXF) — Specialiserat operativt mönster "Atom" (förenklad representation av ett enstaka föremål)
* SMPTE ST 391:2004 (arkiverad 2010). Television — Material Exchange Format (MXF) — Driftsmönster 1b (Enstaka objekt, sammansatta paket)
* SMPTE ST 392:2004. Television — Material Exchange Format (MXF) — Driftsmönster 2a (spellistobjekt, enstaka paket)
* SMPTE ST 393:2004. Television — Material Exchange Format (MXF) — Operationellt mönster 2b (spellistobjekt, sammansatta paket)
* SMPTE ST 394:2006. Television — Material Exchange Format (MXF) — Systemschema 1 för MXF Generic Container
* SMPTE ST 405:2006. Television — Material Exchange Format (MXF) — Element och individuella dataobjekt för MXF Generic Container System Scheme 1
* SMPTE ST 407:2006. Television — MXF — Driftsmönster 3a och 3b
* SMPTE ST 408:2006. Television — MXF — Operationsmönster 1c, 2c och 3c
* SMPTE ST 410: 2008. Materialutbytesformat - Generisk strömpartition.
* SMPTE ST 422:2006. Materialutbytesformat — Mappning av JPEG2000-kodströmmar till MXF Generic Container
* SMPTE ST 429.4:2006. D-Cinema Packaging — MXF JPEG 2000-applikation
* SMPTE ST 429.5:2006. D-Cinema Packaging — Tidsinställd textspårfil
* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption
* SMPTE ST 434:2006. Material Exchange Format — XML-kodning för metadata och filstrukturinformation
* SMPTE ST 436:2006. Television — MXF-mappningar för VBI-linjer och tilläggsdatapaket
* SMPTE ST 2019-4:2009. Mappning av VC-3-kodningsenheter till MXF Generic Container
* SMPTE ST 2037:2009. Mappning av VC-1 till MXF Generic Container
* SMPTE RP 2008:2008. Material Exchange Format — Mappa AVC-strömmar till MXF Generic Container
* SMPTE RP 2057:2011. Textbaserad metadatatransport i MXF
* SMPTE EG 41:2004. Material Exchange Format (MXF) — Teknisk riktlinje. Obs: Detta dokument var inte längre listat på SMPTEs webbplats när det konsulterades i januari 2012.
* SMPTE EG 42:2004. Material Exchange Format (MXF) — MXF Descriptive Metadata
* SMPTE RDD 3:2008. e-VTR MXF Interoperabilitetsspecifikation
* SMPTE RDD 9-2009. MXF-interoperabilitetsspecifikation för Sony MPEG Long GOP-produkter
* SMPTE-metadataregistrets kalkylbladsmeny.

### MXF strukturell metadata

Strukturell metadata är grundläggande i en MXF-fil eftersom den innehåller användbar information om innehållet i filen. MXF-metadata innehåller information som bildhastighet, bildstorlek, datum för filskapande och anpassat ändringsdatum. Den strukturella metadatan beskriver strukturen och kapaciteten hos en MXF-fil som inkluderar teknisk beskrivning av de olika väsentliga komponenterna och förmedlar hur utdatatidslinjen är sammansatt.

## Referenser

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Framstegsrapport](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [OpenSource C++ Library for MXF](http://www.freemxf.org/)

