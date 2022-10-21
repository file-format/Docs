{
  "date" : "2019-10-11",
"Schlüsselwörter": [ "sh-Datei", ".sh-Datei", "Erweiterung", "Format", "sh-Dateibeispiel", "sh-Dateiformat", "wie man eine sh-Datei ausführt" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash-Shell-Skriptdatei",
  "description":"Erfahren Sie mehr über das SH-Dateiformat und APIs, die SH-Dateien erstellen und öffnen können.",
  "linktitle" :"SCH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Was ist eine SH-Datei?

Eine Datei mit der Erweiterung .sh ist eine Skriptsprache-Befehlsdatei, die ein Computerprogramm enthält, das von der Unix-Shell ausgeführt werden soll. Es kann eine Reihe von Befehlen enthalten, die sequentiell ausgeführt werden, um Operationen wie Dateiverarbeitung, Ausführung von Programmen und andere derartige Aufgaben auszuführen. Diese werden vom Benutzer über die Befehlszeilenschnittstelle oder im Batch ausgeführt, um mehrere Vorgänge gleichzeitig auszuführen. Skriptdateien können in Texteditoren wie Notepad, Notepad++, Vim, Apple Terminal und anderen ähnlichen Anwendungen unter Windows, MacOS und Linux OS geöffnet werden.

## SH-Dateiformat

SH-Dateien werden im Klartext nach der definierten Syntax geschrieben. Diese Skriptdateien unterstützen:

* `Kommentare` - Kommentare beginnen mit einem # und werden von der Shell ignoriert.
* `Shortcuts` - Diese können verwendet werden, um einen Befehl für eine kurze und einfache Ausführung umzubenennen.
* `Batch Jobs` - Mehrere Befehle können automatisch ausgeführt werden, die ansonsten manuell eingegeben werden müssten. Dadurch entfällt die Notwendigkeit, darauf zu warten, dass ein Benutzer jede Stufe der Sequenz auslöst.
* `Generalisierung` - Mit einfachen Schleifen wird viel mehr Verallgemeinerung für Operationen wie die Konvertierung von Bildern von einem Format in ein anderes erreicht.

## Beispiel einer SH-Datei

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Wie führe ich die SH-Datei aus?
Die SH-Dateien werden normalerweise unter Linux ausgeführt, selbst unter Windows müssen Sie eine Verbindung zu einem Linux-Terminal herstellen, indem Sie Software wie Putty verwenden, um die sh-Dateien auszuführen. Im Folgenden sind die Schritte zum Ausführen einer SH-Datei auf einem Linux-Terminal aufgeführt.

1. Öffnen Sie das Linux-Terminal und wechseln Sie in das Verzeichnis, in dem sich die SH-Datei befindet.
2. Legen Sie mit dem Befehl „chmod“ die Ausführungsberechtigung für Ihr Skript fest (falls nicht bereits festgelegt).
3. Führen Sie das Skript mit einer der folgenden Methoden aus
1. `./Dateiname.sh`
2. `sh Dateiname.sh`
3. `bash script-name-here.sh`

## Verweise

* [Bashscripting für Anfänger](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

