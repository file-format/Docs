{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MXF - Materialeudvekslingsformat",
  "keywords": [
"MXF",
"matroska video",
"mkv format",
"hvordan man afspiller MXF-filer",
"SMPTE",
"multimedie",
"video"
],
  "description": "Lær om MXF filformat og API'er, der kan oprette og åbne MXF filer.",
  "linktitle": "MXF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-mx-daf"
}
},
  "lastmod": "2021-03-01"
}

## Hvad er en MXF fil?

En fil med filtypenavnet .mxf er et multimediebeholderformat, der indeholder digitale video- og lydmedier sammen med metadataoplysninger om filen. Det følger SMPTE-standarden (Society of Motion Picture and Television Engineers), som er en global sammenslutning af fagfolk fra ingeniør-, teknologi- og ledere, der arbejder i medie- og underholdningsindustrien. MXF-filer kan konverteres til andre filformater såsom [AVI](/video/avi/) eller [MOV](/video/mov/).

## MXF filformat

MXF-filer er faktisk binære filer, der består af en sekvens af bytes i et bestemt format. Afkodningsapplikationer skal være i overensstemmelse med dette format for at forstå det og udtrække information fra det. Formatet tillader tilføjelse af nye elementer uden at bryde bagudkompatibiliteten ved hjælp af KLV-kodningen, som er beskrevet nedenfor.

 * Nøgle – elementets identifikator, en SMPTE Universal Label (UL)
 * Længde – længden af dataene, som er den variabel-længde-kodning, der bruges for at reducere mængden af plads, der kræves til dette element
 * Værdi – den faktiske værdi af elementet.

### SMPTE-formatspecifikationer

MXF-filformatet er blevet defineret af følgende SMPTE-specifikationer.

* SMPTE ST 377-1:2011. Fjernsyn — Material Exchange Format (MXF) — Filformatspecifikation

* SMPTE ST 377-2 (arbejde i gang fra januar 2012). KLV-kodet udvidelsessyntaks til MXF.

* SMPTE ST 378:2004 (Arkiveret 2010). Fjernsyn — Material Exchange Format (MXF) — Operationelt mønster 1a (enkelt element, enkelt pakke)

* SMPTE ST 379-1:2009. Material Exchange Format (MXF) — MXF Generic Container

* SMPTE ST 379-2:2010. Material Exchange Format (MXF) -- MXF Constrained Generic Container

* SMPTE ST 380:2004. Fjernsyn — Material Exchange Format (MXF) — Descriptive Metadata Scheme-1 (Standard, Dynamic)

* SMPTE ST 381-1:2005. Fjernsyn — Material Exchange Format (MXF) — Kortlægning af MPEG-streams i MXF Generic Container (Dynamisk)

* SMPTE ST 381-2:2011. Material Exchange Format (MXF) — Kortlægning af MPEG-streams ind i den MXF Constrained Generic Container

* SMPTE ST 382:2007. Material Exchange Format (MXF) — Kortlægning af AES3-streams og Broadcast Wave Audio til MXF Generic Container

* SMPTE ST 383:2008. Fjernsyn — Material Exchange Format (MXF) — Tilknytning af DV-DIF-data til den generiske MXF-beholder

* SMPTE ST 384:2005. Fjernsyn — Material Exchange Format (MXF) — Kortlægning af ukomprimerede billeder i den generiske MXF-beholder

* SMPTE ST 385:2004. Fjernsyn — Material Exchange Format (MXF) — Kortlægning af SDTI-CP-essens og metadata i den generiske MXF-beholder

* SMPTE ST 386:2004 (Arkiveret 2010). Fjernsyn — Material Exchange Format (MXF) — Mapping Type D-10 Essence Data til MXF Generic Container

* SMPTE ST 387:2004 (Arkiveret 2010). Fjernsyn — Material Exchange Format (MXF) — Mapping Type D-11 Essence Data til MXF Generic Container

* SMPTE ST 388:2004 (Arkiveret 2010). Fjernsyn — Material Exchange Format (MXF) — Kortlægning af A-law Coded Audio i MXF Generic Container

* SMPTE ST 389:2005. Fjernsyn — Material Exchange Format (MXF) — MXF Generisk Container Reverse Play System Element

* SMPTE ST 390:2011. Fjernsyn — Material Exchange Format (MXF) — Specialiseret operationelt mønster "Atom" (forenklet repræsentation af et enkelt element)

* SMPTE ST 391:2004 (Arkiveret 2010). Fjernsyn — Materialeudvekslingsformat (MXF) — Operationelt mønster 1b (enkelt vare, sammensatte pakker)

* SMPTE ST 392:2004. Fjernsyn — Materialeudvekslingsformat (MXF) — Operationelt mønster 2a (afspilningslisteelementer, enkelt pakke)

* SMPTE ST 393:2004. Fjernsyn — Materialeudvekslingsformat (MXF) — Operationelt mønster 2b (afspilningslisteelementer, grupperede pakker)

* SMPTE ST 394:2006. Fjernsyn — Material Exchange Format (MXF) — Systemskema 1 for MXF Generic Container

* SMPTE ST 405:2006. Fjernsyn — Material Exchange Format (MXF) — Elementer og individuelle dataelementer for MXF Generic Container System Scheme 1

* SMPTE ST 407:2006. Fjernsyn — MXF — Driftsmønstre 3a og 3b

* SMPTE ST 408:2006. Fjernsyn — MXF — Operationelle mønstre 1c, 2c og 3c

* SMPTE ST 410: 2008. Materialeudvekslingsformat - Generisk streampartition.

* SMPTE ST 422:2006. Materialeudvekslingsformat — Tilknytning af JPEG2000-kodestrømme til den generiske MXF-beholder

* SMPTE ST 429.4:2006. D-Cinema Packaging — MXF JPEG 2000-applikation

* SMPTE ST 429.5:2006. D-Cinema Packaging — Timed Text Track File

* SMPTE ST 429.6:2006. D-Cinema Packaging — MXF Track File Essence Encryption

* SMPTE ST 434:2006. Materialeudvekslingsformat — XML-kodning til metadata og filstrukturoplysninger

* SMPTE ST 436:2006. Fjernsyn — MXF-kortlægninger til VBI-linjer og tilhørende datapakker

* SMPTE ST 2019-4:2009. Kortlægning af VC-3-kodningsenheder i den generiske MXF-beholder

* SMPTE ST 2037:2009. Kortlægning af VC-1 til MXF Generic Container

* SMPTE RP 2008:2008. Materialeudvekslingsformat — Tilknytning af AVC-streams til den generiske MXF-beholder

* SMPTE RP 2057:2011. Tekstbaseret metadatatransport i MXF

* SMPTE EG 41:2004. Materialeudvekslingsformat (MXF) — Engineering Guideline. Bemærk: Dette dokument var ikke længere opført på SMPTE-webstedet, da det blev konsulteret i januar 2012.

* SMPTE EG 42:2004. Material Exchange Format (MXF) — MXF Descriptive Metadata

* SMPTE RDD 3:2008. e-VTR MXF Interoperabilitetsspecifikation

* SMPTE RDD 9-2009. MXF-interoperabilitetsspecifikation for Sony MPEG Long GOP-produkter

* SMPTE metadata registreringsdatabasen regneark menu.


### MXF strukturelle metadata

Strukturelle metadata er grundlæggende i en MXF-fil, da de indeholder nyttige oplysninger om indholdet af filen. MXF-metadata indeholder information såsom billedhastighed, billedstørrelse, filoprettelsesdato og tilpasset ændringsdato. De strukturelle metadata beskriver strukturen og mulighederne for en MXF-fil, der omfatter teknisk beskrivelse af de forskellige væsentlige komponenter og formidling af, hvordan output-tidslinjen er sammensat.

## Referencer

 * [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
 * [MXF - Progress Report](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
 * [OpenSource C++ Library for MXF](http://www.freemxf.org/)

