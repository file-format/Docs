{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/VT-Dateiformat",
  "description":"Erfahren Sie mehr über das PDF/VT-Dateiformat und APIs, die PDF/VT-Dateien erstellen und öffnen können.",
  "linktitle" :"PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Was ist PDF/VT? #

PDF/VT, veröffentlicht als [ISO 16612-2](https://www.iso.org/standard/46428.html) im August 2010 als Standard, wurde entwickelt, um den variablen Dokumentendruck (VDP) in einer Vielzahl von zu ermöglichen Umgebungen. Der Standard macht variable Informationen und Transaktionsdruck als Grundlage für den Standard. Der variable Datendruck wird verwendet, wenn ein Teil der Informationen für jeden Empfänger des Inhalts unterschiedlich ist. Der Transaktionsdruck umfasst Rechnungen, Kontoauszüge und andere Dokumente, die Rechnungsinformationen mit Marketinginformationen kombinieren. Dies führt zu einer Mischung aus verbesserter Verarbeitung von Bildern, Text und anderen Inhaltstypen. PDF/VT ermöglicht eine zuverlässige und dynamische Verwaltung von Seiten für High Volume Transactional Output (HVTO)-Druckdaten durch Verwendung des Document Part Metadata (DPM)-Konzepts. PDF/VT-Dateien können im Adobe Acrobat Viewer geöffnet werden, ohne dass eine andere Komponente hinzugefügt werden muss.

## Dokumentteilhierarchie ##

Die Document Part (DPart)-Hierarchie ist wie eine Baumstruktur von Document Part-Knoten, die auf allen Seiten im Dokument basiert. Die Elemente dieses Baums werden als DPart-Knoten bezeichnet. Jeder interne Knoten enthält andere DPart-Knoten und jeder Blattknoten gibt eine oder mehrere Seiten für einen Empfänger an. Im Wesentlichen legt die DPart-Hierarchie die Reihenfolge und Beziehung von Dokumenten oder Dokumententeilen in einer PDF/VT-Datei fest. Die Baumstruktur der DPart-Knoten stellt den internen Inhalt eines PDF/VT-Dokuments einfach dar, da es Unterdokumente für viele Empfänger enthalten kann und jeder Dokumentteil den Seiten für einen einzelnen Empfänger entspricht. Die DPart-Hierarchie ist in PDF/VT-Dateien erforderlich.

## Dokumentteil-Metadaten (DPM) ##

Die Dokumentteilmetadaten (DPM) sind jedem Knoten in der Dokumentteilhierarchie zugeordnet und können verwendet werden, um Informationen über das Teildokument eines bestimmten Empfängers und seine Teile zu übermitteln. Insbesondere kann das DPM Informationen über die Eigenschaften oder Informationen über die Empfänger in verschlüsselter Form enthalten.

## Konformitätsstufen ##

PDF/VT wird den folgenden drei Konformitätsstufen verliehen. Diese basieren alle auf [PDF](/de/pdf/) 1.6.

* `PDF/VT-1` - Es basiert auf PDF/X-4 und enthält alle Ressourcen, die zum Rendern eines PDF-Dokuments erforderlich sind.
* `PDF/VT-2` - PDF/VT-2-Dokumente wurden für den Austausch mehrerer Dateien entwickelt und können auf externe Ausgabebedingungen, externe Inhalte oder beides verweisen. Ein PDF/VT-Dokument und alle seine referenzierten PDF-Dateien und externen Output Intents werden gemeinsam als PDF/VT-2-Dateisatz bezeichnet. Acrobat 9 und unterstützen diese Funktion.
* „PDF/VT-2s“ – Unterstützt PDF/VT-2-Live-Streaming. Dadurch können segmentierte Datenabschnitte verarbeitet werden.

## Verweise ##

* [PDF/VT – Von Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [ISO 16612-2 Grafiktechnologie](https://www.iso.org/standard/46428.html)

