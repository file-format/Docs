{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER-Datei – ASP.NET-Masterseiten-Dateiformat",
  "description" :"Erfahren Sie mehr über das MASTER-Dateiformat und APIs zum Erstellen und Öffnen von MASTER-Dateien.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Was ist eine MASTER-Datei?

Eine MASTER-Datei ist eine Master-Webseiten-Vorlagendatei, die mit ASP.NET erstellt wurde. Es dient als Ausgangspunkt für die Erstellung mehrerer Seiten, die das gleiche Layout und die gleichen Einstellungen wie die MASTER-Datei haben. Die Vorlagen-MASTER-Datei enthält Einstellungen für Kopfzeile, Navigationsmenüs, Fußzeile, Schriftart und Stilinformationen. Mithilfe einer MASTER-Datei können Sie schnell mehrere Webseiten erstellen.

Sie können eine MASTER-Datei mit Microsoft Visual Studio 2022 und höher öffnen.

## MASTER-Dateiformat – Weitere Informationen

Eine MASTER-Datei wird im HTML-Dateiformat erstellt und gespeichert und ähnelt jeder anderen Webseitendatei. Es ist in bearbeitbare und nicht bearbeitbare Abschnitte unterteilt. Die bearbeitbaren Abschnitte sind diejenigen, die geändert werden können, um den Anforderungen des Benutzers gerecht zu werden. Die nicht bearbeitbaren Abschnitte werden ausgegraut, wenn die MASTER-Datei in Microsoft Visual Studio geöffnet wird.

Masterseiten bestehen aus zwei Teilen, nämlich der Masterseite selbst und einer oder mehreren Inhaltsseiten.

### MASTER-Seite

Die Masterseite hat die Erweiterung .master und wurde in ASP.NET erstellt. Es verfügt über ein vordefiniertes Layout, das statischen Text, HTMLtags und serverseitige Steuerelemente umfasst. In gewöhnlichen ASPX-Seiten wird die @ Page-Direktive verwendet. Im Falle von .master-Dateien wird dies durch die @ Master-Direktive ersetzt.

### Inhaltsseiten

Eine Inhaltsseite stellt den Inhalt für die Platzhaltersteuerelemente der Masterseite dar. Hierbei handelt es sich um ASPX-Seiten, die eigentlich das CodeBehind der Masterseite darstellen. Inhaltsseiten werden mithilfe der @ Page-Direktive gebunden, indem ein MasterPageFile-Attribut eingefügt wird, das auf die zu verwendende Masterseite verweist, wie unten gezeigt.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Verweise

* [Übersicht über ASP.NET-Masterseiten](https://learn.microsoft.com/en-us/ previous-versions/aspnet/wtxbf3hh(v=vs.100))

