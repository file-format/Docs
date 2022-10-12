{
  "date" : "2021-04-22",
"Schlüsselwörter": [ "AppX-Datei", "Erweiterung", "Format", "So öffnen Sie eine AppX-Datei", "AppX-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Was ist eine APPX-Datei?",
  "description":"Erfahren Sie mehr über das APPX-Dateiformat und APIs, die APPX-Dateien erstellen und öffnen können.",
  "linktitle" :"APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Was ist eine APPX-Datei?

Eine APPX-Datei ist ein verteilbares Paketdateiformat, das für die Verteilung und Installation einer Anwendung verwendet wird. Es wurde mit Windows 8 eingeführt, um im Microsoft Windows Store veröffentlicht zu werden. Es enthält alle Dateien, die zum Installieren einer Windows-Anwendung erforderlich sind. Dazu gehören Metadaten, Dateien und Informationen zu Anmeldeinformationen. Ein moderneres Verpackungsdateiformat ist MSIX, das derzeit häufiger verwendet wird als APPX.

## APPX-Dateiformat - Weitere Informationen

APPX-Dateien werden als komprimierte Dateien im Dateiformat [ZIP](/de/compression/zip/) gespeichert. Dadurch wird das gesamte Paket zu einer Archivdatei mit reduzierter Dateigröße, die einfach in den Microsoft Store hochgeladen werden kann.

## Wie werden Dateien in einer APPX-Datei angezeigt?

Um den Inhalt oder die Dateien in einer APPX-Datei anzuzeigen, sollten die folgenden Schritte befolgt werden.

1. Da APPX-Dateien als komprimierte ZIP-Dateien gespeichert werden, benennen Sie die Datei in die Erweiterung .zip um
1. Verwenden Sie ein beliebiges Dekomprimierungstool wie 7-Zip, WinZip oder WinRAR, um die in der APPX-Datei enthaltenen Dateien zu extrahieren

## Wie erstelle ich eine APPX-Datei?

Es gibt zwei Methoden, die zum Erstellen von APPX-Dateien verwendet werden können.

1. Verwenden von MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) wird verwendet, um beide zu erstellen App-Pakete (.msix oder .appx) und App-Paket-Bundle-Dateien (.msixbundle oder .appxbundle). Darüber hinaus kann es Dateien aus einem App-Paket extrahieren. MakeApp.exe ist mit dem Windows 10 SDK verfügbar und kann über die Eingabeaufforderung verwendet werden.
1. Verwenden von Microsoft Visual Studio – Entwickler [erstellen APPX-Dateien] (https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) normalerweise mit Microsoft Visual Studio. Sobald die Anwendungsentwicklung abgeschlossen ist und die App zur Veröffentlichung bereit ist, kann die APPX-Paketdatei erstellt werden, indem sie in Visual Studio veröffentlicht wird.

## Verweise

* [Erstellen Sie ein MSIX-Paket oder -Bundle mit MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [APPX-Dateien mit Microsoft Visual Studio erstellen](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

