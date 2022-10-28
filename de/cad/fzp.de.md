{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das FZP-Dateiformat und APIs, die FZP-Dateien erstellen und öffnen können.",
  "title" :"FZP-Dateiformat - Fritzing XML-Teilebeschreibungsdatei",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## Was ist eine FZP-Datei?

Eine FZP-Datei ist eine XML-Datei, die von [Fritzing](https://fritzing.org/) Electronic Circuit Prototyping and Design Application erstellt wurde. Es enthält Informationen zu den Eigenschaften, Anschlüssen und Bussen des Teils im Dateiformat [XML](/de/web/xml/). FPZ-Dateien können in Fritzing nicht unabhängig verwendet werden. Stattdessen werden sie als Teil der FZPZ-Archivdatei importiert.

## FZP-Dateiformat - Weitere Informationen

FZP-Dateien sind XML-Dateien, die Informationen zu den Eigenschaften, Anschlüssen und Bussen des Teils enthalten. Darüber hinaus enthalten FZP-Dateien auch Informationen über Titel, Beschreibung, Autor und Veröffentlichungsdatum der FZP-Datei. Wenn eine Fritzing-Teildatei exportiert wird, erstellt die Fritzing-App ein komprimiertes [FZPZ](/de/compression/fzpz/)-Archiv, das eine FZP-Datei und vier [SVG](/de/image/svg/)-Dateien enthält.

Die [Spezifikationen des FZP-Dateiformats] (https://github.com/fritzing/fzp/blob/master/docs/README.md) sind auf Github von Fritzing verfügbar.

## Beispiel für eine FZP-Dateistruktur

Eine typische FZP-Datei hat die folgende XML-Struktur.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## Verweise

* [Spezifikationen des FZP-Dateiformats](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [Neuteile mit fzpz-Erweiterung](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

