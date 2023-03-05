{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Microsoft Access-Berichtsdatei",
  "keywords" :[ "mar", "mar-Datei", "mar-Dateiformat", "was ist ein Zugriffsbericht", "Zugriffsbericht", "Microsoft-Zugriffsbericht"],
  "description":"Erfahren Sie mehr über das Dateiformat Access Report (MAR), das von der Microsoft Access-Software verwendet wird, um eine Verknüpfung oder einen Link zum Microsoft Access-Bericht zu erstellen.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
"identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Was ist der Zugriffsbericht (MAR-Datei)? ##
Eine von Microsoft Access als Verknüpfung des Berichts erstellte Datei wird mit der Dateierweiterung .mar gespeichert. Ein **Microsoft Access-Bericht** bietet eine Möglichkeit, die Informationen in der Microsoft Access-Datenbank zu formatieren, anzuzeigen und zusammenzufassen. Mit diesen Berichten können Sie Ihre Daten in einem präzisen und informativen Layout formatieren, um sie auf dem Bildschirm anzuzeigen oder auszudrucken. Der Bericht zeigt nur die statischen Daten an, was bedeutet, dass wir die Daten in Tabellen beim Anzeigen des Access-Berichts nicht ändern können. Der Bericht zeigt beim Öffnen die neuesten Daten an.

## Microsoft Access Report (MAR)-Dateiformat

Das MAR-Dateiformat wird von der Microsoft Access-Software verwendet, um eine Verknüpfung oder einen Link zum Microsoft Access-Bericht zu erstellen, bei dem es sich um ein Datenbankobjekt handelt, das nützlich ist, wenn Sie die Informationen in Ihrer Datenbank für eine der folgenden Verwendungen präsentieren müssen:

- Anzeige einer Zusammenfassung der Daten.
- Schnappschüsse der Daten archivieren.
- Details zu einzelnen Datensätzen anzeigen.
- Etiketten erstellen.

## Teile des Zugriffsberichts
Das Design eines Access-Berichts ist in verschiedene Abschnitte unterteilt, die in der Designansicht angezeigt werden können. Die folgende Tabelle erklärt, wie jeder Abschnitt funktioniert und Ihnen beim Erstellen von Berichten helfen kann.
| Abschnitt | Wie der Abschnitt beim Drucken angezeigt wird | Wo der Abschnitt verwendet werden kann |
---------|----|------|
| Berichtskopf | Zu Beginn des Berichts. | Verwenden Sie die Kopfzeile des Berichts für Informationen, die normalerweise auf einem Deckblatt erscheinen, wie z. B. ein Logo, ein Titel oder ein Datum. Wenn Sie ein berechnetes Steuerelement, das die Aggregatfunktion Sum verwendet, in den Berichtskopf einfügen, gilt die berechnete Summe für den gesamten Bericht. Der Berichtskopf wird vor dem Seitenkopf gedruckt. |
| Seitenkopfzeile | Oben auf jeder Seite. | Verwenden Sie einen Seitenkopf, um den Berichtstitel auf jeder Seite zu wiederholen. |
| Gruppenkopf | Am Anfang jeder neuen Gruppe von Datensätzen. | Verwenden Sie die Gruppenkopfzeile, um den Gruppennamen auszudrucken. Verwenden Sie beispielsweise in einem nach Produkt gruppierten Bericht die Gruppenkopfzeile, um den Produktnamen zu drucken. Wenn Sie ein berechnetes Steuerelement platzieren, das die Sum-Aggregatfunktion im Gruppenkopf verwendet, gilt die Summe für die aktuelle Gruppe. Sie können mehrere Gruppenkopfabschnitte in einem Bericht haben, je nachdem, wie viele Gruppierungsebenen Sie hinzugefügt haben. Weitere Informationen zum Erstellen von Gruppenkopf- und -fußzeilen finden Sie im Abschnitt Hinzufügen von Gruppierungen, Sortierungen oder Summen. |
| Einzelheit | Erscheint einmal für jede Zeile in der Datensatzquelle. | Hier platzieren Sie die Steuerelemente, die den Hauptteil des Berichts bilden. |
| Gruppenfuß | Am Ende jeder Datensatzgruppe. | Verwenden Sie eine Gruppenfußzeile, um zusammenfassende Informationen für eine Gruppe zu drucken. Sie können mehrere Gruppenfußzeilenabschnitte in einem Bericht haben, je nachdem, wie viele Gruppierungsebenen Sie hinzugefügt haben. |
| Seitenfuß | Am Ende jeder Seite. | Verwenden Sie eine Seitenfußzeile, um Seitenzahlen oder Informationen pro Seite zu drucken. |
| Berichtsfuß | Am Ende des Berichts. Hinweis: In der Entwurfsansicht wird der Berichtsfuß unterhalb des Seitenfußes angezeigt. In allen anderen Ansichten (z. B. Layoutansicht oder wenn der Bericht gedruckt oder in der Vorschau angezeigt wird) wird der Berichtsfuß jedoch über dem Seitenfuß angezeigt, direkt nach dem letzten Gruppenfuß oder der Detailzeile auf der letzten Seite. | Verwenden Sie die Berichtsfußzeile, um Berichtssummen oder andere zusammenfassende Informationen für den gesamten Bericht zu drucken. |






## Verweise ##

- [Einführung in Berichte in Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Entwerfen von Berichten in Access](https://www.uis.edu/informationtechnologyservices/wp-content/uploads/sites/106/2013/04/DesigningReportsinAccess2010.pdf)

