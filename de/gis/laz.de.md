{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ – Komprimierte LIDAR-Datenaustauschdatei",
  "description":"Erfahren Sie mehr über das LAZ-Dateiformat und die APIs, mit denen LAZ-Dateien erstellt und geöffnet werden können.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Was ist eine LAZ-Datei?

Das LAZ-Dateiformat ist eine komprimierte Version des LAS-Dateiformats (Lidar LASer), das speziell für die Speicherung von Lidar-Punktwolkendaten entwickelt wurde. LAZ-Dateien behalten die gleichen Daten und die gleiche Struktur wie LAS-Dateien bei, verwenden jedoch verlustfreie Komprimierungstechniken, um die Dateigröße zu reduzieren und gleichzeitig die ursprüngliche Datentreue zu bewahren.

## LAZ-Dateiformat – Kurze Geschichte

Das LAZ-Dateiformat wurde entwickelt, um der wachsenden Nachfrage nach effizienter Speicherung und Übertragung großer LIDAR-Datensätze gerecht zu werden. Durch die Komprimierung von LAS-Dateien reduzieren LAZ-Dateien ihre Größe erheblich, wodurch sie einfacher zu verwalten und zu übertragen sind. Die Komprimierung wird durch die Verwendung einer Kombination verschiedener Algorithmen wie Entropiekodierung und Kodierung mit variabler Länge erreicht, um LIDAR-Punktattribute in einer kompakteren Form darzustellen.

## LAZ-Dateiformat

Trotz der Komprimierung behalten LAZ-Dateien die Möglichkeit, die ursprünglichen LAS-Daten ohne Informationsverlust vollständig wiederherzustellen. Dies bedeutet, dass eine einmal dekomprimierte LAZ-Datei auf die gleiche Weise wie eine unkomprimierte LAS-Datei verarbeitet und analysiert werden kann. Der Komprimierungs- und Dekomprimierungsprozess wird normalerweise mit spezieller Software oder Bibliotheken durchgeführt, die das LAZ-Format unterstützen.

Das LAZ-Dateiformat gewährleistet die Kompatibilität mit LAS-Dateien und gewährleistet so die Interoperabilität zwischen Lidar-Software und Verarbeitungstools. Dies bedeutet, dass Anwendungen, die LAS-Dateien lesen und verarbeiten können, LAZ-Dateien normalerweise ohne Änderungen verarbeiten können. Darüber hinaus enthalten LAZ-Dateien weiterhin den Dateiheader, Datensätze variabler Länge (VLRs) und Punktdatensätze, wodurch die gleiche Struktur wie bei LAS-Dateien erhalten bleibt.

## Vorteile des LAZ-Dateiformats

**Reduzierte Dateigröße:** Durch die LAZ-Komprimierung wird die Dateigröße von LIDAR-Datensätzen erheblich reduziert, wodurch diese besser verwaltbar und einfacher zu speichern und zu übertragen sind.

**Datenintegrität:** Die LAZ-Komprimierung ist verlustfrei, was bedeutet, dass die dekomprimierten Daten eine exakte Kopie der ursprünglichen LAS-Daten sind, sodass kein Informations- oder Präzisionsverlust entsteht.

**Interoperabilität:** LAZ-Dateien sind mit LAS-Dateien kompatibel und ermöglichen eine nahtlose Integration in vorhandene LIDAR-Software und -Workflows.

**Effiziente Verarbeitung:** Aufgrund ihrer reduzierten Größe können LAZ-Dateien schneller geladen und verarbeitet werden, was die Gesamtverarbeitungs- und Analysezeiten verkürzt.

Das LAZ-Dateiformat hat sich in der Lidar-Community als Standard für die Speicherung und den Austausch komprimierter Lidar-Daten durchgesetzt. Es bietet ein Gleichgewicht zwischen effizienter Datenkomprimierung und Datenintegrität und ermöglicht so eine einfachere Handhabung großer LIDAR-Datensätze bei gleichzeitiger Beibehaltung der Genauigkeit und Qualität der Originaldaten.

## Verweise

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
