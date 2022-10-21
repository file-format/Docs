{
  "date" : "2021-06-30",
  "keywords" :[ "mst-Datei", "mst-Dateiformat", "was ist eine mst-Datei", "Datei", "mst-Beispiel", "mst-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das MST-Dateiformat und APIs, die MST-Dateien erstellen und öffnen können.",
  "title" :"MST - Windows Installer-Paketdatei",
  "linktitle" :"MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Was ist eine MST-Datei?
Die Dateien mit der Erweiterung .mst werden verwendet, um den Inhalt eines MSI-Pakets umzuwandeln. Sie werden häufig von Systemadministratoren verwendet, um die benutzerdefinierten Einstellungen auf eine vorhandene MSI-Datei anzuwenden. Die MST-Dateien werden zusammen mit dem ursprünglichen MSI-Paket in ihren Softwareverteilungssystemen wie Gruppenrichtlinien verwendet. MST-Dateien werden im Allgemeinen in der Softwareentwicklung und beim Testen zum Konfigurieren der in der Entwicklung befindlichen Versionen der Software verwendet.

## MST-Dateiformat
Eine MST- oder Transformationsdatei wird verwendet, um die Installationsoptionen für Programme zu sammeln, die den Microsoft Windows Installer in einer Datei verwenden. Diese Dateien werden häufig in der Befehlszeile des Installationsprogramms (MSIEXEC.EXE) oder in einer Gruppenrichtlinie für die Softwareinstallation verwendet. in einer Microsoft Active Directory-Domäne. Die MST-Dateien können auch mit umschlossenen ausführbaren Installationsprogrammen verwendet werden. Ein allgemeiner Fall ist, dass jemand Befehlszeilenparameter an das verpackte Installationsprogramm übergeben möchte. Dazu benötigen Sie eine MST-Datei, die die Eigenschaft WRAPPED_ARGUMENTS zur Eigenschaftstabelle hinzufügt. Diese Dateien können nicht mit allgemeinen Editoren erstellt oder bearbeitet werden. Hierfür stehen spezielle Tools zur Verfügung.

### Wie verwendet man MST-Dateien?
Die MST-Dateien können mit verschiedenen Tools generiert werden, und Ocra wird im Allgemeinen zum Generieren von MST-Dateien verwendet. Dann können die Einstellungen nach Bedarf angepasst und an einem bestimmten Ort gespeichert werden. Danach können die MST-Dateien in Verbindung mit MSI-Dateien verwendet werden. Wenn Sie diese Dateien testen möchten; Verwenden Sie die folgende Syntax in der Befehlszeile

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS-Eigenschaft

Sie können auch die Eigenschaft **TRANSFORMS** des Windows-Installationsprogramms verwenden, die eigentlich eine Liste der Transformationen ist, die das Installationsprogramm bei der Installation des Pakets anwendet. Das Installationsprogramm führt die Transformationen in derselben Reihenfolge aus, wie sie in der Eigenschaft TRANSFORM aufgelistet sind. Transformationen können nach Dateinamen mit der Erweiterung .mst oder vollständigem Pfad angegeben werden. Um mehr als eine Transformation anzugeben, trennen Sie jeden Dateinamen oder ein Semikolon wie im folgenden Beispiel.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Verweise

* [MST-Transformationsdateien](https://www.exemsi.com/documentation/mst-transformation-files/)
* [TRANSFORMS-Eigenschaft](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


