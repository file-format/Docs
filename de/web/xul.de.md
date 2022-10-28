{
  "date" : "2021-05-24",
  "keywords" :["xul", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "XML User Interface Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - Sprachdatei der XML-Benutzeroberfläche",
  "description":"Erfahren Sie mehr über das XUL-Dateiformat und APIs, die XUL-Dateien erstellen und öffnen können.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Was ist eine XUL-Datei?

Eine Datei mit der Erweiterung .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) steht für XML User Interface Language) ist eine auf [XML](/de/web/xml/) basierende Auszeichnungssprachendatei für Erstellen von Benutzeroberflächen. Es wurde von Mozilla für Entwickler entwickelt, um grafische Benutzeroberflächenelemente zu erstellen, die anderen Auszeichnungssprachen ähneln, die zum Erstellen von Webseiten verwendet werden. XUL wurde von Mozilla in seinem Firefox-Browser weit verbreitet, wo es die Mozilla-Codebasis verwendete. Das XUL-Rendering wird mit dem durchgeführt
[Gecko-Engine](https://en.wikipedia.org/wiki/Gecko_(software)). Firefox-Forks wie Pale Moon, Basilisk und Waterfox unterstützen weiterhin XUL-Add-Ons. XUL-Dateien werden mit dem MIME-Typ identifiziert: application/vnd.mozilla.xul+xml.

## XUL-Dateiformat

XUL-Dateien werden basierend auf dem XML-Dateiformat im Klartext geschrieben und mit der Gecko-Engine gerendert. Die drei Hauptbestandteile einer XUL-Struktur sind:

* `Content` - Dies beinhaltet die Deklarationen des Fensters und der darin enthaltenen Elemente der Benutzeroberfläche.
* `Skin` - Enthält alle Stylesheets, Bilder und andere themenbezogene Dateien. Das Aussehen eines Fensters wird in den Stylesheets beschrieben.
* „Gebietsschema“ – Text, der in einem Fenster angezeigt wird, wird separat gespeichert und mehrere Sätze von Sprachdateien können von Benutzern verwendet werden.

### XUL-Beispiel

Im folgenden Beispiel werden drei Schaltflächen erstellt, die in vertikaler Richtung übereinander gestapelt werden.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Verweise

* [XUL – Von Wikipedia](https://en.wikipedia.org/wiki/XUL)
* [XUL Archivierte Dokumentation – Von Mozilla](https://wiki.mozilla.org/XUL:Home_Page)

