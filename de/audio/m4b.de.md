{
  "date" : "2021-06-09",
  "keywords" :[ "m4b", "mp3", "Datei", "Erweiterung", "Format", "Was ist das m4b-Dateiformat", "Musik", "m4b-Dateiformat", "M4b vs. MP3", "Spezifikation des m4b-Dateiformats "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das M4B-Dateiformat und APIs, die M4B-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"M4B - MPEG-4 Hörbuchdateiformat",
  "linktitle" :"M4B",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Was ist eine M4B-Datei?
Die Datei mit der Erweiterung .m4b ist ein Hörbuch, das im Allgemeinen von Apple-Büchern und iTunes verwendet wird. Das in diesem Format verwendete Audio wird in MPEG-4 gespeichert und mithilfe der AAC-Codierung komprimiert. Eine M4B-Datei ist M4A sehr ähnlich, unterstützt jedoch die Hörbuch-bezogenen Funktionen wie Lesezeichen und Kapitelumbrüche. Die M4B-Dateien sind sowohl in DRM-fähigen als auch in DRM-freien Versionen verfügbar. DRM-verschlüsselte Hörbücher sind normalerweise kostenpflichtige Hörbücher aus dem iTunes Store. Dagegen kann DRM-frei leicht über das Internet gefunden werden.

## M4B-Dateiformat
Die Hörbuchdateien, die Metadaten, Bilder, Lesezeichen und Hyperlinks enthalten, können mit der Erweiterung .m4a gespeichert werden, aber im Allgemeinen wird beim Speichern die Erweiterung .m4b verwendet, nur um anzugeben, dass die Datei ein Hörbuch-Dateiformat hat. Fairplay DRM (Digital Rights Management) wird von apply verwendet, um seine M4B-Dateien zu schützen. Daher können die von iTunes heruntergeladenen Dateien nur auf autorisierten Geräten oder Computern abgespielt werden.


## M4B gegen M4A

Sowohl M4B als auch [MP3](https://docs.fileformat.com/audio/mp3/) sind reine Audiodateiformate.

**M4B**: Siegt im Vergleich zu MP3 qualitativ, wenn beide mit der gleichen Bitrate kodiert werden. M4B ist eine Hörbuchdatei, die mit AAC-Codierung komprimiert wird. Es ist im Grunde mit „MPEG-4 Audio Layer“ verbunden, Dateien mit der Erweiterung .m4b sind die Audioschicht von MPEG-4-Filmen, aber mit zusätzlichen Hörbuch-bezogenen Funktionen. Sein Ziel ist es, MP3 zu überholen und zum neuen Standard in der Audiokomprimierung zu werden. Es ist MP3 in vielerlei Hinsicht sehr ähnlich, wurde jedoch entwickelt, um eine bessere Qualität bei gleicher oder sogar kleinerer Dateigröße zu erzielen. Das M4B-Format wurde zuerst von Apple eingeführt. Der Formattyp wird auch als Apple Lossless Encoder (ALE) realisiert.

Daher konnte M4B derzeit nicht den Mainstream-Erfolg von MP3 erreichen, da das Audioformat noch nicht allgemein abspielbar ist.

**MP3**: Ein digitales Audioformat, das jedem gut bekannt ist. Ein allererstes Komprimierungsformat in der Szene und wurde unter Musikhörern sehr berühmt. Sein Mainstream-Erfolg ist so schnell, dass der Dateityp universell abgespielt werden kann und mit fast allem, Hardware oder Software, kompatibel ist. Im Allgemeinen erzeugt der M4A eine bessere Klangqualität, aber viele würden argumentieren, dass der Klangunterschied, ob es stimmt oder nicht, nicht vergleichbar ist und es Zeitverschwendung wäre, zu versuchen, MP3-Dateien in M4A-Dateien umzuwandeln. Schließlich führt die Konvertierung nur dazu, dass Sie die ursprüngliche Klangqualität verlieren.

## Spezifikation des M4B-Dateiformats

Ähnlich wie bei [M4A](/de/audio/m4a/) bestehen auch die M4B-Dateien aus aufeinanderfolgenden Chunks. Jeder Chunk hat einen 8-Byte-Header und ist wie folgt unterteilt:
- 4-Byte-Chunk-Größe (Big-Endian, High-Byte zuerst)
- 4-Byte-Chunk-Typ - eine der vordefinierten Signaturen: "ftyp", "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "ctab", „skip“, „jP2“, „wide“, „load“, „imap“, „matt“, „chap“, „kmat“, „clip“, „crgn“, „sync“, „tmcd“, „PICT ", "scpt", "ssrc".

Ähnlich wie bei M4A ist der erste Block in M4B vom Typ „ftype“ und hat einen Untertyp bei Offset 8. Der M4B wird durch den Untertyp definiert, der „M4B_“ sein muss.

Chunks iterieren, bis Chunks unbekannten Typs erkannt werden, es wird eine M4B-Datei (MPEG-4 Audio) erstellt.

## Verweise ##

* [MPEG-4 Teil 14 – von Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A, M4B, M4P) Format & Beispiel für Wiederherstellung](https://www.file-recovery.com/m4a-signature-format.htm)

