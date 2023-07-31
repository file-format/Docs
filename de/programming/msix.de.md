{
  "date" : "2021-04-22",
"Schlüsselwörter": [ "msix-Datei", "Erweiterung", "Format", "wie man eine msix-Datei öffnet", "msix-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Was ist eine MSIX-Datei?",
  "description":"Erfahren Sie mehr über MSIX-Dateien und APIs, die MSIX-Dateien erstellen und öffnen können.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Was ist eine MSIX-Datei?

Eine MSIX-Datei ist ein Windows-App-Paketformat, das zum Erstellen und Verteilen von Anwendungen in Windows 10 verwendet wird. Dies ist das moderne Paketdateiformat im Vergleich zu [APPX](/de/programming/appx/) und MSI, die endgültig eingestellt werden in dieses neue Dateiformat. Es kann für die Bereitstellung von Win32-, WPF- und Windows Forms-Apps verwendet werden. MSIX-Dateien sind zuverlässig und zielen auf die Optimierung von Netzwerk und Speicherplatz ab. Entwickler verwenden diese, um Programme über den Microsoft Store (früher bekannt als Windows Store) an Endbenutzer zu verteilen.

## MSIX-Dateiformat – Weitere Informationen

MSIX-Dateien sind [ZIP](/de/compression/zip/)-komprimiert, wobei alle Dateien in der gepackten Datei enthalten sind. Zusätzlich zu den App-bezogenen Dateien enthält die MSIX-Datei [.xml](/de/web/xml/)-Konfigurationsdateien, die Informationen zur App-Installation enthalten.

## Was ist in einem MSIX-Paket enthalten?

Ein MSIX-Paket besteht aus den folgenden Dateien.

* `AppxBlockMap.xml` - Bekannt als Paketblockzuordnungsdatei, ist es ein XML-Dokument, das eine Liste von App-Dateien mit Indizes und kryptografischen Hashes für jeden Datenblock enthält, der im Paket gespeichert ist.
* „AppxManifest.xml“ – Ein XML-Dokument, das die Informationen enthält, die für die Bereitstellung, Anzeige und Aktualisierung einer MSIX-App erforderlich sind. Diese Informationen umfassen Paketidentität, Paketabhängigkeiten, erforderliche Funktionen, visuelle Elemente und Erweiterbarkeitspunkte.
* „AppxSignature.p7x“ – Eine Datei, die generiert wird, wenn das Paket signiert wird. Alle MSIX-Pakete müssen vor der Installation signiert werden. Mit der AppxBlockmap.xml kann die Plattform das Paket installieren und validiert werden.

## Verweise

* [MSIX-Übersicht](https://learn.microsoft.com/en-us/windows/msix/overview)
* [APPX-Dateien mit Microsoft Visual Studio erstellen](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

