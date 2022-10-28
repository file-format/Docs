{
  "date" : "2019-10-11",
  "keywords" :[ "Potx-Datei", "Potx-Dateiformat", "Was ist eine Potx-Datei", "Datei", "Potx-Beispiel", "Potx-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POTX - Microsoft PowerPoint-Präsentationsvorlage",
  "description":"Erfahren Sie mehr über das POTX-Dateiformat und APIs, die POTX-Dateien erstellen und öffnen können.",
  "linktitle" : "POTX",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine POTX-Datei?

Dateien mit der Erweiterung .POTX stellen Microsoft PowerPoint-Vorlagenpräsentationen dar, die mit Microsoft PowerPoint 2007 und höher erstellt wurden. Dieses Format wurde erstellt, um das Dateiformat [POT](/de/presentation/pot/) zu ersetzen, das auf dem binären Dateiformat basiert und von PowerPoint 97-2003 unterstützt wird. Die generierten Dateien können verwendet werden, um Präsentationen mit demselben Layout und anderen Einstellungen zu erstellen, die auf neue Dateien angewendet werden müssen. Diese Einstellungen können Stile, Hintergründe, Farbpaletten, Schriftarten und Standardeinstellungen umfassen. Solche Dateien werden generiert, um gebrauchsfertige Vorlagendateien für den amtlichen Gebrauch zu erstellen.

## Kurze Geschichte ##

Anfang des Jahres 2000 beschloss Microsoft, die Änderung vorzunehmen, um den Standard für **Office Open XML** aufzunehmen. Dokumente verschiedener Typen unter diesem neuen Standard wurden durch das Anhängen von „X“ in ihren Erweiterungen gekennzeichnet, wobei „X“ für XML steht. 2007 wurde dieses neue Dateiformat Teil von Office 2007 und wird auch in den neuen Versionen von Microsoft Office weitergeführt. Der neue Dateityp hat zusätzliche Vorteile von kleinen Dateigrößen, weniger Änderungen durch Beschädigung und gut formatierter Bilddarstellung.

## Dateiformatspezifikationen ##

Dateien, die mit dem Open XML-Dateiformat von Office generiert wurden, sind eine Sammlung von XML-Dateien zusammen mit anderen Dateien, die Verknüpfungen zwischen allen Bestandteilen der Dateien bereitstellen. Diese Sammlung ist eigentlich ein komprimiertes Archiv, das extrahiert werden kann, um seinen Inhalt anzuzeigen. Benennen Sie dazu einfach die POTX-Dateierweiterung in zip um und extrahieren Sie sie, um ihren Inhalt zu beobachten.

Die folgenden Abschnitte beleuchten jeden einzelnen von ihnen.

### [Content_Types].xml ###

Dies ist die einzige Datei, die beim Extrahieren der ZIP-Datei auf der Basisebene gefunden wird. Es listet die Inhaltstypen für Teile innerhalb des Pakets auf. Alle Verweise auf die im Paket enthaltenen XML-Dateien werden in dieser XML-Datei referenziert. Es folgt ein Inhaltstyp für einen Folienteil:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Wenn dem Paket neue Teile hinzugefügt werden müssen, können Sie dies tun, indem Sie das neue Teil hinzufügen und alle Beziehungen innerhalb der .rels-Dateien aktualisieren. Zu beachten ist, dass für eine solche Änderung auch die Content_Types.xml aktualisiert werden muss.

### \_rels (Ordner) ###

Beziehungen zwischen den anderen Teilen und Ressourcen außerhalb des Pakets werden vom Beziehungsteil verwaltet. Der Ordner "Beziehungen" enthält eine einzelne XML-Datei, in der die Beziehungen auf Paketebene gespeichert sind. Links zu den wichtigsten Teilen der PPTX-Dateien sind in dieser Datei als URIs enthalten. Diese URIs identifizieren die Art der Beziehung jedes Schlüsselteils zum Paket. Dies umfasst die Beziehung zum primären Office-Dokument, das sich als ppt/presentation.xml befindet, und andere Teile innerhalb von docProps als Kern- und erweiterte Eigenschaften.
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

