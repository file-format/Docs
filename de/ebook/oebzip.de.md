{
  "date" : "2021-03-23",
  "keywords" :[ "OEBZIP", "Open eBook Publication Structure", "extension", "format", "eBook", "OEBPS", "IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das OEBZIP-Dateiformat und APIs, die OEBZIP-Dateien erstellen und öffnen können.",
  "title" :"OEBZIP - Komprimierte offene eBook-Publikationsstruktur",
  "linktitle" :"OEBZIP",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Was ist eine OEBZIP-Datei? ##

Die OEBZIP-Dateien wurden vom International Digital Publishing Forum (**IDPF**) eingeführt. Ebenso [OEB](/de/ebook/oeb/), diese Dateien sind XML-basierte Spezifikationen für die Struktur, den Inhalt und die Darstellung von elektronischen Büchern, jedoch in komprimierter oder gezippter Form.

## Technische Details des OEBZIP-Dateiformats ##

Das OEBZIP stellte weitere neue Funktionalitäten im Bereich der Rendering-Steuerung zur Verfügung, darunter unter anderem Verbesserungen im Markup-Vokabular (jetzt eine grundlegende Teilmenge von XHTML 1.1) und eine stark erweiterte CSS-Unterstützung. Nachhaltigkeitsfaktoren sind gegenüber der früheren Version unverändert.

Das OEBZIP-Dateiformat besteht aus einer Reihe von Dateien, einschließlich einer obligatorischen Paketdatei, die ein Manifest enthält, das alle anderen Komponentendateien auflistet, und einem Buchrücken, der die logische Lesereihenfolge angibt. Außerdem muss ein Reader für OEBZIP-Dateien für Text in [XML](/de/web/xml/) in der Lage sein, Bilder in den Formaten [JPEG](/de/image/jpeg/) und [PNG](/de/image/png/) wiederzugeben . Inhaltskomponenten in anderen Formaten können integriert werden, aber Fallback-Inhalte müssen in einem der grundlegenden OEB-Formate bereitgestellt werden.
  

Das OEBZIP-Dateibündel wurde hauptsächlich als Mid-State-Format verwendet, wobei die Veröffentlichung für Endbenutzer von Verlagen oder Aggregatoren verwaltet wurde, die eBooks in Formen bereitstellten, die für verschiedene eBook-Viewer geeignet waren. Die Nachfolgeversion [EPUB](/de/ebook/epub/) erreicht Endnutzer wahrscheinlich eher in einem Endzustandsformat und dient auch als Zwischenzustandsformat.

## Verweise

* [OEBPS (Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [eBook öffnen](https://en.wikipedia.org/wiki/Open_eBook)


