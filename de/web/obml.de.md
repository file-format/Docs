{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML-Dateiformat - Gespeicherte Opera Mini-Webseitendatei",
  "description" :"Erfahren Sie, was eine OBML-Datei und APIs sind, die OBML-Dateien erstellen und öffnen können.",
  "linktitle" :"OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Was ist eine OBML-Datei?

Eine OBML-Datei (Opera Binary Markup Language) ist eine Offline-Version einer Webseite, die vom mobilen Webbrowser Opera Mini gespeichert wird. Es handelt sich um eine eigenständige, kompakte Version der [HTML](/de/web/html/)-Dateien, die alle Elemente der Seite enthält, die auf bestimmten Geräten offline angezeigt werden können. Das OBML-Dateiformat wurde auf mehrere Versionen aktualisiert, wobei OBML15 und OBML16 allgemein verwendet werden. Ein wichtiger Punkt, den es zu beachten gilt, ist, dass jede Opera Mini-Version nur mit einem OBML-Format kompatibel ist. Daher werden beim Upgrade von Opera Mini zuvor gespeicherte Seiten lesbar bleiben. OBML-Dateien können in HTML und [PDF](/de/pdf/) konvertiert werden.

## OBML-Dateiformat

Das OBML-Dateiformat wird im proprietären Dateiformat von Opera gespeichert und seine Dateiformatspezifikationen sind nicht öffentlich verfügbar. Das [OMBL-Format] (https://github.com/grawity/obml-parser/blob/master/obml.md) wurde jedoch zurückentwickelt, um seine Struktur wie folgt zu decodieren.

### OBML-Datentypen

Gemäß den Ergebnissen des Reverse Engineering verwendet OBML die folgenden primitiven Typen:

* `byte` – Ganzzahl ohne Vorzeichen (1 Byte)
* „short“ – Ganzzahl mit Vorzeichen (2 Bytes, Big-Endian)
* „medium“ – vorzeichenbehaftete Ganzzahl (3 Bytes, Big-Endian)
 * `blob` – { length: short, data: byte[length] }
* „char“ – ein Byte, das ein ASCII-Zeichen enthält
* „string“ – ein Blob mit UTF-8-codiertem Text

### OBML-Header

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Verweise

* [OMBL-Format](https://github.com/grawity/obml-parser/blob/master/obml.md)

