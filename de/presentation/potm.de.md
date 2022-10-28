{
  "date" : "2019-10-11",
  "keywords" :[ "Potm-Datei", "Potm-Dateiformat", "Was ist eine Potm-Datei", "Datei", "Potm-Beispiel", "Potm-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTM - Microsoft PowerPoint-Vorlagendatei mit Makros",
  "description":"Erfahren Sie mehr über das POTM-Dateiformat und APIs, die POTM-Dateien erstellen und öffnen können.",
  "linktitle" : "POTM",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine POTM-Datei?

Dateien mit der Erweiterung POTM sind Microsoft PowerPoint-Vorlagendateien mit Unterstützung für Makros. POTM-Dateien werden mit PowerPoint 2007 oder höher erstellt und enthalten Standardeinstellungen, die zum Erstellen weiterer Präsentationsdateien verwendet werden können. Diese Einstellungen können Stile, Hintergründe, Farbpaletten, Schriftarten und Standardeinstellungen sowie Makros umfassen, die aus benutzerdefinierten Funktionen für bestimmte Aufgaben bestehen. Sie können auch von einer früheren Version von PowerPoint mit installierter Unterstützung für Open XML-Dokumente geöffnet werden. POTM-Dateien können in Microsoft PowerPoint zur Bearbeitung wie jede andere PowerPoint-Datei geöffnet werden.

## Dateiformatspezifikationen ##

Das POTM-Dateiformat basiert auf Office OpenXML-Spezifikationen und ähnelt der Struktur der [PPTX](/de/presentation/pptx/)-Datei, die ein komprimiertes [ZIP](/de/compression/zip/)-Archiv ist.

Folien in einer POTM-Datei können Text, Bilder, Videos, Grafiken und andere Objekte enthalten, die innerhalb der Seite frei angeordnet werden können. POTM-Vorlagen werden dann verwendet, um mehrere Dateien zu erstellen, die alle Formatierungsoptionen der Datei erben. In der POTM-Datei enthaltene Makros werden daher auch von anderen Präsentationen vererbt. Die Einbettung in die Dokumentenstruktur erfolgt über den in MS Office enthaltenen Macro Recorder, der Befehlsfolgen speichern und Makros erstellen kann, um diese automatisch zu replizieren.

Dateien, die mit dem Open XML-Dateiformat von Office generiert wurden, sind eine Sammlung von XML-Dateien zusammen mit anderen Dateien, die Verknüpfungen zwischen allen enthaltenen Dateien bereitstellen. Diese Sammlung ist eigentlich ein komprimiertes Archiv, das extrahiert werden kann, um seinen Inhalt anzuzeigen. Benennen Sie dazu einfach die POTM-Dateierweiterung in zip um und extrahieren Sie sie, um ihren Inhalt zu beobachten.

Die folgenden Abschnitte beleuchten jeden einzelnen von ihnen.

### [Content_Types].xml ###

Dies ist die einzige Datei, die beim Extrahieren der ZIP-Datei auf der Basisebene gefunden wird. Es listet die Inhaltstypen für Teile innerhalb des Pakets auf. Alle Verweise auf die im Paket enthaltenen XML-Dateien werden in dieser XML-Datei referenziert. Es folgt ein Inhaltstyp für einen Folienteil:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Wenn dem Paket neue Teile hinzugefügt werden müssen, können Sie dies tun, indem Sie das neue Teil hinzufügen und alle Beziehungen innerhalb der .rels-Dateien aktualisieren. Zu beachten ist, dass für eine solche Änderung auch die Content_Types.xml aktualisiert werden muss.

### \_rels (Ordner) ###

Beziehungen zwischen den anderen Teilen und Ressourcen außerhalb des Pakets werden vom Beziehungsteil verwaltet. Der Ordner "Beziehungen" enthält eine einzelne XML-Datei, in der die Beziehungen auf Paketebene gespeichert sind. Links zu den wichtigsten Teilen der Präsentationsdateien sind in dieser Datei als URIs enthalten. Diese URIs identifizieren die Art der Beziehung jedes Schlüsselteils zum Paket. Dies umfasst die Beziehung zum primären Office-Dokument, das sich als ppt/presentation.xml befindet, und andere Teile innerhalb von docProps als Kern- und erweiterte Eigenschaften.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Jeder Teil des Dokuments, der die Quelle einer oder mehrerer Beziehungen ist, hat seinen eigenen Beziehungsteil, in dem sich jeder dieser Beziehungsteile in einem \_rels-Unterordner des Teils befindet und benannt wird, indem '.rels' an den Namen des Teils angehängt wird Teil. Der Hauptinhaltsteil (presentation.xml) hat seinen eigenen Beziehungsteil (presentation.xml.rels). Es enthält Beziehungen zu anderen Teilen des Inhalts wie slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml sowie die URIs für externe Links.

#### Explizite Beziehung ####

Bei einer expliziten Beziehung wird mit dem Id-Attribut von a auf eine Ressource verwiesen<Relationship> Element. Das heißt, die ID in der Quelle wird direkt einer ID eines Beziehungselements zugeordnet, mit einem expliziten Verweis auf das Ziel.

Eine Folie könnte beispielsweise einen Hyperlink wie diesen enthalten:
```
<a:hlinkClick r:id#"rId2">
```
Die r:id#"rId2" verweist auf die folgende Beziehung innerhalb des Beziehungsteils für die Folie (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implizite Beziehung ####

Für eine implizite Beziehung gibt es keinen solchen direkten Verweis auf ein `<Relationship> ID`. Stattdessen wird die Referenz verstanden.

### ppt-Ordner ###

Dies ist der Hauptordner, der alle Details zum Inhalt der Präsentation enthält. Standardmäßig hat es folgende Ordner:

* \_rels
* Thema
* Folien
* Folienlayouts
* SlideMaster

und folgende XML-Dateien:

* Präsentation.xml
* presProps.xml
* tableStyles.xml
* viewProps.xml

## Verweise ##

* [[MS-PPTX] - PPTX-Dateiformat](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)
* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)

