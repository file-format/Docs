{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS – Lidar LASer-Dateiformat",
  "description":"Erfahren Sie mehr über das LAS-Dateiformat und die APIs, mit denen LAS-Dateien erstellt und geöffnet werden können.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Was ist eine LAS-Datei?

Das LAS-Dateiformat (Lidar LASer) ist ein Binärdateiformat, das speziell für die Speicherung von LIDAR-Punktwolkendaten entwickelt wurde. Es wurde von der American Society for Photogrammetry and Remote Sensing (ASPRS) als standardisiertes Format für den Austausch und die Interoperabilität von LIDAR-Daten entwickelt und wird gepflegt.

LAS-Dateien speichern detaillierte Informationen zu einzelnen LIDAR-Punkten, einschließlich ihrer 3D-Koordinaten (x, y und z), Intensitätswerte, Klassifizierungscodes und zusätzlicher Attribute. Das Format unterstützt sowohl diskrete Return- als auch vollständige Wellenform-Lidar-Daten und ermöglicht die Speicherung mehrerer Returns pro Laserimpuls.

## LAS-Dateiformat

Die Struktur einer LAS-Datei besteht aus drei Hauptabschnitten: dem Dateikopf, den Datensätzen variabler Länge (VLRs) und den Punktdatensätzen.

1. Dateikopf: Der Dateikopf enthält wichtige Informationen zur LAS-Datei, wie z. B. die Datenformatversion, das Punktdatenformat, die Anzahl der Punkte, die Koordinaten des Begrenzungsrahmens, das Koordinatenreferenzsystem (CRS) und andere Metadaten. Es bietet eine Zusammenfassung der in der Datei enthaltenen LIDAR-Daten.

2. Datensätze variabler Länge (VLRs): VLRs sind optional und können zusätzliche Metadaten und benutzerdefinierte Informationen zu den LIDAR-Daten speichern. VLRs ermöglichen eine flexible Erweiterung des Formats, um spezifischen Benutzeranforderungen gerecht zu werden. Beispiele für VLRs sind Informationen über das Sensorsystem, Datenverarbeitungsparameter oder Klassifizierungsschemata.

3. Punktdatensätze: Die Punktdatensätze speichern die tatsächlichen LIDAR-Messungen. Jeder Punktdatensatz stellt einen einzelnen LIDAR-Punkt dar und enthält Attribute wie X-, Y- und Z-Koordinaten, Intensitätswerte, Klassifizierungscodes (z. B. Boden, Vegetation, Gebäude) und andere benutzerdefinierte Attribute. In den Punktdatensätzen können auch Zeitstempel, Rückgabewerte und Scanwinkel gespeichert werden.

LAS-Dateien unterstützen verschiedene Datenformate (0 bis 10), um verschiedene Arten von LIDAR-Daten und die erforderliche Informationsebene zu berücksichtigen. Beispielsweise stellt Format 0 ein einfaches Punktformat mit grundlegenden Informationen dar, während die Formate 1 bis 3 umfassendere Daten einschließlich Wellenforminformationen für jede Rückgabe bereitstellen.

LAS-Dateien werden von LIDAR-Software und -Verarbeitungstools weitgehend unterstützt, was sie zu einem Standardformat für den Austausch und die Analyse von LIDAR-Daten macht. Darüber hinaus können LAS-Dateien mithilfe verlustfreier Komprimierungstechniken komprimiert werden, um die Dateigröße zu reduzieren und gleichzeitig die ursprüngliche Datentreue beizubehalten. Die komprimierte Version von LAS-Dateien wird oft als LAZ bezeichnet und bietet effiziente Speicher- und Datenübertragungsfunktionen.

## Verweise

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
