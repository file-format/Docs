{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME-Datei – Was ist eine .time-Datei? Zeitpunkt, zu dem die Datei unter Linux erstellt wurde",
  "description" : "TIME-Datei – Was ist eine .time-Datei? Zeitpunkt, zu dem die Datei unter Linux erstellt wurde",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Was ist eine TIME-Datei?

Das TIME-Dateiformat wurde von einem Websystem namens LIGHT verwendet, das Benutzern dabei half, ihr Leben aufzuzeichnen, zu organisieren und zu teilen. Im Wesentlichen speicherte es eine Sammlung von Beiträgen und stellte einen Ordner auf der Lebensseite des Benutzers im System dar.

## So finden Sie heraus, wann eine Datei unter Linux erstellt wurde

Unter Linux können Sie den Befehl stat verwenden, um herauszufinden, wann eine Datei erstellt wurde. So können Sie es machen:

Öffnen Sie ein Terminal und geben Sie den folgenden Befehl ein:

```
stat <file_path>
```

Ersetzen Sie `<file_path> ` mit dem Pfad zu der Datei, die Sie interessiert. Zum Beispiel:

```
stat /path/to/your/file.txt
```

Dieser Befehl zeigt verschiedene Informationen über die Datei an, einschließlich ihrer Erstellungszeit. Suchen Sie nach der Zeile, die mit Geburt oder Datei: beginnt. Die Geburtszeit gibt an, wann die Datei im Dateisystem erstellt wurde.

Hier ist ein Beispiel dafür, wie die Ausgabe aussehen könnte:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

In diesem Beispiel gibt die Geburtszeit an, wann die Datei erstellt wurde.

