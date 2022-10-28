{
  "date" : "2021-04-26",
  "keywords" :[ "m4a", "mp3", "Datei", "Erweiterung", "Format", "was ist das m4a-Dateiformat", "Musik", "m4a-Dateiformat", "M4A vs. MP3", "Spezifikation des m4a-Dateiformats "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das M4A-Dateiformat und APIs, die M4A-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"M4A - MPEG-4-Audiodatei",
  "linktitle" : "M4A",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-04-26"
}

## Was ist eine M4A-Datei?
Das **M4A-Dateiformat** ist eine Audiodatei, die mit AAC (Advanced Audio Coding) erstellt wurde, was als verlustbehaftete Komprimierung bekannt ist. Das Wort M4A wird als MPEG 4 Audio abgekürzt. Diese Audiodateien haben normalerweise die Dateierweiterung .m4a. Dies gilt insbesondere für ungeschützte Inhalte. Es kann verschiedene Arten von Audioinhalten wie Hörbücher, Lieder und Podcasts speichern. M4A wird normalerweise als fortgeschritteneres Format als MP3 realisiert, das normalerweise nicht nur für Audio entwickelt wurde. Es ist nur eine Audioschicht in MPEG 1- oder 2-Videodateien. Das M4A-Format wird von FairPlay Digital Rights Management verschlüsselt, da es über den iTunes Store verkauft wurde, verwenden Sie die Erweiterung .m4p. Die Apple iPhones verwenden MPEG-4-Audio für ihre Klingeltöne, aber diese Audiodateien verwenden die Erweiterung .m4r.


## M4A gegen MP3

Sowohl M4A als auch [MP3](https://docs.fileformat.com/audio/mp3/) sind reine Audiodateiformate.

**M4A**: Besser als MP3 in Bezug auf Qualität und Größe, wenn es mit der gleichen Bitrate codiert wird. Die Dateierweiterung .m4a ist so verbreitet, weil sie von Apple für die Verwendung im iTunes Music Store verwendet wurde. M4A ist eine Audiodatei, die mit der MPEG-4-Technologie komprimiert wurde; ein Algorithmus für verlustbehaftete Komprimierung. Es ist im Grunde mit „MPEG-4 Audio Layer“ verbunden, Dateien mit der Erweiterung .m4a sind die Audioschicht von MPEG-4-Filmen. Es soll MP3 überholen und zum neuen Standard in der Audiokomprimierung werden. Es ist MP3 in vielerlei Hinsicht sehr ähnlich, wurde jedoch eingeführt, um eine bessere Qualität bei gleicher oder sogar kleinerer Dateigröße zu erzielen. Das M4A-Format wurde zuerst von Apple eingeführt. Der Formattyp wird auch als Apple Lossless Encoder (ALE) realisiert.

Daher kann das M4A derzeit nicht den Mainstream-Erfolg des MP3 erreichen, da das Audioformat noch nicht allgemein abspielbar ist. Es ist irgendwie nur auf MacOS, iPod und andere Apple-Produkte beschränkt.

**MP3**: Das bekannteste digitale Audioformat. Es war auch eines der ersten Kompressionsformate in der Szene und wurde bei Musikliebhabern sehr beliebt. Sein Mainstream-Erfolg ist so schnell, dass der Dateityp universell und mit fast allem, Hardware oder Software, abgespielt werden kann. Im Allgemeinen erzeugt der M4A eine bessere Klangqualität, aber viele würden argumentieren, dass der Klangunterschied, ob wahr oder nicht, nicht unterscheidbar ist und es Zeitverschwendung wäre, zu versuchen, MP3-Dateien in M4A-Dateien umzuwandeln. Letztendlich führt die Konvertierung nur dazu, dass Sie die ursprüngliche Klangqualität verlieren.

## Spezifikation des M4A-Dateiformats

Die M4A-Dateien bestehen aus aufeinanderfolgenden Chunks. Jeder Chunk hat einen 8-Byte-Header und ist wie folgt unterteilt:
- 4-Byte-Chunk-Größe (Big-Endian, High-Byte zuerst)
- 4-Byte-Chunk-Typ - eine der vordefinierten Signaturen: "ftyp", "mdat", "moov", "pnot", "udta", "uuid", "moof", "free", "skip", „jP2“, „wide“, „load“, „ctab“, „imap“, „matt“, „kmat“, „clip“, „crgn“, „sync“, „chap“, „tmcd“, „scpt ", "ssrc", "PICT".

Der erste Chunk wird vom Typ „ftype“ sein und hat einen Untertyp bei Offset 8. Der M4A definiert durch den Untertyp, der „M4A_“ sein muss, für M4B muss der Untertyp „M4B_“ sein und für M4P muss der Untertyp sein sei "M4P_".

Chunks iterieren, bis Chunks unbekannten Typs erkannt werden, es wird eine M4A-Datei (MPEG-4 Audio) erstellt.

## Verweise ##

* [MPEG-4 Teil 14 – von Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A, M4B, M4P) Format & Beispiel für Wiederherstellung](https://www.file-recovery.com/m4a-signature-format.htm)

