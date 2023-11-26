{
  "date" : "2023-01-31",
  "keywords" :["Ausführungsdatei", "Was ist eine Ausführungsdatei", "Datei", "Wie öffnet man eine Ausführungsdatei", "Ausführungsdateierweiterung", "Erweiterung"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das RUN-Dateiformat und die APIs, mit denen RUN-Dateien erstellt und geöffnet werden können.",
  "title" :"RUN-Dateiformat – Ausführbare Linux-Datei",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## Was ist eine RUN-Datei?

Das .run-Dateiformat wird häufig zum Verteilen von Software- oder Anwendungsinstallationsprogrammen in der Linux-Umgebung verwendet. Um die Software zu installieren, müssen Sie die Datei ausführbar machen, was mit dem folgenden Befehl möglich ist:

```bash
chmod +x file_name.run 
```

Anschließend können Sie die Datei mit dem folgenden Befehl ausführen:

```bash
./file_name.run 
```

Der Installationsvorgang kann je nach der spezifischen Datei und dem Programm, die Sie installieren möchten, variieren.

Das .run-Dateiformat ist eine Art Shell-Skript, das zum Verteilen von Software- oder Anwendungsinstallationsprogrammen in der Linux-Umgebung verwendet wird. Es handelt sich um ein eigenständiges Paket, das alles enthält, was zur Installation der Software erforderlich ist, einschließlich Binärdateien, Bibliotheken und Konfigurationsdateien.

Es ist wichtig zu beachten, dass .run-Dateien auch bösartigen Code enthalten können. Daher ist es immer eine gute Idee, die Quelle der Datei zu überprüfen und sie auf Viren zu scannen, bevor Sie sie ausführen.

Darüber hinaus sind für die Ausführung und Installation einiger .run-Dateien möglicherweise Root-Rechte erforderlich. Daher müssen Sie möglicherweise den Befehl "sudo" verwenden, um die Datei mit erhöhten Berechtigungen auszuführen:

```bash
sudo ./filename.run
```

## Wie öffne ich eine RUN-Datei?

Um eine .run-Datei zu öffnen, müssen Sie sie ausführbar machen, was mit dem Befehl "chmod" erfolgen kann:

```bash
chmod +x filename.run 
```

Sobald die Datei ausführbar gemacht wurde, können Sie sie ausführen, indem Sie Folgendes eingeben:

```bash
./filename.run
```

Das Ausführen einer .run-Datei ist nicht dasselbe wie das Öffnen in einem Texteditor. Beim Ausführen einer .run-Datei werden deren Anweisungen ausgeführt, die von der Installation eines Programms bis zur Ausführung eines Skripts reichen können. Um den Inhalt einer .run-Datei anzuzeigen, müssen Sie sie in einem Texteditor wie Nano oder Vim öffnen:

```
nano filename.run
```
oder
```
vim filename.run
```

## Verweise
* [So führen Sie .bin- und .run-Dateien in Ubuntu aus](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


