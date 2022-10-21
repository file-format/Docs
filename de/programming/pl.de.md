{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "Datei", "Erweiterung", "Format", "Perl", "Perl-Sprache", "PL-Dateien", "Programmierung"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das PL-Dateiformat und APIs, die PL-Dateien erstellen und öffnen können.",
  "title" :"PL-Datei - Perl-Skriptdateiformat",
  "linktitle" :"PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## Was ist eine PL-Datei?

Eine Datei mit der Erweiterung .pl ist eine Perl-Skriptdatei, die eine Skriptsprache ist. Diese werden mit der Perl Interpreter-Software kompiliert und ausgeführt. Eine PL-Skriptdatei enthält Codezeilen, Variablen und Kommentare. Skriptsprachen sind vergleichsweise schwer zu handhaben
andere Programmierdateiformate wie [PHP](/de/programming/php/) verstehen. PL-Dateien können erstellt werden und sind mit Windows, macOS und Linux kompatibel.

## Kurze Geschichte der Perl-Skriptsprache

Diese Sprache wurde erstmals 1987 verwendet, daher haben diese Dateien ihren Ursprung in diesem Jahr. 1989 wurde Perl 2 veröffentlicht. Später wurde es aktualisiert und bis zur Version 5.35 modifiziert, und die nächste Version soll nächstes Jahr veröffentlicht werden.

In jedem Update wurden Tools zu Funktionalität, Leistung und Aussehen der Sprache und Dateien hinzugefügt. In diesen Jahren gab es viele Überarbeitungen der Versionen. Es war ursprünglich eine einfache Skriptsprache, aber jetzt umfasst es auch viele andere Module. Ursprünglich war es eine sehr einfache Sprache, aber die Schriften dieser Sprache waren ziemlich schwer zu verstehen, da sie kompakt waren.

## Spezifikationen für Perl-Dateiformaterweiterungen

Es gibt einige Eigenschaften oder Spezifikationen dieser Programmierdateien, einige davon sind wie folgt:

* Der in diesen Dateien enthaltene Code liegt im Nur-Text-Format vor und wird für die Skriptentwicklung verwendet
* Scripting des Servers, Parsen von Text und Serververwaltung sind die Hauptaspekte, die das Script dieser Sprache abdeckt
* Viele beliebte Programme, die mit dieser Sprache verbunden sind, sind Active State Active Perl und Bare Bones BBEdit (kompatibel mit Mac OS).
* Diese Sprache gilt als Hochsprache
* Für Win32 muss der Benutzer möglicherweise die native Binärverteilung der Sprache installieren
* Es erfordert einige Skripting-Tools, um in verschiedenen Windows Resource Kits ausführbar zu werden
* Visual Studio .NET ist ein bekanntes Framework für die Entwicklung von Programmiersprachen. Das als Visual Perl bekannte Active State-Tool wird verwendet, um Perl in Visual Studio hinzuzufügen
* In den Dateien beschreibt die erste Zeile des Quellcodes die Informationen des verwendeten Interpreters. Die PL-Dateien beginnen normalerweise mit der Zeile **#!/usr/bin/perl**, die Ihren Computer anweist, dieses Skript mit einem auf dem Computer installierten Perl-Interpreter auszuführen


## PL-Skriptbeispiele

```
#!/usr/bin/perl
print "Hello, world\n";
```

Dies wird gedruckt

```
Hello, World
```

### Einzeiliger Kommentar ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Mehrzeiliger Kommentar ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Variablenzuweisung ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skalare Variablenzuweisung ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Einfache Skalaroperationen ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Verweise ##

- [Python (Programmiersprache) - Wikipedia](https://en.wikipedia.org/wiki/Python_(Programmiersprache))

