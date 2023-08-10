{
  "date" : "2021-09-06",
  "keywords" :[ "dacpac", "extension", "file", "file format", "Database File Type", "Database File Format", "Data Tier Application Package" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das DACPAC-Dateiformat und APIs, die DACPAC-Dateien erstellen und öffnen können.",
  "title" :"DACPAC - Datenschicht-Anwendungspaket",
  "linktitle" : "DACPAC",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Was ist eine DACPAC-Datei?

Eine Datei mit der Erweiterung .dacpac (steht für Data Tier Application Package) ist eine Datenbankdatei, die mit Microsoft SQL Server Data Tier Application erstellt wurde und das Datenbankmodell zur Darstellung von Datenbankobjekten enthält. Da es das vollständige Modell der Datenbank enthält, wird es verwendet, um eine Datenbank aus den im Modell verfügbaren Details wiederherzustellen. DACPAC-Dateien werden normalerweise an Bereitstellungsteams zur Installation beim Kunden übergeben, um die Datenbank wiederherzustellen. Diese können mit geöffnet werden
[Microsoft SQL Server 2019](https://www.microsoft.com/en-us/sql-server/sql-server-2019).

## DACPAC-Dateiformat - Weitere Informationen

Die DACPAC-Datenpaketdateien sind eigentlich komprimierte ZIP-Dateien, die mehrere [XML](/de/web/xml/)-Dateien enthalten, die Informationen über das Datenbankmodell enthalten, wie z. B. Tabellen und Ansichten, die zum Wiederherstellen einer Datenbank verwendet werden. Um den Inhalt von DACPAC-Dateien anzuzeigen, benennen Sie die Dateien von .dacpac in [.zip](/de/compression/zip/) um und extrahieren Sie das Zip-Archiv mit einem beliebigen Dekomprimierungsprogramm.

Im Folgenden sind einige Dateien aufgeführt, die sich in einer DACPAC-Datei befinden.

* [Content_Types].xml
```
<?xml version="1.0" encoding="utf-8"?>
<Types
xmlns="http://schemas.openxmlformats.org/package/2006/content-types">
<Default Extension="xml" ContentType="text/xml" />
</Types>
```
* DacMetadata.xml

```
<?xml version="1.0" encoding="utf-8"?>
<DacType xmlns="http://schemas.microsoft.com/sqlserver/dac/Serialization/2012/02">
<Name>CRM</Name>
<Version>1.0.0.0</Version>
</DacType>
```
* Origin.xml

* model.xml

Es ist anzumerken, dass DACPAC keine DATA und andere Objekte auf Serverebene enthält. Die Datei kann alle Objekttypen enthalten, die im SSDT-Projekt aufbewahrt werden können.

## Verweise

* [Anwendungen auf Datenebene – Vorteile](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/data-tier-applications)
* [Bereitstellen einer Datenebenenanwendung – Microsoft](https://learn.microsoft.com/en-us/sql/relational-databases/data-tier-applications/deploy-a-data-tier-application)
* [Wie erstelle ich eine DACPAC-Datei?](https://azureplayer.net/2018/10/how-to-create-dacpac-file/)

