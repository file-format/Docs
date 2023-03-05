{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "Erweiterung", "Datei", "Dateiformat", "Datenbankdateityp", "Datenbankdateiformat", "Datenbankdateien" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das NSF-Dateiformat und APIs, die NSF-Dateien erstellen und öffnen können.",
  "title" :"NSF-Dateiformat - Lotus Notes-Datenbankformat",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Was ist eine NSF-Datei?

Eine Datei mit der Erweiterung .nsf (Notes Storage Facility) ist ein Datenbankdateiformat, das von der [IBM Notes-Software](https://en.wikipedia.org/wiki/HCL_Domino) verwendet wird, die früher als Lotus Notes bekannt war. Es definiert das Schema, um verschiedene Arten von Objekten wie E-Mails, Termine, Dokumente, Formulare und Ansichten zu speichern. Alle diese Informationen sind in einer einzigen NSF-Datei für die geschäftliche Zusammenarbeit ähnlich einer PST/OST-Datei enthalten. Zu den Anwendungen, die NSF-Dateien öffnen können, gehören IBM Lotus Notes und IBM Domino.

## NSF-Dateiformatspezifikationen

NSF-Dateien sind binärer Natur und ihre Spezifikationen sind von Joachim Metz auf [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database% verfügbar. 20file%20format.asciidoc). Gemäß diesen Angaben besteht eine NSF-Datei aus:

* Dateikopf
* Datenbank-Header

Außerdem besteht es aus:

* Superblock
* Bucket-Deskriptorblock
* Bitmap
* Relocation-Vektor-Bucket aufzeichnen
* Zusammenfassung Buckets
* Nicht zusammenfassende Buckets


### NSF-Datei-Header

Der Header der NSF-Datei ist 6 Byte groß. Es besteht aus:

|Offset|Größe|Wert|Beschreibung|
---|---|---|---|
0|2|0x1a 0x00|Signatur|
2|4| |Die Größe des Datenbank-Headers|

### Datenbank-Header

Der Header der NSD-Datenbank enthält die folgenden bestätigten Werte.

* Datenbankinformationen
* Datenbankkennung (DBID)
* Replikationsinformationen
* Pufferflags für Datenbankinformationen
* Titel
* Kategorien
* Klasse
* Designklasse (Vorlagenname)
* Spezielle Notenkennungen
* Polsterung
* Datenbankinformationen 2
* Datenbankinformationen 3
* Datenbankinformationen 4
* Datenbankinformationen 5
* Polsterung
* Kennung der Datenbankinstanz (DBIID)
* Replikationsverlauf

## Verweise

* [NSF-Format – Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

