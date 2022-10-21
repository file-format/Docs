{
  "date" : "2021-06-09",
  "keywords" :[ "m4p", "mp3", "Datei", "Erweiterung", "Format", "Was ist das m4p-Dateiformat", "Musik", "m4p-Dateiformat", "M4b vs. MP3", "Spezifikation des m4p-Dateiformats "],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das M4P-Dateiformat und APIs, die M4P-Dateien erstellen, konvertieren und öffnen können.",
  "title" :"M4P - MPEG-4 Hörbuchdateiformat",
  "linktitle" :"M4P",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Was ist eine M4P-Datei?
Die Datei mit der Erweiterung .m4p ist eine Audiodatei, die normalerweise im Apple iTunes Store zum Download verfügbar ist. Mit anderen Worten können wir sagen, dass M4P eine AAC-Datei ist, aber durch die Verwendung eines Digital Rights Management (DRM) kopiergeschützt ist. Das bedeutet, dass M4P-Dateien nur auf autorisierten Systemen oder Geräten abgespielt werden können. Normalerweise sind M4P-Dateien spezifisch für Apple-Multimediageräte. Diese Dateien können also nur auf Apple MacBooks, Podcasts, Smartphones wie iPhone 6 oder iPhone 7 abgespielt werden.

## M4P-Dateiformat
M4P steht für MPEG 4 Protected (Audio) und codiert das Audio mit Advanced Audio Codec (AAC) und schützt die Datei vor unbefugter Verwendung der Datei. Dieses Dateiformat wird normalerweise als Audiodateiformat eines iTunes Music Store angesehen. Apple verwendet sein FairPlay Digital Rights Management (DRM)-System, um M4P-Dateien zu schützen. FairPlay DRM basiert auf einer von Veridisc entwickelten Technologie. Sein Schutzmechanismus funktioniert durch die Verschlüsselung des AAC-Audiostreams mit der AES-Verschlüsselung. Der Benutzer erhält einen Hauptschlüssel, der seinem Konto zur Entschlüsselung zugeordnet ist. Dieses Dateiformat wurde als Ersatz für das MP3-Dateiformat eingeführt, da MP3 ursprünglich nicht als Audiodatei gedacht war, sondern als Schicht III in einer MPEG 1- oder 2-Videodatei.


## Spezifikation des M4P-Dateiformats

Ähnlich wie bei [M4A](/de/audio/m4a/) bestehen auch die M4P-Dateien aus aufeinanderfolgenden Chunks. Jeder Chunk hat einen 8-Byte-Header und ist wie folgt unterteilt:
- 4-Byte-Chunk-Größe (Big-Endian, High-Byte zuerst)
- 4-Byte-Chunk-Typ - eine der vordefinierten Signaturen: "mdat", "moov", "pnot", "moof", "udta", "uuid", "free", "skip", "ftyp", „jP2“, „wide“, „load“, „imap“, „matt“, „chap“, „kmat“, „clip“, „crgn“, „sync“, „tmcd“, „PICT“, „scpt ", "ctab", "ssrc".

Ähnlich wie bei M4A ist der erste Block in M4P vom Typ „ftype“ und hat einen Untertyp bei Offset 8. Der M4P wird durch den Untertyp definiert, der „M4P_“ sein muss.

Stücke wiederholen, bis ein Stück unbekannten Typs erkannt wird, es wird eine M4P-Datei (MPEG-4 Audio) erstellt.

## Verweise ##

* [MPEG-4 Teil 14 – von Wikipedia](https://en.wikipedia.org/wiki/MPEG-4_Part_14)
* [MPEG-4 Part 14 Audio (M4A, M4B, M4P) Format & Beispiel für Wiederherstellung](https://www.file-recovery.com/m4a-signature-format.htm)

