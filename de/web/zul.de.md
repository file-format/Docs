{
  "date" : "2021-05-24",
  "keywords" :["zul", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "öffnen"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK-Benutzeroberflächendatei",
  "description":"Erfahren Sie mehr über das ZUL-Dateiformat und APIs, die ZUL-Dateien erstellen und öffnen können.",
  "linktitle" :"ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Was ist eine ZUL-Datei?

Eine Datei mit der Erweiterung .zul ist eine Webdatei, die mit der User Interface Markup Language (ZUML) erstellt wurde und Definitionen für Elemente der Benutzeroberfläche enthält. Ajax- und Java-Klassen unterstützen die Verwendung von [XML](/de/web/xml/)-basiertem ZUML für die Entwicklung serverseitiger Dateien. Das ZUL-Dateiformat wurde von ZK entwickelt, einem UI-Framework, mit dem Sie Web- und Mobilanwendungen ohne Kenntnisse von JavaScript oder AJAX erstellen können.

## ZUL-Dateiformat

ZUL-Dateien sind XML-basiert und bestehen aus verschiedenen Elementen zum Erstellen der Benutzeroberfläche. Der ZK-Loader verwendet jedes XML-Element, um eine Komponente zu erstellen. Die Gesamtverarbeitung der Seitenelemente wie Seitentitel, Beschreibung etc. wird durch jede XML-Verarbeitungsanweisung von ZUML beschrieben.

### ZUL-Beispiel

Im folgenden Beispiel für ZUML-Code gibt die erste Zeile den Seitentitel an, die zweite Zeile erstellt eine Stammkomponente mit Titel und Rahmen und die dritte Zeile erstellt eine Schaltfläche mit Beschriftung und einem Ereignis-Listener.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Das ZUL-Schema kann von http://www.zkoss.org/2005/zul/zul.xsd heruntergeladen werden.
## Verweise

* [ZUL - Von ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL-Schema](http://www.zkoss.org/2005/zul/zul.xsd)

