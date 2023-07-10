{
  "date" : "2019-12-09",
  "keywords" :[ "3mf-Datei", "3mf-Dateiformat", "was ist eine 3mf-Datei", "Datei", "3mf-Beispiel", "3mf-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Erfahren Sie mehr über das 3MF-Dateiformat und APIs, die 3MF-Dateien öffnen und erstellen können.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Was ist eine 3MF-Datei?

3MF, 3D Manufacturing Format, wird von Anwendungen verwendet, um 3D-Objektmodelle für eine Vielzahl anderer Anwendungen, Plattformen, Dienste und Drucker zu rendern. Es wurde entwickelt, um die Einschränkungen und Probleme in anderen 3D-Dateiformaten wie [STL](/de/cad/stl/) für die Arbeit mit den neuesten Versionen von 3D-Druckern zu vermeiden. 3MF ist ein relativ neues Dateiformat, das vom 3MF-Konsortium entwickelt und veröffentlicht wurde. Es ist reichhaltig genug, um ein Modell vollständig zu beschreiben, wobei interne Informationen, Farben und andere Eigenschaften beibehalten werden, was es erweiterbar macht, um neue Innovationen im 3D-Druck zu unterstützen. Das Format ist erweiterbar, kann allgemein übernommen werden und ist frei von Problemen, die andere weit verbreitete Dateiformate beeinträchtigen.

## Kurze Geschichte ##

Die bestehenden Einschränkungen bei verfügbaren modellbeschreibenden Dateiformaten wie STL und anderen veranlassen die führenden Marken, sich zusammenzuschließen und ein erweiterbares Dateiformat für den 3D-Druck zu formulieren. Eine wichtige Überlegung war, wie Anwendungen Modelldaten an 3D-Drucker übergeben sollten. Das 3MF-Konsortium wurde daher gegründet, um ein neues 3D-Dateiformat namens 3MF zu unterstützen, mit dem Ziel, es erweiterbar genug zu machen, um den Anforderungen des 3D-Drucks gerecht zu werden. Mehrere Unternehmen waren Teil dieses Konsortiums, darunter Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP und andere. Microsoft stellte sein in Arbeit befindliches 3D-Dateiformat als Ausgangspunkt für die gemeinsame Weiterentwicklung der Spezifikation durch das 3MF-Konsortium zur Verfügung.

## 3MF-Dateiformat – Weitere Informationen

3MF ist ein XML-basiertes Datenformat – für Menschen lesbares komprimiertes XML – das Definitionen für Daten im Zusammenhang mit der 3D-Fertigung enthält, einschließlich der Erweiterbarkeit durch Drittanbieter für benutzerdefinierte Daten. Das 3MF-Dateiformat wurde unter Berücksichtigung der Einschränkungen und Probleme anderer 3D-Dateiformate entwickelt. Dies führte zur Formulierung des 3MF-Dateiformats, das lautet:

* **Vollständig:** Enthält alle erforderlichen Modell-, Material- und Eigenschaftsinformationen in einem einzigen Archiv
* **Für Menschen lesbar:** Verwendung gängiger Strukturen wie OPC, [ZIP](/de/compression/zip/) und XML zur Vereinfachung der Entwicklung
* **Einfach:** Eine kurze, klare Spezifikation, die die Entwicklung einfach und die Validierung schnell macht
* **Erweiterbar:** Die Nutzung von XML-Namespaces ermöglicht sowohl öffentliche als auch private Erweiterungen unter Beibehaltung der Kompatibilität
* **Eindeutig:** Klare Sprache und Konformitätstests stellen sicher, dass eine Datei von digital bis physisch immer konsistent ist
* **Kostenlos:** Der Zugriff auf und die Implementierung der 3MF-Spezifikation ist und bleibt frei von Lizenzgebühren, Patenten und Lizenzen

Die Spezifikationen für das 3MF-Dateiformat werden über [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) für den öffentlichen Zugriff und kontinuierliche Aktualisierungen gehostet. Die aktuell veröffentlichte Version ist 1.2.3, die eine Reihe von Konventionen für die Verwendung von XML und anderen weit verbreiteten Technologien beschreibt, um den Inhalt und das Erscheinungsbild eines oder mehrerer 3D-Modelle zu beschreiben. Entwickler, die Systeme zur Verarbeitung von 3MF-Dateiformaten bauen möchten, können sich für Implementierungszwecke auf diese Spezifikationen beziehen.

## Dateiformatspezifikationen ##

Das 3MF-Dateiformat verwendet die Open Packaging-Spezifikationen in Form eines ZIP-Archivs für sein physisches Modell. Es enthält einen wohldefinierten Satz von Teilen und Beziehungen, die einen bestimmten Zweck im Dokument erfüllen. Dadurch folgt das Format auch der Paketfunktion, einschließlich digitaler Signaturen und Miniaturansichten.

### Das 3MF-Dokument ###

Ein typisches 3MF-Dokument sieht wie folgt aus:

![3MF Document Structure](https://raw.githubusercontent.com/3MFConsortium/spec_core/master/images/figure_2-1.png "3MF Document Structure")

Die Nutzlast umfasst den vollständigen Teilesatz, der für die Verarbeitung des 3D-Modellteils erforderlich ist. Alle Inhalte, die zur Herstellung eines in der 3D-Nutzlast beschriebenen Objekts verwendet werden sollen, MÜSSEN im 3MF-Dokument enthalten sein. Die Beschreibung jedes Dokumententeils zusammen mit seinem Status als erforderlich oder Option ist in der folgenden Tabelle angegeben.


|**Name**|**Beschreibung**|**Beziehungsquelle**|**Erforderlich/Optional**
--- | --- | --- | ---
|3D-Modell|Enthält die Beschreibung eines oder mehrerer 3D-Objekte für die Fertigung.|Paket|ERFORDERLICH
|Kerneigenschaften|Der OPC-Teil, der verschiedene Dokumenteigenschaften enthält.|Paket|OPTIONAL
|Ursprung der digitalen Signatur|Der OPC-Teil, der die Wurzel der digitalen Signaturen im Paket ist.|Paket|OPTIONAL
|Digitale Signatur|OPC-Teile, die jeweils eine digitale Signatur enthalten.|Ursprung der digitalen Signatur|OPTIONAL
|Zertifikat für digitale Signatur|OPC-Teile, die ein Zertifikat für digitale Signatur enthalten.|Digitale Signatur|OPTIONAL
|PrintTicket|Stellt Einstellungen zur Verfügung, die beim Ausgeben der 3D-Objekte im 3D-Modellteil verwendet werden sollen.|3D-Modell|OPTIONAL
|Miniaturansicht|Enthält ein kleines JPEG- oder PNG-Bild, das die 3D-Objekte im Paket oder das Paket als Ganzes darstellt.|Paket|OPTIONAL
|3D-Textur|Enthält eine Textur, die verwendet wird, um Farbe auf ein 3D-Objekt im 3D-Modellteil anzuwenden (verfügbar für Erweiterungen)|3D-Modell|OPTIONAL
|Benutzerdefinierte Teile|OPC-Teile, die Metadaten zugeordnet sind|Paket|OPTIONAL

Die [Teile und Beziehungen](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D-Modelle](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Objektressourcen](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Materialressourcen](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) und [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) Abschnitte der Spezifikationen Dokument geben detaillierte Informationen über das 3MF-Dokument.

## Verweise ##

* [3MF-Dateiformatspezifikationen](https://github.com/3MFConsortium/spec_core)
* [3MF – von Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

