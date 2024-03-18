{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "extension", "file", "format", "eBook", "Kindle File Format", "AZW3 File Structure" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das AZW3-Dateiformat und APIs, die AZW3-Dateien erstellen und öffnen können.",
  "title" :"Was ist eine AZW3-Datei?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## Was ist eine AZW3-Datei?

AZW3, auch bekannt als Kindle Format 8 (**KF8**), ist die modifizierte Version des digitalen E-Book-Dateiformats [AZW](/de/ebook/azw/), das für Amazon Kindle-Geräte entwickelt wurde. Das Format ist eine Erweiterung älterer AZW-Dateien und wird auf Kindle Fire-Geräten nur mit Abwärtskompatibilität für das Vorfahren-Dateiformat verwendet, dh [MOBI](/de/ebook/mobi/) und AZW. Amazon hat das KFX-Format (KF Version 10) nach KF8 eingeführt, das auf den neuesten Kindle-Geräten verwendet wird. AZW3-Dateien haben den Internetmedientyp application/vnd.amazon.mobi8-ebook. AZW3-Dateien können in eine Reihe anderer Dateiformate konvertiert werden, z. B. [PDF](/de/pdf/), [EPUB](/de/ebook/epub/), [AZW](/de/ebook/azw/), [DOCX](/de/word-processing/docx/) und [RTF](/de/word-processing/rtf/).

## AZ3/KF8-Dateiformat ##

KF8-Dateien sind binärer Natur und behalten die Struktur eines MOBI-Dateiformats als PDB-Datei bei. Wie bereits erwähnt, kann eine KF8-Datei später sowohl aus einer MOBI- als auch aus einer neueren KF8-Version von EPUB bestehen. Die internen Details des Formats wurden von [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack) entschlüsselt, einem Python-Skript, das die endgültig kompilierte Datenbank parst und MOBI- oder AZW-Quelldateien daraus extrahiert. AZW3 (KF8)-Dateien zielen auf die EPUB3-Version mit der Abwärtskompatibilität für EPUB ab. KF8 kompiliert die EPUB-Dateien und generiert eine binäre Struktur basierend auf dem PDB-Dateiformat.

## Verweise ##

* [KF8 – Von Wikipedia](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)

