{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Materiaaluitwisselingsformaat",
  "keywords" :[ "MXF", "matroska video", "mkv-formaat", "hoe MXF-bestanden af te spelen", "SMPTE", "multimedia", "video"],
  "description":"Meer informatie over MXF-bestandsindelingen en API's die MXF-bestanden kunnen maken en openen.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Wat is een MXF-bestand?

Een bestand met de extensie .mxf is een multimediacontainerformaat dat digitale video- en audiomedia bevat, samen met metadata-informatie over het bestand. Het volgt de SMPTE-standaard (Society of Motion Picture and Television Engineers), een wereldwijde vereniging van professionals uit de techniek, technologie en leidinggevenden die werkzaam zijn in de media- en entertainmentindustrie. MXF-bestanden kunnen worden geconverteerd naar andere bestandsindelingen zoals [AVI](/nl/video/avi/) of [MOV](/nl/video/mov/).

## MXF-bestandsindeling

MXF-bestanden zijn in feite binaire bestanden die bestaan uit een reeks bytes in een bepaald formaat. Decodeertoepassingen moeten aan dit formaat voldoen om het te begrijpen en er informatie uit te halen. Het formaat maakt het mogelijk nieuwe items toe te voegen zonder achterwaartse compatibiliteit te verbreken met behulp van de KLV-codering die hieronder wordt beschreven.

* Sleutel – de identifier van het element, een SMPTE Universal Label (UL)
* Lengte - de lengte van de gegevens, de codering met variabele lengte die wordt gebruikt om de hoeveelheid ruimte die nodig is voor dit item te verminderen
* Waarde – de werkelijke waarde van het element.

### SMPTE-formaatspecificaties

Het MXF-bestandsformaat is gedefinieerd door de volgende SMPTE-specificaties.

* SMPTE ST 377-1:2011. Televisie — Material Exchange Format (MXF) — Specificatie bestandsindeling
* SMPTE ST 377-2 (werk in uitvoering vanaf januari 2012). KLV-gecodeerde extensiesyntaxis voor MXF.
* SMPTE ST 378:2004 (gearchiveerd 2010). Televisie — Material Exchange Format (MXF) — Operationeel patroon 1a (één artikel, één pakket)
* SMPTE ST 379-1:2009. Materiaaluitwisselingsformaat (MXF) — MXF Generieke container
* SMPTE ST 379-2:2010. Materiaaluitwisselingsindeling (MXF) -- MXF-beperkte generieke container
* SMPTE ST 380:2004. Televisie — Material Exchange Format (MXF) — Beschrijvend Metadata Schema-1 (Standaard, Dynamisch)
* SMPTE ST 381-1:2005. Televisie — Material Exchange Format (MXF) — MPEG-streams in kaart brengen in de MXF Generic Container (Dynamic)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) — MPEG-streams in kaart brengen in de MXF-beperkte generieke container
* SMPTE ST 382:2007. Material Exchange Format (MXF) — AES3-streams en Broadcast Wave-audio toewijzen aan de MXF Generic Container
* SMPTE ST 383:2008. Televisie — Material Exchange Format (MXF) — DV-DIF-gegevens toewijzen aan de MXF-generieke container
* SMPTE ST 384:2005. Televisie — Material Exchange Format (MXF) — Mapping van niet-gecomprimeerde afbeeldingen in de MXF Generic Container
* SMPTE ST 385:2004. Televisie — Material Exchange Format (MXF) — SDTI-CP Essence en Metadata in kaart brengen in de MXF Generic Container
* SMPTE ST 386:2004 (gearchiveerd 2010). Televisie — Material Exchange Format (MXF) — Toewijzing van type D-10 Essence-gegevens naar de MXF Generieke container
* SMPTE ST 387:2004 (gearchiveerd 2010). Televisie — Material Exchange Format (MXF) — Mapping Type D-11 Essence Data to the MXF Generic Container
* SMPTE ST 388:2004 (gearchiveerd 2010). Televisie — Material Exchange Format (MXF) — A-law gecodeerde audio toewijzen aan de MXF Generic Container
* SMPTE ST 389:2005. Televisie — Material Exchange Format (MXF) — MXF Generic Container Reverse Play System Element
* SMPTE ST 390:2011. Televisie — Material Exchange Format (MXF) — Gespecialiseerd operationeel patroon "Atom" (vereenvoudigde weergave van een enkel item)
* SMPTE ST 391:2004 (gearchiveerd 2010). Televisie — Material Exchange Format (MXF) — Operationeel patroon 1b (enkel artikel, gecombineerde pakketten)
* SMPTE ST 392:2004. Televisie — Material Exchange Format (MXF) — Operationeel patroon 2a (Play-List Items, Single Package)
* SMPTE ST 393:2004. Televisie — Material Exchange Format (MXF) — Operationeel patroon 2b (Play-List Items, Ganged Packages)
* SMPTE ST 394:2006. Televisie — Material Exchange Format (MXF) — Systeemschema 1 voor de MXF Generic Container
* SMPTE ST 405:2006. Televisie — Material Exchange Format (MXF) — Elementen en individuele gegevensitems voor het MXF Generic Container System Scheme 1
* SMPTE ST 407:2006. Televisie — MXF — Operationele patronen 3a en 3b
* SMPTE ST 408:2006. Televisie — MXF — Operationele patronen 1c, 2c en 3c
* SMPTE ST 410: 2008. Materiaaluitwisselingsformaat - generieke stroompartitie.
* SMPTE ST 422:2006. Materiaaluitwisselingsindeling — JPEG2000-codestromen toewijzen aan de MXF-generieke container
* SMPTE ST 429,4:2006. D-Cinema-verpakking — MXF JPEG 2000-toepassing
* SMPTE ST 429.5:2006. D-Cinema Packaging — Getimed teksttrackbestand
* SMPTE ST 429.6:2006. D-Cinema-verpakking — MXF Track File Essence-codering
* SMPTE ST 434:2006. Materiaaluitwisselingsformaat — XML-codering voor metagegevens en bestandsstructuurinformatie
* SMPTE ST 436:2006. Televisie — MXF-toewijzingen voor VBI-lijnen en aanvullende gegevenspakketten
* SMPTE ST 2019-4:2009. VC-3 codeereenheden toewijzen aan de MXF generieke container
* SMPTE ST 2037:2009. VC-1 toewijzen aan de MXF Generic Container
* SMPTE RP 2008:2008. Indeling materiaaluitwisseling — AVC-streams in kaart brengen in de MXF-generieke container
* SMPTE RP 2057:2011. Op tekst gebaseerd vervoer van metagegevens in MXF
* SMPTE EG 41:2004. Material Exchange Format (MXF) — Technische richtlijn. Opmerking: dit document stond niet langer op de SMPTE-website toen het in januari 2012 werd geraadpleegd.
* SMPTE EG 42:2004. Materiaaluitwisselingsformaat (MXF) — MXF Beschrijvende Metadata
* SMPTE RDD 3:2008. e-VTR MXF-interoperabiliteitsspecificatie
* SMPTE RDD 9-2009. MXF-interoperabiliteitsspecificatie van Sony MPEG Long GOP-producten
* SMPTE metadata register spreadsheet menu.

### MXF structurele metadata

Structurele metadata is van fundamenteel belang in een MXF-bestand omdat het nuttige informatie over de inhoud van het bestand bevat. MXF-metagegevens bevatten informatie zoals framesnelheid, framegrootte, aanmaakdatum van het bestand en aangepaste wijzigingsdatum. De structurele metadata beschrijven de structuur en mogelijkheden van een MXF-bestand dat een technische beschrijving van de verschillende essentiële componenten omvat en aangeeft hoe de outputtijdlijn is samengesteld.

## Referenties

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Voortgangsrapport](http://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [OpenSource C++-bibliotheek voor MXF](http://www.freemxf.org/)

