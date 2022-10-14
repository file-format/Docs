{
  "date" : "2021-07-25",
"keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix-Handbuch",
  "description":"Erfahren Sie mehr über das FODT-Dateiformat und APIs, die MAN-Dateien erstellen und öffnen können.",
  "linktitle" :"MANN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Was ist eine MAN-Datei?

Eine Datei mit der Erweiterung .man steht für Manpage, die ein Benutzerhandbuch für die Unix-Programmierung in Form einer Softwaredokumentation ist. Es wird von dem in Unix enthaltenen Dienstprogramm "Man" verwendet, das zum Anzeigen der Dokumentation verwendet wird. Die Softwaredokumentation enthält Informationen in Abschnitten und Seiten, die mit dem Man-Dienstprogramm vom Befehlsterminal aus abgerufen werden können, indem Befehle ausgegeben werden. Da es als Softcopy der Dokumentation auf dem Computer verfügbar ist, ist für den Zugriff weder eine gedruckte Kopie noch eine Internetverbindung erforderlich.

## Unix Manual Man-Dateiformat - Weitere Informationen

Manpages werden im Nur-Text-Format gespeichert und können in jedem Texteditor zum Anzeigen oder Bearbeiten erstellt und geöffnet werden. In UNIX werden Informationen aus den Manpages abgerufen, indem Befehle vom Terminal ausgegeben werden, die Verweise auf Abschnitts- und Seitennummern aus dem Handbuch enthalten.

### Abschnitte und Seiten

Unix man ist das Handbuch des Systems, in dem sich jedes Seitenargument des Befehls auf den Namen eines Programms, Dienstprogramms oder einer Funktion bezieht. Der Befehl sucht, wenn er mit Abschnittsinformationen versehen ist, nach der Seite in diesem bestimmten Abschnitt. Das Standardverhalten besteht jedoch darin, in allen Abschnitten nach der Seite zu suchen und die erste Seite anzuzeigen, unabhängig davon, ob sie in mehreren Abschnitten vorhanden ist.

### Abschnittsnummern

Nachfolgend finden Sie Informationen zu den Abschnittsnummern des Handbuchs, gefolgt von den darin enthaltenen Seitentypen.

|Abschnittsnummer|Art der Seiten|
---|---|
|1|Ausführbare Programme oder Shell-Befehle|
|2|Systemaufrufe (vom Kernel bereitgestellte Funktionen)|
|3|Bibliotheksaufrufe (Funktionen innerhalb von Programmbibliotheken)|
|4|Spezielle Dateien (normalerweise in /dev zu finden)|
|5|Dateiformate und Konventionen, zB /etc/passwd|
|6|Spiele|
|7|Verschiedenes (einschließlich Makropakete und Konventionen), zB man(7), groff(7)|
|8|Systemverwaltungsbefehle (normalerweise nur für root)|
|9|Kernel-Routinen [kein Standard]|

## Beispiel - Wie liest man MAN-Seiten?

Hier ist ein Beispiel, wie man Informationen über den MkDir-Befehl mit dem Man-Befehl abruft.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Verweise

* [Technische Spezifikationen von OpenDocument – Von Wikipedia](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux-Handbuchseite](https://man7.org/linux/man-pages/man1/man.1.html)

