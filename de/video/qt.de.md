{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"QT-Dateiformat - Quick Movie-Datei",
  "keywords" :[ "QT", "QuickTime-Video", "qt-Format", "Wie man QT-Dateien abspielt", "Quick Movie File", "QTFF", "Video", "Apple" ],
  "description":"Erfahren Sie mehr über das QT-Dateiformat und APIs, die QT-Dateien erstellen und öffnen können.",
  "linktitle" : "QT",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Was ist eine QT-Datei?

Eine Datei mit der Erweiterung .qt ist eine Multimedia-Containerdatei, die vom QuickTime-Framework zum Speichern von Inhalten von Multimediadateien verwendet wird. Das von Apple Inc. entwickelte QuickTime File Format (QTFF) ist eine Multimedia-Containerdatei, die Audio, Video oder Text zur späteren Wiedergabe enthält. Es ist das bevorzugte Format für den Austausch digitaler Medien zwischen Geräten, Anwendungen und Betriebssystemen. QT-Dateien werden auch im [MOV](/de/video/mov/)-Format gespeichert, das ebenfalls von Apple Inc. entwickelt wurde. Zu den Anwendungen, die QT-Dateien öffnen können, gehören Apple QuickTime Player, VLC Media Player und Media Player Classic mit K- Lite-Codec-Paket.

## QT-Dateiformat

Das QTFF ist objektorientiert, das eine flexible Sammlung von Objekten zur einfachen Analyse und Erweiterung bereitstellt. Jeder Track in einer QT-Datei enthält einen digital codierten Medienstrom oder einen Datenverweis auf den Medienstrom, der sich in einer anderen Datei befindet. Die hierarchische Datenstruktur, die aus Objekten besteht, die als Atome bezeichnet werden, fungiert als Track-Container. Dateiformatspezifikationen für [QT-Dateiformat](https://developer.apple.com/documentation/quicktime-file-format) sind offiziell von Apple Inc als Referenz für Entwickler verfügbar.

### Medienbeschreibung

Die Medienbeschreibung einer QuickTime-Datei wird getrennt von den Mediendaten gespeichert. Informationen wie die Anzahl der Tracks, das Videokompressionsformat und Timing-Informationen werden in der Medienbeschreibung (auch bekannt als Filmressource, Filmatom oder einfach Film) gespeichert. In dieser Medienstruktur werden die Mediendaten durch einen Index referenziert. Bei den Mediendaten handelt es sich um die eigentlichen Beispieldaten, wie z. B. Videoeinzelbilder und Audiobeispiele, die im Film verwendet werden.

### Atome

Atom ist die Grundeinheit der QuickTime-Datei. Es gibt zwei Hauptfelder in jedem Atom vor jedem anderen Feld: Größen- und Typfelder. Das Größenfeld zeigt die Größe des Atoms, während das Typfeld den Datentyp angibt, der im Atom gespeichert ist. Von Natur aus sind Atome hierarchisch, was bedeutet, dass ein Atom andere Atome enthalten kann, die wiederum andere enthalten können. Das Layout eines Probenatoms ist im folgenden Bild dargestellt.

Jedes Atom hat zwei Teile, Header und Daten. Der Header enthält die Größen- und Typfelder und der Datenteil enthält die eigentlichen Daten. Außerdem wird jedes Feld unten erklärt:

#### Atomgröße

Header und Inhalt des Atoms werden durch eine 32-Bit-Ganzzahl angegeben, die als Atomgröße bekannt ist. Das Größenfeld enthält die Größe des Atoms in Byte, ausgedrückt als 32-Bit-Ganzzahl ohne Vorzeichen.

#### Atomtyp

Der Typ des Atoms wird auch durch eine 32-Bit-Ganzzahl angezeigt, die meistens als vierstelliges Feld mit knemonic Wert behandelt wird, wie z. B. „moov“ (0x6D6F6F76) für ein Filmatom oder „trak“ (0x7472616B) für ein Spuratom. Sobald der Atomtyp bekannt ist, können seine Daten interpretiert werden.

![alt text](../QT_Sample_Atom.png "QT File Format")

## Dateistruktur ##

QT/MOV-Dateien bestehen aus aufeinanderfolgenden Chunks. Jeder Chunk hat einen 8-Byte-Header: 4-Byte-Chunk-Größe (Big-Endian, High-Byte zuerst) und 4-Byte-Chunk-Typ – eine der vordefinierten Signaturen: „ftyp“, „mdat“, „moov“, „pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", „clip“, „crgn“, „sync“, „chap“, „tmcd“, „scpt“, „ssrc“, „PICT“. Der erste Chunk ist vom Typ „ftype“ und hat einen Untertyp bei Offset 8. MOV wird durch den Untertyp definiert, der „qt“ sein muss. Um eine MOV-Datei zu erstellen, müssen Chunks iteriert werden, bis ein unbekannter Typ erkannt wird.

Hier ist ein Musterbeispiel: Bei der Untersuchung der Binärdaten einer Muster-MOV-Datei ist ersichtlich, dass sie mit einer Signatur **ftyp** (Hex: 66 74 79 70) bei Offset 4 beginnt, die den QuickTime-Container-Dateityp definiert. Der Dateiuntertyp ist **qt~_~_** (hex: 71 74 20 20), was auf den MOV-Dateityp verweist. Die erste Blockgröße ist 32 (Hex: 00 00 00 20, Big-Endian, High Byte First), Größe liegt bei Offset 0. Bei Offset 32 (Hex: 20) liegt der zweite Chunk, der eine Größe von 8 und hat Geben Sie **mdat** (hex: 6D 64 61 74) ein.

Der nächste Chunk befindet sich bei Offset 32+8#40 (Hex: 28) und hat eine Größe von 3.263.028 (Hex: 00 31 CA 34) und Typ **mdat** (Hex: 6D 64 61 74) bei Offset 44 (Hex : 2C). Der nächste Chunk befindet sich bei Offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) und hat eine Größe von 21.189 (hex: 00 00 52 C5) und Typ **moov** (hex: 6D 6F 6F 76) bei Offset 1.836.019.574 (hex: 00 31 CA 60). Dies ist der letzte Block, also beträgt die Gesamtdateigröße 3.263.068 + 21.189 # 3.284.257 Bytes.

## Verweise ##

* [QT-Dateiformat – Apple Inc.](https://developer.apple.com/documentation/quicktime-file-format)
* [QuickTime-Dateiformat – Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)
