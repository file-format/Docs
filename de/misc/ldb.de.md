{
"Datum": "20.04.2023",
  "keywords": [
"LDB-Datei",
"Was ist eine LDB-Datei",
"Welche Informationen enthält LDB",
"Was ist der Zweck der LDB-Datei",
"LDB-Erweiterung",
"Datei",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "LDB-Dateiformat – Microsoft Access-Sperrdatei",
  "description":"Erfahren Sie mehr über das LDB-Format und welche Informationen es enthält.",
"linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
"parent": "misc"
}
},
"lastmod": "20.04.2023"
}

## Was ist eine LDB-Datei?

Eine LDB-Datei ist eine Sperrdatei, die von Microsoft Access verwendet wird, um zu verhindern, dass mehrere Benutzer gleichzeitig dieselbe Datenbank bearbeiten. Wenn der Benutzer eine Access-Datenbank öffnet, erstellt Access eine entsprechende LDB-Datei im selben Verzeichnis wie die Datenbank. Diese Datei enthält Informationen darüber, wer derzeit die Datenbank verwendet und welche Datensätze sie bearbeiten.

Die LDB-Datei wird von Microsoft Access beim Öffnen der Datenbank automatisch erstellt und beim Schließen der Datenbank gelöscht. Es ist wichtig zu beachten, dass die LDB-Datei niemals manuell gelöscht werden sollte, da dies zu Problemen mit der Datenbank führen kann.

Wenn Probleme mit der Microsoft Access-Datenbank auftreten, besteht eine mögliche Lösung darin, die mit dieser Datenbank verknüpfte LDB-Datei zu löschen. Dadurch werden alle Sperren aufgehoben, die Sie möglicherweise am Zugriff auf die Datenbank hindern. Erstellen Sie jedoch unbedingt eine Sicherungskopie der Datenbank, bevor Sie dies versuchen, da das Löschen der LDB-Datei bei unsachgemäßer Vorgehensweise zu Datenverlust oder -beschädigung führen kann.

## LDB-Dateiformat – Weitere Informationen

Eine LDB-Datei in Microsoft Access enthält Informationen über Benutzer, die derzeit auf die Datenbank zugreifen, wie beispielsweise deren Benutzername, Computername und Anmeldezeit. Die LDB-Datei enthält auch Informationen über alle Sperren, die für die Datenbank gesetzt wurden, beispielsweise welche Datensätze von welchem Benutzer bearbeitet werden.

Hier ist eine detailliertere Liste der Arten von Informationen, die in einer LDB-Datei gefunden werden können:

- **Benutzername** – der Name des Benutzers, der gerade auf die Datenbank zugreift
- **Computername** – der Name des Computers, von dem aus der Benutzer auf die Datenbank zugreift
- **Anmeldezeit** – die Zeit, zu der der Benutzer die Datenbank zum ersten Mal geöffnet hat
- **Datensatzsperren** – Informationen darüber, welche Datensätze gerade von welchem Benutzer bearbeitet werden
- **Objektsperren** – Informationen darüber, welche Datenbankobjekte (z. B. Tabellen, Formulare oder Berichte) gerade von welchem Benutzer bearbeitet werden
- **Verbindungsinformationen** – Informationen darüber, wie der Benutzer mit der Datenbank verbunden ist (z. B. ob er eine lokale Verbindung oder eine Netzwerkverbindung verwendet)

Die Informationen in der LDB-Datei werden von Microsoft Access verwendet, um zu verhindern, dass mehrere Benutzer gleichzeitig widersprüchliche Änderungen an derselben Datenbank vornehmen. Wenn ein Benutzer versucht, einen Datensatz oder ein Objekt zu bearbeiten, das bereits von einem anderen Benutzer gesperrt ist, zeigt Microsoft Access eine Meldung an, die darauf hinweist, dass das Objekt bereits verwendet wird. Die LDB-Datei wird aktualisiert, wenn Benutzer die Datenbank öffnen und schließen und Änderungen an gesperrten Objekten vornehmen.

## Verweise
* [Was ist eine LDB-Datei?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

