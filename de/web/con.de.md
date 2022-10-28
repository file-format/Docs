{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON-Datei - Quelldateiformat der Konzeptanwendung",
  "description" :"Erfahren Sie, was eine CON-Datei und APIs sind, die CON-Dateien erstellen und öffnen können.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
"identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## Was ist eine CON-Datei?

Eine CON-Datei ist eine Quellcodedatei für Anwendungen, die für den **Concept Application Server** entwickelt wurden. Es wird zum Schreiben von Anwendungen für den Datenaustausch zwischen dem Server und dem Benutzer verwendet. Auf dem Server gehostete CON-Dateien sind mit einem Webbrowser zugänglich, sofern der Concept Client auf Benutzerseite installiert ist. Concept Application Server ist ein Webserver mit einer kleinen Programmiersprache, die möglicherweise eine [SQL](/de/database/sql/)-Subset-Datenbank-Engine (TinDB) hat.

CON-Dateien können mit RadGs Concept Application Server geöffnet/ausgeführt werden.

## CON-Dateiformat - Weitere Informationen

CON-Dateien werden auf dem Server gehostet und der Zugriff erfolgt über einen Webbrowser auf dem Benutzercomputer. Concept [URLs](/de/web/url/) unterscheiden sich von normalen HTTP-URLs und beginnen mit **concept://**.

### CON-Datei-URL-Beispiel

Auf eine auf dem Concept Application Server gehostete CON-Datei kann über einen Webbrowser unter Verwendung von URLs zugegriffen werden, wie z. B.:

```
concept://domain.server.com/web_application/main.con.
```
## Verweise

* [Konzeptanwendungsserver](https://github.com/Devronium/ConceptApplicationServer)

