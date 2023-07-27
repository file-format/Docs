{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "XML-Papierspezifikationen", "Datei", "Erweiterung", "Dateiformat", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Seitenlayout-Dateiformat",
  "description":"Erfahren Sie mehr über das XPS-Dateiformat und APIs, die XPS-Dateien erstellen und öffnen können.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Was ist eine XPS-Datei? ##

Eine XPS-Datei stellt Seitenlayoutdateien dar, die auf von Microsoft erstellten XML-Papierspezifikationen basieren. Es wurde als Ersatz für das EMF-Dateiformat entwickelt und ähnelt dem Dateiformat [PDF](/de/pdf/), verwendet jedoch XML für Layout, Aussehen und Druckinformationen eines Dokuments. Es ist in der Tat gerechtfertigter zu sagen, dass XPS ein Versuch auf PDF ist, aber aus vielen Gründen nicht genug Popularität erlangen konnte, da es PDF gehört. Microsoft stellt XPS Document Writer standardmäßig ab Windows 7 für die Erstellung von XPS-Dateien zur Verfügung. XPS-Dateien können generiert werden, indem beim Drucken des Dokuments der "Microsoft XPS Document Writer" als Drucker ausgewählt wird.

XPS-Viewer sind als Teil von Windows Vista, Windows 7, Windows 8 und Internet Explorer 6 oder höher integriert. XPS-Dateien werden schreibgeschützt, sobald sie generiert wurden. Dies erhöht das Vertrauen des Benutzers in empfangene Dokumente, die als XPS gesendet wurden, hinsichtlich der Authentizität des Dokuments. Ein XPS-Dokument kann eine oder mehrere Seiten enthalten, die aus dem Originaldokument konvertiert wurden.

## Kurze Geschichte ##

Microsoft reichte die XPS-Spezifikation bei Ecma International ein. Im Juni 2007 wurde das Ecma Technical Committee 46 (TC46) gegründet, um einen Standard zu entwickeln, der auf den OpenXPS-Papierspezifikationen basiert. Ecma International genehmigte den Ecma-Standard (ECMA-388) [XPS-Spezifikationen](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) im Juni 2009 auf der 97. Generalversammlung.

## XPS-Dateiformat ##

Das XPS-Format besteht aus XML-Markup, das die Zusammensetzung eines Dokuments und das visuelle Erscheinungsbild jeder Seite zusammen mit Rendering-Regeln zum Anzeigen oder Drucken des Dokuments definiert. Es behält alle Informationen, um ein Dokument auf jedem System neu zu erstellen, was es unabhängig von den auf diesem System verfügbaren Ressourcen macht. Das Format ist im Wesentlichen ein ZIP-Archiv, und wenn Sie die Dateierweiterung in ZIP umbenennen, sehen Sie die einzelnen Dateien, die die Dokumentdaten enthalten. Zu diesen Dokumenten gehören:

* Dokumentseitendateien (.fpage) - Enthält Dokumentinhalt und Dokumentformateinstellungen. Jede Seite in einem XPS-Dokument hat eine FPAGE-Datei.
* Dokumenteinstellungsdatei (.fdoc) - Speichert die im XPS-Archiv enthaltenen Einstellungen.
* Dokumentfragmentdateien (.frag) - Definiert die Einstellungen für die eigentliche XPS-Datei und jede Seite im Dokument hat ihre eigene .frag-Datei.

{{< figure src="../XPS-1.png" alt="XPS-Dateiformat" >}}

Diese Dateien behalten den Inhalt des Dokuments so bei, dass der XPS-Viewer diese ursprünglichen Schriftarten dennoch rendert, wenn beispielsweise jemand nicht dieselben Schriftarten auf seinem Computer installiert hat. Dies impliziert die Aufnahme einer XML-Markup-Datei für jeden:

* Buchseite
* Texte
* Eingebettete Schriftarten
* Rasterbilder
* 2D-Vektorgrafiken
* Management von Digitalen Rechten

Das XPS-Dokumentformat enthält einen klar definierten Satz von Teilen und Beziehungen, die jeweils einen bestimmten Zweck im Dokument erfüllen. Das Format erweitert auch die Paketfunktionen, einschließlich digitaler Signaturen, Miniaturansichten und Interleaving.

Ein typisches XPS-Dokument sieht wie folgt aus und kann anhand des XPS-Dateiformats [Spezifikationen] analysiert werden (https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard.pdf).

{{< figure src="../XPS-2.png" alt="XPS-Dateiformat" >}}


## Verweise ##

* [XPS-Dateiformatspezifikationen](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS – Von Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

