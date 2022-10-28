{
  "date" : "2019-10-11",
  "keywords" :[ "ASP", "ASP-Datei", "ASP-Dateiformat", "ASP-Dateityp", "Datei", "Typ", "Was ist eine ASP-Datei"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Active Server Pages-Dateiformat",
  "description" :"Erfahren Sie, was eine ASP-Datei und APIs sind, die sie erstellen und öffnen können.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine ASP-Datei?

ASP steht für Active Server Pages, ein Entwicklungsframework zum Erstellen von Webseiten. Es ermöglicht, dass Computercode von einem internen Server ausgeführt wird, um die Webanforderungen zu bedienen. Wenn ein Webbrowser eine Anfrage für eine ASP-Datei generiert, liest der Server die Datei und führt den darin enthaltenen Code/Skript aus, um das **[HTML](/de/web/html/)**-Ergebnis zu generieren, das an zurückgegeben wird Browser zur Anzeige.

Im Gegensatz zu HTML-Seiten, bei denen es sich um statische Seiten handelt, die vom Server bereitgestellt werden, generieren ASP-Dateien zur Laufzeit dynamische Inhalte, die Anforderungen an Daten aus einer Datenbank beinhalten können. ASP-Seiten verwenden normalerweise die Erweiterung .asp anstelle von .html. Da Code/Skript in einer ASP-Datei auf der Serverseite ausgeführt wird, kann der anfordernde Browser den Code nicht sehen, der zum Erstellen der bereitgestellten Seite verwendet wird. Alle modernen Browser sind in der Lage, als Ergebnis generierte Seiten anzuzeigen. Da sie auf Microsoft-Technologie basieren, werden mit ASP erstellte Seiten auf Microsoft Internet Information Services (IIS)-Servern gehostet.

## Kurze Geschichte des ASP-Dateiformats
ASP hat nur wenige Überarbeitungen durchlaufen, bis es durch ASP.NET ersetzt wurde, das eine modernere und effizientere Methode zum Entwickeln und Verwalten von serverseitigen Seiten darstellt. Unterstützung für ASP ist standardmäßig zusammen mit Internet Information Services (IIS) enthalten. ASP wurde in drei verschiedenen Versionen mit jeweils Verbesserungen veröffentlicht.

* ASP 1.0 wurde im Dezember 1996 als Teil von IIS 3.0 veröffentlicht
* ASP 2.0 wurde im September 1997 als Teil von IIS 4.0 veröffentlicht
* ASP 3.0 wurde im November 2000 als Teil von IIS 5.0 veröffentlicht

## Funktionale ASP-Objekte

ASP-Dateien verwenden serverseitige Objekte, um Benutzeranforderungen zu verarbeiten und Ausgabeseiten zu generieren, die Benutzern bereitgestellt werden. Jedes Objekt verfügt über eine Reihe von Sammlungen, Eigenschaften und Methoden zum Verarbeiten von Anforderungen und Antworten. Zu diesen Objekten gehören:

### Objekt anfordern

Wenn ein Browser eine Seite von einem Server anfordert, wird dies als Anforderung bezeichnet. Das Request-Objekt wird verwendet, um Informationen von einem Besucher zu erhalten.

### Antwortobjekt

Das ASP-Antwortobjekt wird verwendet, um eine Ausgabe vom Server an den Benutzer zu senden.

### Serverobjekt

Das ASP-Serverobjekt wird verwendet, um auf Eigenschaften und Methoden auf dem Server zuzugreifen. Es ermöglicht Verbindungen zu Datenbanken (ADO), Dateisystemen und die Verwendung von Komponenten, die auf dem Server installiert sind.

### Sitzungsobjekt

Ein Sitzungsobjekt ist wie eine Verbindung zwischen dem Browser des Benutzers, der eine Seite vom Server anfordert, und dem Server selbst. Dies wird durch ein von ASP erstelltes und an den Computer des Benutzers gesendetes Cookie erreicht. Das Session-Objekt speichert Informationen über oder Änderungseinstellungen für eine Benutzersitzung. In einem Session-Objekt gespeicherte Informationen werden von allen Seiten einer Anwendung gemeinsam genutzt. Allgemeine Informationen, die in Sitzungsvariablen gespeichert werden, sind Name, ID und Einstellungen. Der Server erstellt für jeden neuen Benutzer ein neues Sitzungsobjekt und zerstört das Sitzungsobjekt, wenn die Sitzung abläuft.

### Anwendungsobjekt

Das Anwendungsobjekt enthält Informationen, die von vielen Seiten in der Anwendung verwendet werden (z. B. Datenbankverbindungsinformationen). Auf die Informationen kann von jeder Seite aus zugegriffen werden. Die Informationen können auch an einer Stelle geändert werden, und die Änderungen werden automatisch auf allen Seiten wiedergegeben. Das Application-Objekt wird verwendet, um Variablen von jeder Seite aus zu speichern und darauf zuzugreifen, genau wie das Session-Objekt.

### ASPError-Objekt

Das ASPError-Objekt wurde in ASP 3.0 implementiert und ist in IIS5 und höher verfügbar. Das ASPError-Objekt wird verwendet, um detaillierte Informationen zu Fehlern anzuzeigen, die in Skripts auf einer ASP-Seite auftreten.

**Hinweis:** Das ASPError-Objekt wird erstellt, wenn Server.GetLastError aufgerufen wird, sodass auf die Fehlerinformationen nur mit der Server.GetLastError-Methode zugegriffen werden kann.

## Verweise

* [ASP - Von W3C] (https://www.w3schools.com/asp/default.asp)
* [Einfache ASP-Seiten erstellen](https://docs.microsoft.com/en-us/ previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

