{
  "date" : "2020-08-20",
  "keywords" :[ "eot-Datei", "eot-Dateiformat", "was ist eine eot-Datei", "Datei", "eot-Beispiel", "eot-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - Dateiformat für TrueType-Schriftarten",
  "description":"Erfahren Sie mehr über das EOT-Dateiformat und APIs zum Erstellen und Öffnen von EOT-Dateien.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## Was ist eine EOT-Datei?

Eine Datei mit der Erweiterung .eot ist eine OpenType-Schriftart, die in ein Dokument eingebettet ist. Diese werden hauptsächlich in Webdateien wie einer Webseite verwendet. Es wurde von Microsoft erstellt und wird von Microsoft-Produkten unterstützt, einschließlich der PowerPoint-Präsentationsdatei [.pps](/de/presentation/pps). Die Datei wird nicht primär verwendet und ist eine Art Begleitdokument zum Hauptdokument oder zur Webseite. Ähnlich wie OTF-Schriftarten unterstützt EOT sowohl Postscript- als auch TrueType-Konturen für die Glyphen. EOT-Dateien sind kleiner, da sie mit LZ-Komprimierung komprimiert werden. EOT verwendet ein Microsoft-Tool, um eine Schriftart aus vorhandenen TTF/OTF-Schriftarten zu erstellen.

## Kurze Geschichte

Die EOT-Schriftart wurde 2007 als Teil von CSS3 beim W3C eingereicht, wurde jedoch aufgrund ihrer Anforderungen, dauerhaft auf einem Remote-System installiert zu sein, zum Grund für ihre Ablehnung. Es wurde im März 2008 erneut eingereicht, aber das W3C entschied sich schließlich für das damals standardisierte [Web Font Format](/de/font/woff/) (WOFF).

## EOT-Dateiformat

Details zum EOT-Dateiformat finden Sie auf der [W3-Einreichungsseite](https://www.w3.org/Submission/EOT/#FileFormat) und erläutert die von diesem Schriftformat verwendete Struktur. Das EOT besteht aus einer einzigen EMBEDDEDFONT-Struktur, die genügend grundlegende Informationen über den Schriftartnamen und die unterstützten Zeichen bereitstellt. Durch das Packen dieser Informationen können Benutzeragenten das Entpacken, Dekomprimieren oder Installieren der Schriftart vermeiden, wenn sie bereits auf dem Computer vorhanden ist.

### EMBEDDEDFONT-Struktur
Die EMBEDDEDFONT-Struktur wurde drei Revisionen unterzogen, wobei bei jeder Revision zusätzliche Daten am Ende der Struktur hinzugefügt wurden. Die letzte Überarbeitung der EMBEDDEDFONT-Struktur ist wie unten dargestellt.

|Datentyp|Eintragsname|Beschreibung|
---|---|---|
|unsigned long|EOTSize|Gesamtstrukturlänge in Bytes (einschließlich Zeichenfolgen- und Schriftartdaten)|
|unsigned long|FontDataSize|Länge der OpenType-Schriftart (FontData) in Bytes|
|unsigned long|Version|Versionsnummer dieses Formats - 0x00020002|
|unsigned long|Flags|Flags werden verarbeitet|
|byte[10]|FontPANOSE|Der PANOSE-Wert für diese Schriftart – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|In Windows wird dies von TEXTMETRIC.tmCharSet abgeleitet. Dieser Wert gibt den Zeichensatz der Schriftart an. DEFAULT_CHARSET (0x01) gibt keine Präferenz an. - Siehe https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|Wenn das Bit für ITALIC in OS/2.fsSelection gesetzt ist, ist der Wert 0x01 – siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|unsigned long|Weight|Der Gewichtswert für diese Schriftart – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|unsigned short|fsType|Type-Flags, die Informationen über Einbettungsberechtigungen bereitstellen – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|unsigned short|MagicNumber|Magische Nummer für EOT-Datei - 0x504C. Wird verwendet, um auf Datenbeschädigung zu prüfen.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (Bits 0-31) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (Bits 32-63) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (Bits 64-95) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (Bits 96-127) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (Bits 0–31) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (Bits 32–63) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CheckSumAdjustment|head.CheckSumAdjustment – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|unsigned long|Reserviert1|Reserviert - muss 0 sein|
|unsigned long|Reserviert2|Reserviert - muss 0 sein|
|unsigned long|Reserviert3|Reserviert - muss 0 sein|
|unsigned long|Reserviert4|Reserviert - muss 0 sein|
|unsigned short|Padding1|Padding, um die lange Ausrichtung beizubehalten. Der Füllwert muss immer auf 0x0000 gesetzt werden.|
|unsigned short|FamilyNameSize|Anzahl der vom FamilyName-Array verwendeten Bytes|
|byte|FamilyName[FamilyNameSize]|Array von UTF-16-Zeichen mit der Länge von FamilyNameSize Bytes. Dies ist die Zeichenkette der englischen Schriftfamilie, die in der Namenstabelle der Schriftart gefunden wird (Namens-ID = 1) – siehe https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|Paddingwert muss immer auf 0x0000 gesetzt werden.|
|unsigned short|StyleNameSize|Anzahl der vom StyleName verwendeten Bytes|
|byte|StyleName[StyleNameSize]|Array von UTF-16-Zeichen mit der Länge von StyleNameSize Bytes. Dies ist die Zeichenkette der Unterfamilie der englischen Schriftart, die in der Namenstabelle der Schriftart gefunden wird (Namens-ID = 2) – siehe https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|Paddingwert muss immer auf 0x0000 gesetzt werden.|
|unsigned short|VersionNameSize|Anzahl der von VersionName verwendeten Bytes|
|bytes|VersionName[VersionNameSize]|Array von UTF-16-Zeichen mit der Länge von VersionNameSize Bytes. Dies ist die englischsprachige Versionszeichenfolge, die in der Namenstabelle der Schriftart gefunden wird (Namens-ID = 5) – siehe https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|Auffüllwert muss immer auf 0x0000 gesetzt werden.|
|unsigned short|FullNameSize|Anzahl der vom FullName verwendeten Bytes|
|byte|FullName[FullNameSize]|Array von UTF-16-Zeichen mit der Länge von FullNameSize-Bytes. Dies ist die vollständige Namenszeichenfolge in englischer Sprache, die in der Namenstabelle der Schriftart gefunden wird (Namens-ID = 4) – Siehe https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|Auffüllwert muss immer auf 0x0000 gesetzt werden.|
|unsigned short|RootStringSize|Anzahl der vom RootString-Array verwendeten Bytes|
|byte|RootString[RootStringSize]|Array von UTF-16-Zeichen mit der Länge von RootStringSize-Bytes.|
|unsigned long|RootStringCheckSum|RootString CheckSum-Wert. Siehe Algorithmus zur Verarbeitung von RootStringChecksum unten.|
|unsigned long|EUDCCodePage|Codepage-Wert für die Unterstützung von EUDC-Schriftarten erforderlich.|
|unsigned short|Padding6|Auffüllwert muss immer auf 0x0000 gesetzt werden.|
|unsigned short|SignatureSize|Anzahl der vom Signatur-Array verwendeten Bytes. Derzeit reserviert und sollte auf 0x0000 gesetzt werden.|
|byte|Signature[SignatureSize]|Aktuell reserviert. Wenn die SignatureSize 0x0000 ist, hat dieses Array keine Länge.|
|unsigned long|EUDCFlags|Verarbeitungs-Flags für die EUDC-Schriftart. Typische Werte könnten TTEMBED_XORENCRYPTDATA und TTEMBED_TTCOMPRESSED sein.|
|unsigned long|EUDCFontSize|Anzahl der vom Signatur-Array verwendeten Bytes.|
|byte|EUDCFontData[EUDCFontSize]|Anzahl der für die EUDC-Schriftartdaten verwendeten Bytes. Wenn die EUDCFontSize 0x00000000 ist, hat dieses Array keine Länge.|
|byte|FontData[FontDataSize]|Die Schriftdaten für diese EOT-Datei. Die Daten können komprimiert oder XOR-verschlüsselt sein, wie durch die Verarbeitungs-Flags angegeben.|

## Verweise

* [EOT-Dateiformat](https://www.w3.org/Submission/EOT/)
* [Embedded OpenType](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [Schrifteinbettung](https://en.wikipedia.org/wiki/Font_embedding)

