{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell-Skript – So führen Sie es unter Ubuntu und Linux aus",
  "description":"Erfahren Sie, was Shell Script ist und wie es unter Ubuntu und Linux ausgeführt wird",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Was ist Shell-Skript?

Beim Shell-Scripting wird eine Reihe von Befehlen in eine reine Textdatei geschrieben, die oft als **Shell-Script** bezeichnet wird. Diese Skripte werden von einer Shell ausgeführt, die ein Befehlszeileninterpreter ist. Zu den häufigsten Muscheln gehören

1. Bash (Bourne Again Shell)
2. Zsh (Z-Shell)
3. Fisch.

Shell-Skripte können von einfachen Einzeilern bis hin zu komplexen Programmen reichen und werden zur Ausführung einer Vielzahl von Aufgaben verwendet, wie z. B. Dateibearbeitung, Systemverwaltung und Automatisierung sich wiederholender Aufgaben.

## Vorteile von Shell-Scripting:

1.  **Automatisierung:** Shell-Skripte ermöglichen es Benutzern, sich wiederholende Aufgaben zu automatisieren, wodurch Zeit gespart und das Risiko menschlicher Fehler verringert wird.
    
2.  **Anpassung:** Benutzer können Skripte erstellen, die auf ihre spezifischen Bedürfnisse zugeschnitten sind, was ein hohes Maß an Anpassung ermöglicht.
    
3.  **Stapelverarbeitung:** Shell-Skripte eignen sich hervorragend für die Verarbeitung von Stapelverarbeitungsaufgaben, bei denen mehrere Befehle nacheinander ausgeführt werden müssen.
    
4.  **Systemverwaltung:** Shell-Skripte werden häufig für Systemverwaltungsaufgaben wie Sicherungen, Protokollrotation und Softwareinstallation verwendet.

## Schreiben eines einfachen Shell-Skripts:

Lassen Sie uns ein einfaches Shell-Skript erstellen, das eine Begrüßungsnachricht druckt. Öffnen Sie einen Texteditor und erstellen Sie eine Datei mit dem Namen greeting.sh. Fügen Sie die folgenden Zeilen hinzu:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Speichern Sie die Datei und machen Sie sie ausführbar, indem Sie den folgenden Befehl im Terminal ausführen:

```
chmod +x greeting.sh
```

Jetzt können Sie das Skript ausführen:

```
./greeting.sh
```

Die Ausgabe sollte sein:

```
Hello, welcome to the world of shell scripting!
```

## Ausführen von Shell-Skripten unter Ubuntu und Linux:

Jetzt besprechen wir **wie man eine .sh-Datei unter Ubuntu und Linux ausführt**.

1.  **Machen Sie das Skript ausführbar:** Bevor Sie ein Shell-Skript ausführen, stellen Sie sicher, dass es ausführbar ist. Verwenden Sie den Befehl chmod wie zuvor gezeigt.
    
2.  **Navigieren Sie zum Skriptverzeichnis:** Öffnen Sie ein Terminal und navigieren Sie mit dem Befehl cd zu dem Verzeichnis, das Ihr Shell-Skript enthält.
    
3.  **Führen Sie das Skript aus:** Führen Sie das Skript aus, indem Sie ./scriptname.sh in das Terminal eingeben und scriptname durch den tatsächlichen Namen Ihres Skripts ersetzen.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Verwendung des Bash-Befehls:** Wenn Ihr Skript mit #!/bin/bash beginnt (bekannt als Shebang), können Sie es auch mit dem Bash-Befehl ausführen.

```
bash greeting.sh
```

## Was bedeutet $@ im Shell-Skript?

In Shell-Skripten stellt $@ alle an das Skript übergebenen Befehlszeilenargumente dar. Es wird häufig verwendet, um eine Liste von Argumenten als separate Einheiten zu referenzieren. Bei Verwendung in doppelten Anführungszeichen wie $@ bleiben einzelne Argumente erhalten und berücksichtigen Leerzeichen und Sonderzeichen.

Hier eine kurze Erklärung:

- $@: Stellt alle Positionsparameter (Argumente) dar, die an ein Skript oder eine Funktion übergeben werden. Jedes Argument wird als separates Wort behandelt.
    
- $@: Wenn es in doppelte Anführungszeichen gesetzt wird, bleibt die Trennung der Argumente erhalten und ermöglicht Leerzeichen oder Sonderzeichen innerhalb einzelner Argumente.
    

Hier ist ein einfaches Beispiel zur Veranschaulichung:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Wenn Sie dieses Skript mit Argumenten ausführen, zum Beispiel:

```
bash example.sh arg1 "argument 2" arg3
```

Es würde Folgendes ausgeben:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Wie Sie sehen, repräsentiert $@ alle Argumente und $@ behält die einzelnen Argumente bei, auch wenn sie Leerzeichen enthalten.

