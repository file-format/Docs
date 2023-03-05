{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BML-Dateiformat - Bean Markup Language-Datei",
  "description":"Erfahren Sie mehr über das BML-Dateiformat und APIs, die BML-Dateien erstellen und öffnen können.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Was ist eine BML-Datei?

Eine Datei mit der Erweiterung .bml ist eine Bean Markup Language-Datei, die Java-Klassen zur Unterstützung von Java-Apps speichert. Dies ermöglicht den Zugriff auf Java-Objekte und -Methoden und muss keine neue Funktionalität mithilfe von Java-Klassen erstellen. Es legt fest, wie die Komponenten miteinander verbunden sind, um nützliche Aufgaben zu erfüllen. BML wurde von IBM alphaWorks entwickelt, um die Strukturen und Komponentenbeziehungen zu beschreiben. BML-Dateien können mit jedem Texteditor wie Webbrowser, Microsoft Notepad und Notepad++ geöffnet und angezeigt werden.

## BML-Dateiformat

Die IBM Alphaworks-Website hat zwei Implementierungen von BML bereitgestellt. Die erste Implementierung ist ein Interpreter, der ein BML-Skript „abspielt“, um die gewünschte Bean-Hierarchie zu generieren. Die zweite Implementierung ist ein Compiler, der jedes BML-Skript in reflektionsfreien Java-Code kompiliert. Dies ist insofern vorteilhaft, als es ermöglicht, die Interkomponentenstruktur der Anwendung mit einer Sprache zu erfassen, die für diesen speziellen Zweck entwickelt wurde, mit der zusätzlichen Fähigkeit, sie in „normalen“ Java-Code zu kompilieren.

## BML-Tags

Im Folgenden finden Sie eine Erläuterung einiger der in der BML-Sprache verwendeten Tags:

### Das<bean> Schild:

Das<bean> -Element wird verwendet, um neue Beans zu erstellen oder Beans nach Namen zu suchen. Das<bean> Tag hat folgendes Format:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
Die "id" im Tag ist der Objektregistrierung für die JavaBean zugeordnet.

### Das<string> Schild

Es gibt zwei Möglichkeiten, das String-Tag zu verwenden:

1. So erstellen Sie eine nicht leere Zeichenfolge:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. So erstellen Sie eine leere Zeichenfolge:

```
<string/>
```
## Verweise

* [Objektorientiertes Messaging mit XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Die physische Auszeichnungssprache](http://web.mit.edu/mecheng/pml/standards.htm)
* [Die Bean-Markup-Sprache](https://all4dev.blogspot.com/2019/06/bean-markup-language-tutorial.html)

