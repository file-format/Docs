{
  "date" : "2021-08-31",
  "keywords" :[ "xbe-Datei", "xbe-Dateiformat", "was ist eine xbe-Datei", "Datei", "xbe-Beispiel", "xbe-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das XBE-Dateiformat und APIs, die XBE-Dateien erstellen und öffnen können.",
  "title" :"XBE - iOS-Anwendungspaketdatei",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Was ist eine XBE-Datei?
Eine Datei mit der Erweiterung .xbe ist eine ausführbare Anwendung von einer Xbox-Videospiel-Disc. Die XBE-Dateien sind die Hauptdateien, die im Xbox-System ausgeführt werden und normalerweise nicht auf einem Computer geöffnet werden sollen, aber sie können auf einem PC mit einem Xbox-Emulationsprogramm geöffnet werden. Diese Dateien werden normalerweise von Spieleentwicklern erstellt und dann von Microsoft signiert. Die Dateistruktur ähnelt den Windows PE-Dateien, aber einige wichtige Änderungen gemäß den XBox-Einstellungen werden angewendet, um sie auf XBox lauffähig zu machen.

## XBE-Dateiformat
Die XBE-Datei besteht aus einem Bildheader, einer Sammlung von Abschnittsheadern, einem Zertifikat, lokalen Threadspeicherdaten, einer Sammlung von Bibliotheksversionen, Microsoft-Bitmap und den Abschnitten, die den Code und die Ressourcen enthalten.

### Bildkopfzeile
Der Image-Header enthält die Informationen, die erklären, wo sich die anderen Komponenten der ausführbaren Datei in der Datei befinden und wie die ausführbare Datei behandelt und geladen werden sollte.

### TLS-Tabelle
Die TLS-Tabelle besteht aus allen Informationen, die von der XBE benötigt werden, um den Thread-lokalen Speicher ordnungsgemäß einzurichten. Es ist im Grunde einzigartig für das in PE32-Dateien gefundene TLS-Verzeichnis und kann direkt von dort kopiert werden. Diese Tabelle kann weggelassen werden, wenn die XBE-Datei keinen Thread-lokalen Speicher verwendet und das entsprechende Feld im Bildheader auf Null gesetzt ist.

| Versatz | Größe | Name | Beschreibung |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Rohdaten Start | Absolute (dh keine RVA) Startadresse der TLS-Variablendaten im Programmabbild. |
| 0x0004 | 0x0004 | Rohdaten Ende | Absolute (dh keine RVA) Adresse des Endes der TLS-Variablendaten im Programmabbild. |
| 0x0008 | 0x0004 | Adresse des Index | Absolute (dh keine RVA) Adresse der TLS-Indexvariablen. |
| 0x000C | 0x0004 | Rückrufadresse | Absolute (dh keine RVA) Adresse der nullterminierten TLS-Callback-Funktionstabelle. |
| 0x0010 | 0x0004 | Größe der Nullfüllung | Die Anzahl der Bytes nach den Rohdaten, die im Speicher auf Null gesetzt werden sollen. |
| 0x0014 | 0x0004 | Eigenschaften | Beschreibt die Ausrichtung. |

### Zertifikat

Für jede ausführbare Xbox-Datei, die Informationen zu den Titeln enthält, ist ein Zertifikat erforderlich:
 


- Uhrzeit und Datum, an dem das Zertifikat erstellt wurde
- Titel-ID
- Titel
- Alternative Titel-IDs
- Zulässige Medientypen, von denen die ausführbare Datei ausgeführt werden kann (HD, DVD, CD usw.)
- Spielregion
- Spielbewertungen
- Datenträgernummer
- Ausführung
- LAN-Schlüssel-Rohdaten, die für System Link verwendet werden
- Signaturschlüssel-Rohdaten (zum Signieren von Spielständen)
- Alternative Signaturschlüssel
- Originalgröße des Zertifikats
- Name des Onlinedienstes (in frühen ausführbaren Dateien nicht vorhanden)
- Laufzeit-Sicherheits-Flags (in frühen ausführbaren Dateien nicht vorhanden)
 


### Zulässige Medientypen
Medientypen, die von der ausführbaren Datei ausgeführt werden dürfen. Folgende Werte sind bekannt:
| Medientyp | Wert |
---------------------|------------|
| FESTPLATTE | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIEN_MASKE | 0x00FFFFFF |

### Abschnitte
Die Abschnitte werden durch die Abschnittsüberschriften ausgedrückt. Die Abschnittsüberschriften beginnen direkt nach dem Zertifikat und enthalten Informationen darüber, wo in der Datei die eigentlichen Abschnitte vorhanden sind. In einer ausführbaren Xbox-Datei sind immer mindestens zwei Abschnitte vorhanden:


- .text


- .rDaten


## Verweise



* [Xbe - ausführbare XBox-Datei](https://xboxdevwiki.net/Xbe)


