{
  "date" : "2021-04-20",
"Schlüsselwörter": [ "JSPF-Datei", "jspf", "JSPF-Beispiel", "Erweiterung", "Format", "jspf-Tutorial", "jsp-Fragment", "JSPF-Dateiformat" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JSPF - JSP-Fragmentdateiformat",
  "description":"Erfahren Sie mehr über das JSPF-Dateiformat und APIs, die JSPF-Dateien erstellen und öffnen können.",
  "linktitle" : "JSPF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-21"
}

## Was ist eine JSPF-Datei?
Die Datei mit der Erweiterung .jspf heißt JSP-Fragment; eine statische Datei, die in einer anderen JSP-Datei enthalten ist. Die JSPF-Dateien werden nicht eigenständig kompiliert, sie werden jedoch zusammen mit der Seite kompiliert, auf der sie enthalten sind. Seine Syntax ähnelt dem Code von Java Server Pages (JSP). Es enthält nur ein Fragment von JSP; nicht das gesamte JSP-Dokument enthalten.

## JSPF-Dateiformat
Stattdessen wird der Begriff „JSP-Segment“ verwendet, da der Begriff „JSP-Fragment“ in der JSP 2.0-Spezifikation überladen ist. Die JSP-Fragmente können entweder die Erweiterungen .jsp oder .jspf verwenden und sollten entweder in **/WEB-INF/jspf** oder mit den restlichen statischen Dateien abgelegt werden. Die JSP-Fragmente, die keine vollständigen Seiten sind, müssen die Erweiterung .jspf verwenden und in **/WEB-INF/jspf** platziert werden.

### JSP- oder JSP-Fragment-Dateiorganisation
Eine JSP-Datei enthält die folgenden Abschnitte in der Reihenfolge, in der sie aufgeführt sind:

1. Kommentare öffnen
2. JSP-Seitendirektive(n)
3. Optionale Tag-Bibliothek-Anweisung(en)
4. Optionale JSP-Deklaration(en)
5. HTML- und JSP-Code

Eine JSP- oder JSPF-Datei beginnt beide mit einem serverseitigen Stilkommentar, der als **Eröffnungskommentar** bezeichnet wird:

```
<%-- 
  - Author(s):
  - Date:
  - Copyright Notice:
  - @(#)
  - Description: 
  --%>
```
Dieser Kommentar kann nur auf der Serverseite sichtbar sein, da er während der Wiedergabe der JSP-Seite entfernt wird.

## Wann sollte die JSP-Fragmentdatei verwendet werden?
Wenn eine JSP-Seite eine bestimmte, aber komplexe Struktur erfordert, die auch in anderen JSP-Seiten wiederverwendet werden kann, besteht eine Möglichkeit, dies zu handhaben, darin, sie mithilfe des zusammengesetzten Ansichtsmusters (dem Abschnitt "Muster" von Java Blueprints) in Stücke zu zerlegen. Beispielsweise hat eine JSP-Seite manchmal das folgende logische Layout in ihrer Präsentationsstruktur:

{{< figure src="../jspf.png" alt="JSPF-Dateiformat" >}}

In dieser Situation kann diese zusammengesetzte JSP-Seite in verschiedene Module konvertiert werden, die jeweils als separate JSP-Fragmente bezeichnet werden. Die JSP-Fragmente können dann an geeigneten Stellen auf der zusammengesetzten JSP-Seite platziert werden. Daher wird die JSPF-Datei verwendet, wenn statische Include-Direktiven verwendet werden, um eine Seite einzubinden, die nicht von selbst aufgerufen würde, die Dateien mit der Erweiterung .jspf sollten im Verzeichnis /WEB-INF/jspf/ des Webanwendungsarchivs abgelegt werden ( Krieg).

## JSPF-Beispiel
```
<%@ include file="/WEB-INF/jspf/header.jspf" %>
...
<%@ include file="/WEB-INF/jspf/menuBar.jspf" %>
...
<jsp:include page="<%= currentBody %>" />
...
<%@ include file="/WEB-INF/jspf/footnote.jspf" %>
...
<%@ include file="/WEB-INF/jspf/footer.jspf" %>
...
```

## Verweise

* [Code-Konventionen für die JavaServer-Seiten](https://www.oracle.com/technical-resources/articles/javase/code-convention.html)

