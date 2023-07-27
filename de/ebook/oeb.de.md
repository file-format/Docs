{
  "date" : "2021-03-23",
  "keywords" :[ "OEB", "Open eBook Publication Structure", "extension", "format", "eBook", "OEBPS", "IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das OEB-Dateiformat und APIs, die OEB-Dateien erstellen und öffnen können.",
  "title" :"OEB - Offene eBook-Publikationsstruktur",
  "linktitle" : "OEB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-22"
}

## Was ist eine OEB-Datei?

Die OEB-Dateien wurden vom International Digital Publishing Forum (**IDPF**) eingeführt. Formaler werden die OEB-Dateien auch als **OEBPS** bezeichnet. Diese Dateien sind XML-basierte Spezifikationen für die Struktur, den Inhalt und die Präsentation von elektronischen Büchern. Dieses Dateiformat wurde durch das Format [EPUB](/de/ebook/epub/) ersetzt.

## Technische Details des OEB-Dateiformats

Das OEB-Dateiformat besteht aus einer Reihe von Dateien, einschließlich einer obligatorischen Paketdatei, die ein Manifest enthält, das alle anderen Komponentendateien auflistet, und einem Buchrücken, der die logische Lesereihenfolge angibt. Außerdem muss ein Reader für OEB-Dateien für Text in [XML](/de/web/xml/) in der Lage sein, Bilder in den Formaten [JPEG](/de/image/jpeg/) und [PNG](/de/image/png/) wiederzugeben . Inhaltskomponenten in anderen Formaten können integriert werden, aber Fallback-Inhalte müssen in einem der grundlegenden OEB-Formate bereitgestellt werden.

Das OEBPS 1.2 war ein eng gekoppeltes Update der vorherigen Version (OEBPS 1.0.1). Es bot moderne Funktionalität im Bereich der Rendering-Steuerung, darunter unter anderem Verbesserungen im Markup-Vokabular (jetzt eine echte Teilmenge von XHTML 1.1) und eine stark erweiterte CSS-Unterstützung. Nachhaltigkeitsfaktoren sind gegenüber der früheren Version unverändert.
  

Das OEB-Dateibündel wurde hauptsächlich als Mid-State-Format verwendet, wobei die Veröffentlichung für Endbenutzer von Verlagen oder Aggregatoren verwaltet wurde, die E-Books in Formen bereitstellten, die für verschiedene E-Book-Viewer geeignet waren. Seine Nachfolgeversion, [EPUB](/de/ebook/epub/), wird Endnutzer wahrscheinlich eher als Endzustandsformat erreichen und auch als Mittelzustandsformat dienen.

## Verweise

* [OEBPS (Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [eBook öffnen](https://en.wikipedia.org/wiki/Open_eBook)


