{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX-Datei - HTML-Erweiterungsdateiformat",
  "description" :"Ihr Dateiformatleitfaden, um zu erfahren, was eine HTX-Datei und APIs sind, die HTX-Dateien erstellen und öffnen können.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine HTX-Datei?

Eine HTX-Datei ist eigentlich eine HTML-Datei, die Datenvariablen zum Anzeigen der Datenbankabfrageergebnisse als Webseite enthält. HTX-Dateien werden hauptsächlich mit der Microsoft FrontPage-Webentwicklungssoftware erstellt und im selben Ordner wie die entsprechende Internet Database Connector-Datei (.IDC) gespeichert.

HTX-Dateien können mit Anwendungen wie Microsoft FrontPage und jedem Texteditor wie Notepad, TextEdit oder Atom geöffnet werden.

## HTX-Dateiformat

HTX-Dateien werden als reine Textdatei mit Code zum Abrufen von Daten aus einer Datenbank und zum Speichern in Variablen zur Anzeige gespeichert.


### Beispiel für eine HTX-Datei

Ein Beispiel für eine HTX-Datei ist wie folgt, die einen Seitenkopf zum Anzeigen der Abfragebeschränkung und der auf der Seite angezeigten Dokumente zum Anzeigen für den Benutzer definiert.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Die Ausgabe dieses Beispielcodes lautet wie folgt.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Wie zu sehen ist, ist die HTX-Datei eine Vorlage, die formatiert, wie Ergebnisse zurückgegeben und den Endbenutzern angezeigt werden. Es ist im HTML-Format mit einigen IIS-Erweiterungen und dem Indexdienst geschrieben. Diese Erweiterungen umfassen Variablennamen und andere Codes für die Verarbeitung von Ergebnissen.

## Verweise

* [Formatierung der Ergebnisse in .Htx-Datei](https://learn.microsoft.com/en-us/ previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

