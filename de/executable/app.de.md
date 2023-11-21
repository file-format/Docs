{
"Datum": "02.02.2023",
  "keywords": [
"App-Datei",
"Was ist eine App-Datei",
"Datei",
"Wie öffnet man eine App-Datei",
"App-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
  "toc": true,
  "description":"Erfahren Sie mehr über das APP-Dateiformat und APIs, mit denen APP-Dateien erstellt und geöffnet werden können.",
"title": "APP-Dateiformat – macOS-Anwendungspaket",
"linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent": "ausführbare Datei"
}
},
"lastmod": "02.02.2023"
}

## Was ist eine APP-Datei?

Eine .app-Datei unter macOS ist ein spezieller Verzeichnistyp, der alle zum Ausführen einer bestimmten Anwendung erforderlichen Dateien enthält, einschließlich des ausführbaren Codes, der Ressourcen und der Metadaten. Die Erweiterung .app signalisiert dem Betriebssystem, dass dieses Verzeichnis als einzelne Einheit und nicht als Sammlung separater Dateien behandelt werden soll und dass es direkt über den Finder oder das Dock gestartet werden kann.

Finder ist die Standard-Dateimanageranwendung unter macOS. Es ermöglicht Ihnen, die Dateien und Verzeichnisse auf Ihrem Computer zu durchsuchen und zu organisieren. Das Dock ist eine Funktion von macOS, die schnellen Zugriff auf häufig verwendete Anwendungen und Dokumente ermöglicht. Sowohl im Finder als auch im Dock können Sie Anwendungen starten, indem Sie auf ihre .app-Dateien klicken, wodurch das entsprechende Anwendungspaket geöffnet wird. Wenn Sie eine Anwendung starten, wird der ausführbare Code im .app-Bundle ausgeführt, wodurch die Anwendung zur Verwendung verfügbar gemacht wird. Die .app-Datei ist die Darstellung der Anwendung im Dateisystem und bietet dem Benutzer die Möglichkeit, auf die Anwendung zuzugreifen und sie zu starten.

Wenn Sie auf einem macOS-System im Finder mit der rechten Maustaste auf eine .app-Datei klicken und "Paketinhalt anzeigen" auswählen, können Sie die interne Struktur des Anwendungspakets sehen. Dies ist nützlich, wenn Sie auf von der Anwendung verwendete Ressourcen oder Dateien zugreifen oder den Inhalt der Anwendung zur Fehlerbehebung überprüfen möchten. Der Paketinhalt einer .app-Datei umfasst normalerweise Verzeichnisse für Ressourcen wie Bilder und Sounds sowie den ausführbaren Code für die Anwendung. Indem Sie den Inhalt einer .app-Datei untersuchen, können Sie tiefere Einblicke in den Aufbau und die Funktionsweise der Anwendung gewinnen.

## Wie öffne ich eine APP-Datei?

Um eine .app-Datei unter macOS zu öffnen, doppelklicken Sie einfach im Finder auf die Datei. Dadurch wird die im .app-Bundle enthaltene Anwendung gestartet. Wenn die Anwendung auf Ihrem System installiert ist und mit dem Dateityp .app verknüpft wurde, sollte ein Doppelklick auf die Datei die Anwendung automatisch starten. Wenn die Anwendung nicht mit dem Dateityp .app verknüpft ist, müssen Sie möglicherweise mit der rechten Maustaste auf die Datei klicken und "Öffnen mit" auswählen, um eine geeignete Anwendung zum Öffnen auszuwählen.

Sie können eine .app-Datei auf dem Terminal in macOS öffnen, indem Sie den Befehl "open" verwenden. Navigieren Sie dazu mit dem Befehl "cd" zu dem Verzeichnis, in dem sich die .app-Datei befindet, und führen Sie dann den folgenden Befehl aus:

```
open <AppName>.app 
```

Wo<AppName> ist der Name der Anwendung, die Sie starten möchten. Dadurch wird die Anwendung so gestartet, als hätten Sie im Finder darauf doppelgeklickt. Der Befehl "open" ist ein Allzweckdienstprogramm, mit dem viele verschiedene Dateitypen geöffnet werden können, darunter Anwendungen, Dokumente und Verzeichnisse. Wenn Sie den Befehl "open" für eine .app-Datei verwenden, wird die im Bundle enthaltene Anwendung gestartet.

## Verweise
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
