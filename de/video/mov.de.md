{
  "date" : "2019-10-11",
  "keywords" :[ "mov-Datei", "mov-Dateiformat", "was ist eine mov-Datei", "Datei", "mov-Beispiel", "mov-Dateierweiterung", "Erweiterung", "Format", "QuickTime", "MPEG- 4" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MOV-Datei - Apple QuickTime-Filmdateiformat",
  "description":"Erfahren Sie mehr über das MOV-Dateiformat und APIs, die MOV-Dateien erstellen und öffnen können.",
  "linktitle" :"MOV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-29"
}

## Was ist eine MOV-Datei?

Eine MOV-Datei ist ein von Apple Inc. entwickelter Videodateityp, der einen oder mehrere Tracks enthält. Jede Spur speichert einen Film, Audio, Filmclips und Untertitel. Es ist ein Multimedia-Container, der verschiedene Arten von Medienelementen speichern kann. Das MOV-Videoformat ist sowohl mit Windows- als auch mit Macintosh-Systemen kompatibel. Es verwendet MPEG-4-codiert für die Komprimierung, und Spuren werden in Objekten verwaltet, die als Atome bezeichnet werden und in einer hierarchischen Datenstruktur angeordnet sind.

## Kurze Geschichte des MOV-Dateiformats

Das MPEG-4-Dateiformat hat sich aus der Spezifikation des QuickTime-Dateiformats (**QTFF**) im Jahr 2001 entwickelt. Die Internationale Organisation für Normung hat das Format genehmigt und die Systemspezifikationen MPEG-4 Teil 1 wurden 1999 veröffentlicht. 2001 wurde eine Revisionsdatei veröffentlicht Format [MP4](/de/video/mp4/) wurde veröffentlicht.

Die erste Version von MP4 wurde 2003 als MPEG-4 Part 14 (ISO/IEC 14496-14:2003) überarbeitet. Im Jahr 2004 wurde MP4 verallgemeinert, um eine allgemeine Struktur für alle zeitbasierten Mediendateien zu definieren. Daher wird es jetzt als Grundlage für verschiedene andere Multimedia-Dateiformate verwendet.

## QuickTime-Dateiformat (QTFF) – Weitere Informationen

Um mit digitalem Multimedia zu arbeiten, kann QTFF viele Arten von Daten enthalten. Es ist ein Ideenformat für den Austausch digitaler Medien, da das Format die Standards für die Beschreibung jeglicher Art von Medienstrukturen definiert. Das Dateiformat besteht aus einer flexiblen Sammlung objektorientierter Objekte. Für die Speicherung von Filmen auf Disketten verwendet QuickTime zwei Strukturen, nämlich „Atome“ und „QT-Atome“.

### Atome

Atom ist die Grundeinheit der QuickTime-Datei. Es gibt zwei Hauptfelder in jedem Atom vor jedem anderen Feld: Größen- und Typfelder. Das Größenfeld zeigt die Größe des Atoms, während das Typfeld den Datentyp angibt, der im Atom gespeichert ist. Von Natur aus sind Atome hierarchisch, was bedeutet, dass ein Atom andere Atome enthalten kann, die wiederum andere enthalten können. Das Layout eines Probenatoms ist im folgenden Bild dargestellt.

Jedes Atom hat zwei Teile, „Header“ und „Data“. Der Header enthält die Größen- und Typfelder und der Datenteil enthält die eigentlichen Daten. Außerdem wird jedes Feld unten erklärt:

### Atomgröße

Header und Inhalt des Atoms werden durch eine 32-Bit-Ganzzahl angegeben, die als Atomgröße bekannt ist. Das Größenfeld enthält die Größe des Atoms in Byte, ausgedrückt als 32-Bit-Ganzzahl ohne Vorzeichen.

### Atomtyp

Der Typ des Atoms wird auch durch eine 32-Bit-Ganzzahl angezeigt, die meistens als vierstelliges Feld mit knemonic Wert behandelt wird, wie z. B. „moov“ (0x6D6F6F76) für ein Filmatom oder „trak“ (0x7472616B) für ein Spuratom. Sobald der Atomtyp bekannt ist, können seine Daten interpretiert werden.

### QT-Atome und Atom-Container

QT-Atome bieten ein universelles Speicherformat und verfügen über einen erweiterten Header, der aus den Feldern Size, Type, Atom ID und Count of Child Atoms besteht. QT-Atome werden in einen Atom-Container gepackt, eine eindeutige Datenstruktur mit einem Header mit einer Lock-Zählung. In jedem Atomcontainer gibt es ein Wurzelatom, das das QT-Atom ist. Das Layout des QT-Atoms ist in der folgenden Abbildung dargestellt.

Der Header des QT-Atom-Containers enthält die folgenden Daten:

Reserviert: Ein 10-Byte-Element mit dem Wert 0.

Lock Count: 16-Bit-Ganzzahl mit dem Wert 0.

QT-Atom-Header haben die folgenden Daten:

**Größe -** QT-Atom-Header und -Inhalt werden in Bytes durch eine 32-Bit-Ganzzahl angegeben. Im Falle eines Blattatoms enthält dieses Feld dann die Größe eines einzelnen Atoms.

**Typ -** Der Atomtyp wird durch eine 32-Bit-Ganzzahl angegeben. Falls es sich um das Wurzelatom handelt, wird der Wert auf „sean“ gesetzt.

**Atom-ID -** Dies ist eine 32-Bit-Ganzzahl, die die Atom-ID anzeigt und für alle Geschwister eindeutig sein muss. Wurzelatom hat immer den Wert der Atom-ID als 1.

**Reserviert -** Eine 16-Bit-Ganzzahl, die auf 0 gesetzt werden muss.

**Child count -** Eine 16-Bit-Ganzzahl, die die Anzahl der untergeordneten Atome eines Atoms angibt.

**Reserviert -** Eine 32-Bit-Ganzzahl, die auf 0 gesetzt werden muss.

## Dateistruktur von MOV-Dateien

MOV-Dateien bestehen aus aufeinanderfolgenden Chunks. Jeder Chunk hat einen 8-Byte-Header: 4-Byte-Chunk-Größe (Big-Endian, High-Byte zuerst) und 4-Byte-Chunk-Typ – eine der vordefinierten Signaturen: „ftyp“, „mdat“, „moov“, „pnot ", "udta", "uuid", "moof", "free", "skip", "jP2", "wide", "load", "ctab", "imap", "matt", "kmat", „clip“, „crgn“, „sync“, „chap“, „tmcd“, „scpt“, „ssrc“, „PICT“. Der erste Chunk ist vom Typ „ftype“ und hat einen Untertyp bei Offset 8. MOV wird durch den Untertyp definiert, der „qt“ sein muss. Um eine MOV-Datei zu erstellen, müssen Chunks iteriert werden, bis ein unbekannter Typ erkannt wird.

Hier ist ein `Beispielbeispiel`: Beim Betrachten der Binärdaten einer Beispiel-MOV-Datei ist ersichtlich, dass sie mit einer Signatur **ftyp** (Hex: 66 74 79 70) bei Offset 4 beginnt, die den QuickTime-Container-Dateityp definiert. Der Dateiuntertyp ist **qt~_~_** (hex: 71 74 20 20), was auf den MOV-Dateityp verweist. Die erste Blockgröße ist 32 (Hex: 00 00 00 20, Big-Endian, High Byte First), Größe liegt bei Offset 0. Bei Offset 32 (Hex: 20) liegt der zweite Chunk, der eine Größe von 8 und hat Geben Sie **mdat** (hex: 6D 64 61 74) ein.

Der nächste Chunk befindet sich bei Offset 32+8#40 (Hex: 28) und hat eine Größe von 3.263.028 (Hex: 00 31 CA 34) und Typ **mdat** (Hex: 6D 64 61 74) bei Offset 44 (Hex : 2C). Der nächste Chunk befindet sich bei Offset 40 + 3.263.028#3.263.068 (hex: 00 31 CA 5C) und hat eine Größe von 21.189 (hex: 00 00 52 C5) und Typ **moov** (hex: 6D 6F 6F 76) bei Offset 1.836.019.574 (hex: 00 31 CA 60). Dies ist der letzte Block, also beträgt die Gesamtdateigröße 3.263.068 + 21.189 # 3.284.257 Bytes.

## Wie konvertiere ich MOV-Dateien?

Es gibt viele Mediaplayer und Software-Videoeditoren, um MOV-Dateien in andere gängige Videodateiformate zu konvertieren. Zu den Mediaplayern, die MOV-Dateien in andere Formate konvertieren können, gehören:

* VideoLAN VLC-Mediaplayer
* Eltima Elmedia-Player

Mehrere Mediaplayer und Videoeditoren, einschließlich VideoLAN VLC Mediaplayer und Eltima Elmedia Player, können MOV-Dateien in andere Formate konvertieren. Diese Software kann MOV-Dateien in folgende Videoformate konvertieren.

* MPEG-4-Video - [MP4](/de/video/mp4/)
* WebM-Video - [WEBM](/de/video/webm/)
* Videotransportstrom - [TS](/de/video/ts/)
* Fortgeschrittenes Systemformat - [ASF](/de/video/ts/)
* Ogg-Vorbis-Audio - [OGG](/de/audio/ogg/)
* MP3-Audio - [MP3](/de/audio/mp3/)
* Kostenloser verlustfreier Audio-Codec - [FLAC](/de/audio/flac/)
* WAVE-Audio - [WAV](/de/audio/wav/)

## Open-Source-API für MOV-Dateien

* [React Native API zum Konvertieren von MOV in MP4](https://github.com/taltultc/react-native-mov-to-mp4)
* [Python-API zum Reparieren von MOV-Dateien](https://github.com/nrosenstein-stuff/movrepair)
* [Ruby-API zum Konvertieren von MOV in GIF](https://github.com/skygroundmedia/convert-mov-to-gif)

## Verweise

* [https://en.wikipedia.org/wiki/QuickTime_File_Format](https://en.wikipedia.org/wiki/QuickTime_File_Format)

