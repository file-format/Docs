{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF-Dateiformat - Was ist eine XFDF-Datei?",
  "description":"Erfahren Sie mehr über XFDF-Dateien und APIs, die XFDF-Dateien erstellen und öffnen können.",
  "linktitle" :"XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine XFDF-Datei?

Eine Datei mit der Erweiterung .xfdf ist ein XML-Formulardatenformat, das mit der Adobe Acrobat-Software generiert wird. Wie [FDF](/de/pdf/fdf/) enthält XFDF die Beschreibung der Formularelemente und ihre Werte im XML-Format. Dazu können die Namen und Werte von Textfeldern im PDF-Formular gehören. XFDF werden in einem für Menschen lesbaren Format gespeichert und können mit Programmiersprachen wie C# programmatisch gelesen werden.

## XFDF-Dateiformat - Weitere Informationen

XFDF-Dateien werden im XML-Dateiformat gespeichert, einem universellen Format, das für den Import und Export von Daten verwendet wird. Eine XFDF-Dateistruktur besteht aus einem Header, gefolgt von Feldwerten und Elementdaten, wie unten gezeigt.

|Element|Attribut|Inhalt|
---|---|---|
|\<XFDF> ||Oberstes Element|
|\<fields> ||Alle Feldwerte für diese Vorlage|
|<field (T)> |name |Feldname|
|<value (V)> |Wert |Feldwert|

## Verweise

* [Unterstützung des FDF-Formats durch Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe-Entwicklerressourcen](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

