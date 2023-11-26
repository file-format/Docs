{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AXD-Datei – ASP.NET Web-Handler-Dateiformat",
  "description" :"Erfahren Sie, was eine AXD-Datei ist und welche APIs es gibt, mit denen AXD-Dateien erstellt und geöffnet werden können.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## Was ist eine AXD-Datei?

Eine AXD-Datei ist eine Webeinstellungsdatei, die zum Verarbeiten und Abrufen eingebetteter Ressourcenanforderungen in ASP.NET verwendet wird. Es enthält Anweisungen zum Abrufen eingebetteter Ressourcen wie Bilder, JavaScript-Dateien ([.JS](/web/js/)) und [.CSS](/web/css/)-Dateien. AXD-Dateien werden zum Einfügen von Ressourcen in clientseitige Seiten verwendet. Dadurch können Clientseiten auf standardmäßige Weise auf diese Ressourcen auf dem Server zugreifen.

## AXD-Dateiformat

AXD-Dateien werden serverseitig als Binärdateien gespeichert. Es bezieht sich auf eine Web-Handler-Datei in ASP.NET, bei der es sich um Komponenten handelt, die Antworten auf bestimmte Anforderungen an einen Webserver generieren. AXD-Dateien führen eine benutzerdefinierte Verarbeitung durch, bevor sie die Antwort basierend auf clientseitigen Seitenanforderungen generieren. Diese werden normalerweise als **WebResource.axd**-Dateien gespeichert.

### Was ist die Datei WebResource.axd?

Die meisten ASP.NET-Projekte speichern AXD-Dateien als WebResource.axd-Dateien, die es clientseitigen Seiten ermöglichen, Ressourcen herunterzuladen, die in eine Assembly eingebettet sind. Wenn Sie Ihre Anwendung im Debugmodus ausführen, kann es zu einer langsamen Leistung kommen, da der WebResources.axd-Handler nicht zwischengespeichert wird.

## Verweise

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

