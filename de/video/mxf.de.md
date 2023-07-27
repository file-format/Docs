{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Materialaustauschformat",
  "keywords" :[ "MXF", "Matroska-Video", "mkv-Format", "Wie man MXF-Dateien abspielt", "SMPTE", "Multimedia", "Video" ],
  "description":"Erfahren Sie mehr über das MXF-Dateiformat und APIs, die MXF-Dateien erstellen und öffnen können.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Was ist eine MXF-Datei?

Eine Datei mit der Erweiterung .mxf ist ein Multimedia-Containerformat, das digitale Video- und Audiomedien zusammen mit Metadateninformationen über die Datei enthält. Es folgt dem SMPTE-Standard (Society of Motion Picture and Television Engineers), einer globalen Vereinigung von Fachleuten aus Technik, Technologie und Führungskräften, die in der Medien- und Unterhaltungsbranche tätig sind. MXF-Dateien können in andere Dateiformate wie [AVI](/de/video/avi/) oder [MOV](/de/video/mov/) konvertiert werden.

## MXF-Dateiformat

MXF-Dateien sind eigentlich Binärdateien, die aus einer Folge von Bytes in einem bestimmten Format bestehen. Dekodierungsanwendungen müssen mit diesem Format kompatibel sein, um es zu verstehen und Informationen daraus zu extrahieren. Das Format ermöglicht das Hinzufügen neuer Elemente, ohne die Abwärtskompatibilität zu beeinträchtigen, indem die unten beschriebene KLV-Codierung verwendet wird.

* Key – die Kennung des Elements, ein SMPTE Universal Label (UL)
* Länge – die Länge der Daten, bei der es sich um die Codierung mit variabler Länge handelt, die verwendet wird, um den für dieses Element erforderlichen Speicherplatz zu reduzieren
* Wert – der tatsächliche Wert des Elements.

### SMPTE-Formatspezifikationen

Das MXF-Dateiformat wurde durch die folgenden SMPTE-Spezifikationen definiert.

* SMPTE-ST 377-1:2011. Fernsehen – Material Exchange Format (MXF) – Dateiformatspezifikation
* SMPTE ST 377-2 (in Arbeit seit Januar 2012). KLV-codierte Erweiterungssyntax für MXF.
* SMPTE ST 378:2004 (archiviert 2010). Fernsehen – Material Exchange Format (MXF) – Betriebsmuster 1a (Einzelartikel, Einzelpaket)
* SMPTE-ST 379-1:2009. Material Exchange Format (MXF) – generischer MXF-Container
* SMPTE ST 379-2:2010. Material Exchange Format (MXF) – MXF Constrained Generic Container
* SMPTE-ST 380:2004. Fernsehen – Material Exchange Format (MXF) – Beschreibendes Metadatenschema-1 (Standard, Dynamisch)
* SMPTE-ST 381-1:2005. Fernsehen – Material Exchange Format (MXF) – Zuordnen von MPEG-Streams zum generischen MXF-Container (dynamisch)
* SMPTE ST 381-2:2011. Material Exchange Format (MXF) – Mapping von MPEG-Streams in den MXF Constrained Generic Container
* SMPTE-ST 382:2007. Material Exchange Format (MXF) – Zuordnung von AES3-Streams und Broadcast-Wave-Audio zum generischen MXF-Container
* SMPTE-ST 383:2008. Fernsehen – Material Exchange Format (MXF) – Zuordnen von DV-DIF-Daten zum generischen MXF-Container
* SMPTE ST 384:2005. Fernsehen – Material Exchange Format (MXF) – Zuordnung von unkomprimierten Bildern in den generischen MXF-Container
* SMPTE ST 385:2004. Fernsehen – Material Exchange Format (MXF) – Zuordnen von SDTI-CP-Essenz und -Metadaten zum generischen MXF-Container
* SMPTE ST 386:2004 (archiviert 2010). Fernsehen – Material Exchange Format (MXF) – Zuordnung von Essenzdaten des Typs D-10 zum generischen MXF-Container
* SMPTE ST 387:2004 (archiviert 2010). Fernsehen – Material Exchange Format (MXF) – Zuordnung von Essenzdaten des Typs D-11 zum generischen MXF-Container
* SMPTE ST 388:2004 (archiviert 2010). Fernsehen – Material Exchange Format (MXF) – Zuordnen von A-law-codiertem Audio in den generischen MXF-Container
* SMPTE ST 389:2005. Fernsehen – Material Exchange Format (MXF) – Generisches MXF-Container-Reverse-Play-Systemelement
* SMPTE-ST 390:2011. Fernsehen – Material Exchange Format (MXF) – Spezialisiertes Betriebsmuster „Atom“ (vereinfachte Darstellung eines einzelnen Elements)
* SMPTE ST 391:2004 (archiviert 2010). Fernsehen – Material Exchange Format (MXF) – Betriebsmuster 1b (Einzelartikel, Sammelpakete)
* SMPTE-ST 392:2004. Fernsehen – Material Exchange Format (MXF) – Betriebsmuster 2a (Wiedergabelistenelemente, einzelnes Paket)
* SMPTE ST 393:2004. Fernsehen – Material Exchange Format (MXF) – Betriebsmuster 2b (Wiedergabelistenelemente, Sammelpakete)
* SMPTE ST 394:2006. Fernsehen – Material Exchange Format (MXF) – Systemschema 1 für den generischen MXF-Container
* SMPTE ST 405:2006. Fernsehen – Material Exchange Format (MXF) – Elemente und einzelne Datenelemente für das MXF Generic Container System Scheme 1
* SMPTE ST 407:2006. Fernsehen – MXF – Betriebsmuster 3a und 3b
* SMPTE ST 408:2006. Fernsehen – MXF – Betriebsmuster 1c, 2c und 3c
* SMPTE ST 410: 2008. Materialaustauschformat – Generische Stream-Partition.
* SMPTE ST 422:2006. Material Exchange Format – Zuordnung von JPEG2000-Codestreams zum generischen MXF-Container
* SMPTE ST 429.4:2006. D-Cinema Packaging – MXF JPEG 2000-Anwendung
* SMPTE ST 429.5:2006. D-Cinema-Verpackung – Zeitgesteuerte Textspurdatei
* SMPTE-ST 429.6:2006. D-Cinema Packaging – MXF Track File Essence-Verschlüsselung
* SMPTE ST 434:2006. Material Exchange Format – XML-Kodierung für Metadaten und Dateistrukturinformationen
* SMPTE ST 436:2006. Fernsehen – MXF-Mappings für VBI-Leitungen und zusätzliche Datenpakete
* SMPTE-ST 2019-4:2009. Zuordnung von VC-3-Codierungseinheiten zum generischen MXF-Container
* SMPTEST 2037:2009. Zuordnung von VC-1 zum generischen MXF-Container
* SMPTE-RP 2008:2008. Materialaustauschformat – Zuordnen von AVC-Streams zum generischen MXF-Container
* SMPTE-RP 2057:2011. Textbasierter Metadatentransport in MXF
* SMPTE EG 41:2004. Material Exchange Format (MXF) – Engineering Guideline. Hinweis: Dieses Dokument war zum Zeitpunkt der Abfrage im Januar 2012 nicht mehr auf der SMPTE-Website aufgeführt.
* SMPTE EG 42:2004. Material Exchange Format (MXF) – Beschreibende MXF-Metadaten
* SMPTE-RDD 3:2008. e-VTR MXF-Interoperabilitätsspezifikation
* SMPTE-RDD 9-2009. MXF-Interoperabilitätsspezifikation von Sony MPEG Long GOP-Produkten
* Tabellenkalkulationsmenü für die SMPTE-Metadatenregistrierung.

### Strukturelle MXF-Metadaten

Strukturelle Metadaten sind in einer MXF-Datei von grundlegender Bedeutung, da sie nützliche Informationen über den Inhalt der Datei enthalten. MXF-Metadaten enthalten Informationen wie Bildrate, Bildgröße, Dateierstellungsdatum und benutzerdefiniertes Änderungsdatum. Die strukturellen Metadaten beschreiben die Struktur und die Fähigkeiten einer MXF-Datei, die die technische Beschreibung der verschiedenen wesentlichen Komponenten und die Vermittlung der Zusammensetzung der Ausgabezeitachse umfasst.

## Verweise

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Fortschrittsbericht](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [OpenSource C++ Bibliothek für MXF](http://www.freemxf.org/)

