
{
  "date" : "2023-02-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"4. Datei – Dateiformat der vierten Sprache",
  "description":"Erfahren Sie anhand von Beispielen und APIs, mit denen 4th-Dateien erstellt und geöffnet werden können, was das .4th-Dateiformat ist.",
  "linktitle" : "4th",
  "menu" : {
    "docs" : {
      "identifier":"programming-4th",
      "parent" : "programming"
}
},
  "lastmod" : "2023-02-09"
}

## Was ist eine 4. Datei?

Eine Datei mit der Dateierweiterung .4th ist eine Programmierdatei, die für die **Forth Programming Language** erstellt wurde. Es enthält Quellcode für Programme, die in der Programmiersprache Forth geschrieben sind, und generiert die Ausgabe, wenn das Programm ausgeführt wird. Es handelt sich lediglich um eine weitere Programmiersprachendatei, die der Quelldatei [C](/programming/c/) und [C++](/programming/cpp/) ähnelt.

## 4. Dateiformat – Weitere Informationen


### Codebeispiel für die vierte Programmiersprache

Hier ist ein Beispiel für ein einfaches, in Forth geschriebenes Programm, das die Fakultät einer bestimmten Zahl berechnet:

```
: factorial ( n -- n! )
   dup 0=
   if
      drop 1
      exit
   then
   1
   swap
   begin
      dup 1-
      dup 0=
      if
         drop
         exit
      then
      swap
      *
   repeat
;

```

In diesem Beispiel nimmt das Fakultätswort ein einzelnes Argument n und gibt seine Fakultät zurück. Das Wort "dup" dupliziert den Wert oben auf dem Stapel, "drop" verwirft den Wert oben auf dem Stapel und "*" multipliziert die beiden Werte oben auf dem Stapel. Die if- und begin/until-Konstrukte steuern den Programmablauf.

Um dieses Programm zu verwenden, geben Sie die Definition in den Forth-Interpreter ein und rufen dann das Fakultätswort mit der Zahl auf, deren Fakultät Sie finden möchten:

```
10 factorial .
```
Dies würde zur Ausgabe 3628800 führen, was der Fakultät von 10 entspricht.

## Verweise

* [Programmiersprache Forth](https://en.wikipedia.org/wiki/Forth_(programming_language))

