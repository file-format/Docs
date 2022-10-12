{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE-Datei - HTML5-Cache-Manifestdateiformat",
  "description" :"Erfahren Sie, was eine APPCACHE-Datei und APIs sind, die APPCACHE-Dateien erstellen und öffnen können.",
  "linktitle" :"APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Was ist eine APPCACHE-Datei?

Eine APPCACHE-Datei ist eine Textdatei, die die Liste der Ressourcen enthält, die von Browsern für den Offline-Zugriff auf die Webanwendungen zwischengespeichert werden sollen. Dies ist nützlich, wenn keine Internetverbindung besteht. In einer solchen Situation verwendet der Browser die Offline-Cache-Ressourcen, um Zugriff auf die Webinhalte bereitzustellen. Die APPCACHE-Datei enthält Webressourcen wie Bilder (z. B. **[PNG](/de/image/png/)**, **[WEBP](/de/image/webp/)** usw.), Stylesheets **([ CSS])(/de/web/css/)** und Skriptdateien (z. B. Javascript-Dateien **[JS](/de/web/js/)**).

Zu den Anwendungen, die **APPCACHE-Dateien öffnen können**, gehören Webbrowser wie Google Chrome, Safari und Firefox.

## APPCACHE-Dateiformat - Weitere Informationen

APPCACHE-Dateien sind einfache Textdateien, die Offline-Zugriff auf Webseiten bieten, die ohne Internetverbindung ausgeführt werden können. Das Vorhandensein von APPCACHE kennzeichnet eine Seite als offline verfügbar.

### Wie verweise ich auf eine APPCACHE-Datei?

Auf Ihrer HTML-Seite wird wie folgt auf eine APPCACHE-Datei verwiesen.

```
<html manifest="example.appcache">
  ...
</html>
```

## Struktur einer APPCACHE-Manifestdatei

Eine einfache APPCACHE-Manifestdatei sieht wie folgt aus.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Dies ist ein einfachstes Beispiel, und es können auch komplexere Strukturen vorhanden sein.

## Vorteile des APPCACHE-Manifests

Die Verwendung der Cache-Schnittstelle bietet Webanwendungen die folgenden Vorteile.

1. Offline-Browsing – Die Cache-Oberfläche ermöglicht Endbenutzern, Ihre gesamte Website zu durchsuchen, wenn sie offline sind
1. Geschwindigkeit – Cache ermöglicht Hochgeschwindigkeitszugriff auf Offline-Inhalte direkt von der Disc
1. Ständige Zugänglichkeit – Falls Ihre Website ausfällt, haben Benutzer weiterhin Zugriff auf die Webinhalte und können die Offline-Erfahrung nutzen

## Verweise

* [Ein Leitfaden für Anfänger zum AppCache-Manifest](https://web.dev/appcache-beginner/)

