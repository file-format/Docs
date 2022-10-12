{
  "date" : "2021-06-30",
  "keywords" :[ "msi-Datei", "MSI-Dateiformat", "was ist eine msi-Datei", "Datei", "msi-Beispiel", "msi-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das MSI-Dateiformat und APIs, die MSI-Dateien erstellen und öffnen können.",
  "title" :"MSI - Windows Installer-Paketdatei",
  "linktitle" :"MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Was ist eine MSI-Datei?
Eine MSI-Datei, die zum Installieren und Starten von Windows-Programmen verwendet wird; ein vollständiges Paket für Microsoft Windows, das Installationsinformationen für ein typisches Softwareprogramm enthält, einschließlich wesentlicher zu installierender Dateien und Informationen zum Installationsort. Die MSI-Dateien können auch das Paket für Software-Updates enthalten. MSI-Dateien ähneln [EXE](/de/executable/exe/), aber EXE kann manchmal keine Installationsinformationen enthalten und das Softwareprogramm kann direkt ausgeführt werden, wenn die EXE-Datei ausgeführt wird.

## MSI-Dateiformat
Windows Installer ist eigentlich eine API (Application Programming Interface) und Softwarekomponente von Microsoft Windows, die für die Installation, Entfernung und Wartung eines Softwareprogramms verwendet wird. Die Installationsinformationen und die optionalen Dateien sind als Installationspakete und lose relationale Datenbanken gepackt, die als strukturierte COM-Speicher strukturiert sind. gut bekannt als **MSI-Dateien**, mit der Dateierweiterung .msi. Die Pakete mit der Dateierweiterung **.mst** enthalten **Transformation Scripts** von Windows Installer, Dateien mit der Erweiterung **.msm** enthalten **Merge Modules** und die Dateierweiterung **.pcp** wird für **Patch-Erstellungseigenschaften** verwendet. Windows Installer wird fortschrittlicher, nachdem es gegenüber seinen früheren Versionen, der Setup-API, erhebliche Änderungen vorgenommen hat. Ein GUI-Framework und die automatische Generierung der Deinstallationssequenz sind die neuen Features von Windows Installer. Es wurde jetzt als Alternative zu eigenständigen ausführbaren Installer-Frameworks in Betracht gezogen.

### Logische Struktur von MSI-Paketen
Ein Paket bezeichnet die Installation eines oder mehrerer Vollprodukte und wird im Allgemeinen durch eine **GUID** identifiziert. Ein Produkt besteht aus einer oder mehreren Komponenten und ist in verschiedene Merkmale gruppiert. Der Windows Installer verarbeitet Abhängigkeiten zwischen verschiedenen Produkten nicht gleichzeitig. Die logische Struktur von Paketen besteht aus den folgenden Elementen:

- **Produkte**: Ein einzelnes, installiertes, funktionierendes Programm oder eine Kombination aus mehreren Programmen ist ein Produkt. Ein Produkt wird durch eine eindeutige GUID identifiziert.
- **Features**: Kann eine beliebige Anzahl von Komponenten und anderen Unterfunktionen enthalten. Kleinere Pakete können aus einem einzigen Feature bestehen.
- **Komponenten**: Komponente wird von Windows Installer als Einheit behandelt; kann Programmdateien, Ordner, Registrierungsschlüssel, COM-Komponenten und Verknüpfungen enthalten.
- **Schlüsselpfade**: Ein Schlüsselpfad ist eine bestimmte Datei, ODBC-Datenquelle oder ein Registrierungsschlüssel, den der Paketautor als kritisch für eine bestimmte Komponente angibt.

## Verweise

* [Windows Installer – von Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


