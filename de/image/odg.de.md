{
  "date" : "2019-10-11",
  "keywords" :[ "odg-Datei", "odg-Dateiformat", "was ist eine odg-Datei", "Datei", "odg-Beispiel", "odg-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ODG-Dateiformat",
  "description":"Erfahren Sie mehr über das ODG-Dateiformat und APIs, die ODG-Dateien erstellen und öffnen können.",
  "linktitle" : "ODG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine ODG-Datei?

Das ODG-Dateiformat wird von der Draw-Anwendung von Apache OpenOffice verwendet, um Zeichnungselemente als Vektorbild zu speichern. Es folgt den von Advancement of Structural Information Standards (OASIS) festgelegten XML-basierten Dateiformatspezifikationen. ODG stellt Zeichnungen als Vektorbilder mit Punkten, Linien und Kurven dar. Neben OpenOffice bieten auch LibreOffice und andere Anwendungen Unterstützung für die Arbeit mit dem ODG-Dateiformat. Andere von OpenOffice unterstützte Formate sind beispielsweise [ODT](/de/word-processing/odt/), ODF, [ODP](/de/presentation/odp/) und [ODS](/de/spreadsheet/ods/).


## ODG-Dateiformatspezifikationen

Das ODG-Dateiformat basiert auf dem OpenDocument-Format, das ein strukturiertes XML-Dokumentformat mit einem gut definierten Schema ist.
Jede strukturelle Komponente eines OpenDocument-Formats wird durch ein Element dargestellt, das zugeordnete Attribute hat. Die XML-basierte Struktur ist für alle Dokumenttypen wie Textdokument, Tabellenkalkulation oder eine Zeichnungsdatei gleich. Ein Dokument kann verschiedene Stile enthalten. Eine OpenDocument-Dateistruktur besteht aus den folgenden Elementen.
* Dokument Root
* Metadaten dokumentieren
* Körperelement und Dokumenttypen
* Anwendungseinstellungen
* Skripte
* Schriftartdeklarationen
* Stile
* Seitenstile und Layouts

## Dokumentenwurzeln ##

Ein Dokumentstammelement enthält das gesamte Dokument und ist das primäre Element einer Datei im OpenDocument-Format. Dieselben Arten von Dokumentwurzelelementen sind auf alle Arten von Dokumenten wie Text, Dokumente, Tabellenkalkulationen und Zeichnungsdokumente anwendbar.

### Wurzelelemente ###
Ein einzelnes XML-Dokument wird durch ein eigenes Root-Element dargestellt. Die fünf verschiedenen unterstützten Root-Elemente sind wie folgt.

`<office:document> ` - Vollständiges Office-Dokument in einem einzigen XML-Dokument.
`<office:document-content> ` - Dokumentinhalt und im Inhalt verwendete automatische Stile.
`<office:document-styles> ` - Stile, die im Dokumentinhalt verwendet werden, und automatische Stile, die in den Stilen selbst verwendet werden.
`<office:document-meta> ` - Dokumentiere Metainformationen, wie z. B. den Autor oder den Zeitpunkt der letzten Speicheraktion.
`<office:document-settings> ` - Anwendungsspezifische Einstellungen wie Fenstergröße oder Druckerinformationen.

### Metadaten des ODG-Dokuments ###
Das OpenDocument enthält alle Metadatenelemente im \<office:meta> Element. Diese allgemeinen Informationen zu einem Dokument sind am Anfang des Dokuments enthalten, und Anwendungen können mehrere Instanzen derselben Elemente aktualisieren.

### Körperelement und Dokumenttypen ###
Der Dokumentkörper gibt den Inhaltstyp an, der in dem Dokument enthalten ist, indem das Dokumenttypelement verwendet wird. Diese Dokumenttypen sind:
* Textdokumente
* Zeichnungsunterlagen
* Präsentationsunterlagen
* Tabellendokumente
* Diagrammdokumente
* Bilddokumente

### Anwendungseinstellungen ###
Die Einstellungen für Office-Anwendungen stellen verschiedene Einstellungen dar, die sich auf die Dokumentkonfiguration oder das visuelle Erscheinungsbild des Dokuments beziehen. Jede Kategorie wird durch ein ` dargestellt<config:config-item-set> `. Beispiele für solche Einstellungskategorien sind:
* Dokumenteinstellungen zB Standarddrucker
* Einstellungen anzeigen, z. B. Zoomstufe

### Skripte ###
Es ist üblich, dass ein Dokument mehrere Skripte enthält. Jedes Skript in einer OpenDocument-Datei wird durch ein ` dargestellt<office:script> `Element. Diese Skriptelemente sind in einem einzigen ` enthalten<office:scripts> `Element. Skripts aktualisieren ein Dokument nicht, während das Dokument geladen wird.
### Schriftartdeklarationen ###

Eine Schriftartdeklaration enthält Informationen über die vom Autor eines Dokuments verwendeten Schriftarten. Diese Informationen helfen, diese Schriftarten auf anderen Systemen zu finden.
```
<define name="office-font-face-decls">
<optional>
<element name="office:font-face-decls">
<zeroOrMore>
<ref name="style-font-face"/>
</zeroOrMore>
</element>
</optional>
</define>
```
### Stile ###
Die folgenden Stile werden vom OpenDocument-Format unterstützt.

„Allgemeine Stile“ – Die XML-Darstellungen solcher Stile werden als Stile bezeichnet
„Automatische Stile“ – Enthält Formatierungseigenschaften, die in der Benutzeroberflächenansicht eines Dokuments einem Objekt wie einem Absatz zugewiesen werden.
„Mater Styles“ – ein allgemeiner Stil, der Formatierungsinformationen und zusätzliche Inhalte enthält, die zusammen mit dem Dokumentinhalt angezeigt werden, wenn der Stil angewendet wird. Ein Beispiel für einen Masterstil sind Masterseiten.

## Verweise ##
* [OASIS Open Document Format für Office-Anwendungen](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument-Format – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

