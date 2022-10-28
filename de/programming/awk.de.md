{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK-Dateiformat - AWK-Skriptdatei",
  "description":"Erfahren Sie mehr über das AWK-Dateiformat und APIs, die AWK-Dateien erstellen und öffnen können.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
"Bezeichner": "Programmierung-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Was ist eine AWK-Datei?

Eine AWK-Datei ist eine Skriptdatei, die für die Textverarbeitungsanwendung **AWK** erstellt wurde, die im Lieferumfang von Unix- und Linux-Betriebssystemen enthalten ist. Es enthält logische Anweisungen zum Ausführen von Aktionen an Text oder Inhalt einer Datei, wie z. B. Abgleichen, Ersetzen und Drucken von Text. Dies hilft beim Generieren von Berichten und formatiertem Text aus der Eingabedatei. Das Dienstprogramm awk befindet sich bei den meisten Linux-/Unix-Distributionen normalerweise unter /usr/bin/awk.

## Wie erstelle ich ein AWK-Skript?

Eine AWK-Datei kann in einem beliebigen Texteditor unter Linux/Unix OS erstellt oder geöffnet werden. Eine neue AWK-Skriptdatei kann wie folgt erstellt werden.

```
$ vi script.awk
```

Dadurch wird die AWK-Datei im Texteditor geöffnet. Geben Sie einige Anweisungen wie folgt in den Texteditor ein.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Die erste Zeile dieses Textinhalts wird wie folgt erklärt.

* \#! – als „Shebang“ bezeichnet, das einen Interpreter für die Anweisungen in einem Skript angibt
* /usr/bin/awk – ist der Interpreter
* -f – Interpreteroption, die zum Lesen einer Programmdatei verwendet wird

## Wie führe ich ein AWK-Skript aus?

Speichern Sie die Datei und machen Sie das Skript ausführbar, indem Sie den folgenden Befehl ausführen:
```
$ chmod +x script.awk
```

Das Skript kann dann wie folgt ausgeführt werden.

```
$ ./script.awk
```

das führt zu folgender Ausgabe.

```
Writing my first Awk executable script!
```

## Bezug ##

* [Skripte mit der Programmiersprache Awk schreiben](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

