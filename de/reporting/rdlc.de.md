{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDLC - Berichtsdefinitionssprache clientseitig",
  "keywords" :[ "rdlc", "Berichtsdefinitionssprache", "mkv-Format", "XSD", "Berichtsdefinitionssprache clientseitig"],
  "description":"Erfahren Sie mehr über das RDLC-Dateiformat, das eine XML-Darstellung einer SQL Server Reporting Services-Berichtsdefinition ist.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Was ist eine RDLC-Datei? ##

RDLC steht für Report Definition Language Client-Seite. Tatsächlich handelt es sich um eine Erweiterung der Berichtsdatei, die mithilfe der Microsoft-Berichtstechnologie erstellt wurde. Die SQL Server 2005-Version von Report Designer wird verwendet, um diese Dateien zu erstellen. Das **ReportViewer**-Steuerelement auf der Clientseite kann die RDLC-Berichte direkt ausführen.

## RDL VS RDLC-Dateien
|.rdl-Dateien |.rdlc-Dateien|
---|---|
|RDL-Dateien werden von der SQL Server 2005-Version von Report Designer erstellt|RDLC-Dateien werden von der Visual Studio 2005-Version von Report Designer erstellt|
|Es wird in SQL Server Reporting Services verwendet|Es wird in Visual Studio verwendet|
|Es ist ein entfernter Bericht|Es ist ein lokaler Bericht|
|Zur Ausführung wird eine Reporting Services-Instanz benötigt|Keine Reporting Services-Instanz erforderlich|

## Client-Berichtsdefinitionsdateien (.rdlc) erstellen
Das ReportViewer-Steuerelement wird verwendet, um Client-Berichtsdefinitionsdateien (.rdlc) mithilfe der integrierten Verarbeitungsfunktion des Steuerelements auszuführen. Die Client-Berichte, die Sie im lokalen Verarbeitungsmodus ausführen, können einfach in Ihrem Anwendungsprojekt erstellt werden. Im Folgenden sind die Ansätze zum Erstellen des Berichts aufgeführt:

- Verwenden Sie den **Berichtsassistenten**, um eine neue Client-Berichtsdefinition (.rdlc) zu erstellen.

– Erstellen Sie mithilfe von Visual Studio eine neue Clientberichtsdefinitionsdatei (RDLC).

- Generieren Sie programmgesteuert eine Berichtsdefinition.


Sie können einen Bericht nur in der Vorschau anzeigen, indem Sie ihn in einem **ReportViewer**-Steuerelement ausführen. Bitte beachten Sie, dass Sie die Berichtsdefinition jederzeit öffnen und bearbeiten und dann die Anwendung erstellen oder bereitstellen können, um die Ergebnisse zu überprüfen.

## Verweise ##

- [Erstellen von Client-Berichtsdefinitionsdateien (.rdlc)](https://docs.microsoft.com/en-us/ previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))

