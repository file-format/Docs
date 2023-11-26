{
"Datum": "07.03.2023",
  "keywords": [
"Manifestdatei",
"Was ist eine ManifestDatei?",
"Datei",
"Manifest-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MANIFEST-Dateiformat – Windows-Anwendungsmanifestdatei",
  "description":"Erfahren Sie mehr über das MANIFEST-Format und die APIs, mit denen MANIFEST-Dateien erstellt und geöffnet werden können.",
"linktitle": "MANIFEST",
  "menu": {
    "docs": {
      "identifier": "system-manifest",
"parent": "system"
}
},
"lastmod": "07.03.2023"
}

## Was ist eine MANIFEST-Datei?

Eine Manifestdatei ist eine Datei, die Informationen über eine Softwareanwendung oder ein Softwarepaket enthält. Die Datei wird normalerweise mit der Dateierweiterung .manifest benannt. Die Manifestdatei enthält Informationen zu den im Paket enthaltenen Dateien, ihren Versionsnummern und etwaigen Abhängigkeiten des Pakets von anderen Softwarekomponenten.

Manifestdateien werden häufig auf der Windows-Plattform verwendet, um sicherzustellen, dass Softwareanwendungen ordnungsgemäß installiert und konfiguriert werden. Sie können verwendet werden, um beispielsweise anzugeben, welche Versionen gemeinsam genutzter Bibliotheken verwendet werden sollen, welche Konfigurationsdateien enthalten sein sollen und welche Registrierungsschlüssel während der Installation geändert werden sollen.

Neben Windows können Manifestdateien auch in anderen Kontexten verwendet werden, beispielsweise für Webanwendungen oder Android-Anwendungen. Das spezifische Format und der Inhalt einer Manifestdatei hängen von der Plattform und der zu packenden Anwendung ab.

## Mehr Informationen

Manifestdateien liegen im XML-Format vor. XML ist eine weit verbreitete Auszeichnungssprache zum Erstellen strukturierter Dokumente und Daten und wird häufig in der Softwareentwicklung zur Beschreibung von Konfigurationen, Einstellungen und anderen Metadaten verwendet.

Im Kontext von Softwareanwendungen enthält eine Manifest-XML-Datei normalerweise Informationen über die Abhängigkeiten der Anwendung, Versionsinformationen und andere Konfigurationseinstellungen. Die Datei wird verwendet, um sicherzustellen, dass die Anwendung korrekt installiert wird und über alle erforderlichen Komponenten und Ressourcen verfügt, um ordnungsgemäß ausgeführt zu werden.

Die Manifest-XML-Datei kann im Anwendungspaket enthalten sein oder als separate Datei, die während der Installation heruntergeladen wird. Der Name trägt normalerweise die Dateierweiterung ".manifest" und folgt einem bestimmten Format, das von der Plattform oder dem Framework definiert wird, auf dem die Anwendung basiert.

Beispielsweise wird im Microsoft .NET Framework eine Manifest-XML-Datei verwendet, um die Abhängigkeiten und Versionsinformationen für eine Anwendung zu beschreiben, und sie ist normalerweise als Teil der Assembly der Anwendung enthalten. Die Datei wird von der Common Language Runtime (CLR) verwendet, um die richtigen Versionen der zu ladenden Assemblys zu ermitteln und sicherzustellen, dass die Anwendung ordnungsgemäß ausgeführt wird.

## Verweise
* [Manifestdatei](https://en.wikipedia.org/wiki/Manifest_file)

