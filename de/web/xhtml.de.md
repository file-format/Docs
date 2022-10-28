{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Datei", "Erweiterung", "Dateiformat", "Dateierweiterung", "erweiterbares HTML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Extensible Hypertext Markup Language File Format",
  "description":"Erfahren Sie mehr über das XHTML-Dateiformat und die APIs, die XHTML-Dateien erstellen und öffnen können.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine XHTML-Datei?

XHTML ist ein textbasiertes Dateiformat mit Markup im XML, das eine Neuformulierung von HTML 4.0 verwendet. Diese Dateien eignen sich gut zum Öffnen oder Betrachten in einem Webbrowser. XHTML wurde entworfen, um strukturierter zu sein, weniger Scripting, generischer; Nutzung aller vorhandenen Möglichkeiten von XML und mehr Geräteunabhängigkeit. XHTML bietet einen allgemein sinnvollen Satz von Elementen und Attributen mit Erweiterungsmöglichkeiten in Kombination mit Stylesheets. Die Attribute werden aus der Sammlung von Metadatenattributen verwendet. XHTML bietet Flexibilität und Zugänglichkeit, indem es alle **[HTML](/de/web/html/)**-Präsentationselemente Stylesheets unterordnet. Stylesheets sind vielseitiger als diese Präsentationselemente. Spezifikationen für HTML 4.01, HTML5 und XHTML werden dynamisch vom World Wide Web Consortium (W3C) entwickelt.

## Kurze Geschichte des XHTML-Dateiformats

Die Geschichte von XHTML beginnt mit einem Dokumententwurf, der im Dezember 1998 vom World Wide Web Consortium veröffentlicht wurde. Dieses Dokument bezieht sich auf die „Umformulierung von HTML in XML“, eine Spezifikation namens XHTML 1.0. Diese neue Spezifikation hat HTML in XML unter Verwendung der vorhandenen Elemente oder Attribute neu formuliert. Im Mai 1999 erklärte das W3 Consortium, dass HTML 4.0 in eine XML-Anwendung umgeformt worden sei. dh XHTML. Am 26. Januar 2000 wurde die erste Spezifikation, die XHTML 1.0 definiert, vom W3C veröffentlicht. Am 31. Mai 2001 kündigte das W3C XHTML als eigenständige Sprache an und begann mit der Entwicklung von HTML 5.0. Im Jahr 2005 wurde jedoch eine Arbeitsgruppe (WHATWG) gegründet, die darauf abzielte, gewöhnliches HTML unabhängig von XHTML zu verbessern. Die WHATWG begann schließlich, parallel zu XHTML 2 an HTML5 zu arbeiten.

## XHTML-Dateiformat

XHTML ist ein Format, bei dem es sich um eine Sammlung verschiedener Dokumenttypen und Module handelt, die HTML 4 nachahmen, kategorisieren und erweitern. Die Dateien in XHTML sind XML-basiert und zielen darauf ab, mit den auf XML basierenden Benutzerprogrammen zusammenzuarbeiten. XHTML-Dateien sind XML-konform. Standard-XML-Tools werden verwendet, um XHTML-Dateien anzuzeigen, zu bearbeiten und zu validieren. Von HTML Document Object Model oder dem XML Document Object Model [DOM] abhängige Anwendungen können über XHTML-Dokumente arbeiten. Wenn sich Content-Entwickler heute für XHTML entscheiden, können sie alle damit verbundenen Vorteile von XML genießen, ohne sich Gedanken über die Vorwärts- oder Rückwärtskompatibilität ihrer Inhalte machen zu müssen.

Ein Satz verwandter Elemente bildet ein Modul in XHTML. Ein Formular- oder Tabellenmodul kann verschiedene Formular- oder Tabellenelemente enthalten, die auf einer Webseite angezeigt werden können. Die Modularisierung zielte darauf ab, HTML-Elemente in Gruppen von zahlreichen verknüpften Elementen zu isolieren. Damit Entwickler von Inhalten die Vorteile der Modulauswahl für verschiedene Gerätetypen nutzen können. Darüber hinaus ermöglichen Module Benutzeragenten, Elemente auszuwählen, ohne die Konsistenz mit dem XHTML-Standard zu verlieren. Die Parsing-Anforderungen von XHTML sind dieselben wie von XML, während HTML seine eigenen praktiziert.

### Dokumentkonformität

XHTML2 bietet Spezifikationen, die XHTML 1.0-Dokumenten entsprechen, die die Namensraumelemente und -attribute von XML und XHTML 1.0 verwenden. Es gibt zwei Arten von Dokumentkonformität.

Ein strikt konformes Dokument basiert auf XML und benötigt nur die in dieser Spezifikation definierten obligatorischen Dienste. Folgende Kriterien müssen für XHTML-Dateien erfüllt sein:

* Eine Datei muss den Einschränkungen entsprechen, die in DTDs und in Anhang B definiert sind.
* Das Basiselement der Datei muss html sein.
* Das Basiselement der Datei muss eine Deklaration für den XHTML-Namensraum enthalten und sollte wie folgt definiert sein:

```
http://www.w3.org/1999/xhtml.
```

* Das Basiselement könnte folgendermaßen geschrieben werden:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Vor dem Basiselement muss ein DOCTYPE deklariert werden, dessen öffentlicher Bezeichner auf eine der drei Document Type Definitions (DTDs) verweisen muss. Die Systemkennung kann modifiziert werden, um den aktuellen Systemkonventionen zu entsprechen.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

In XML-Dokumenten ist es unnötig, XML-Deklarationen in allen Dokumenten anzugeben; Inhaltsentwickler werden jedoch dazu verleitet, XML-Deklarationen in all ihren XHTML-Dokumenten zu verwenden. Diese Deklaration ist obligatorisch, wenn entweder die Zeichencodierung des Dokuments von UTF-8/16 abweicht oder keine Codierung durch ein geltendes Protokoll festgelegt wurde. Das folgende Beispiel eines XHTML-Dokuments definiert die XML-Deklarationen

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Ein konformer Benutzeragent muss die folgenden Regeln erfüllen:

* Die Analyse und Bewertung des XHTML-Dokuments erfolgt durch einen Benutzeragenten, der dessen Konsistenz mit der XML 1.0-Empfehlung sicherstellt.
* Im Falle eines validierenden Benutzeragenten muss dieser die Gültigkeit der Dokumente für ihre referenzierten DTDs gemäß XML prüfen. Wenn die XHTML-Datei vom Benutzeragenten als generisches XML verarbeitet wird, werden die Merkmale des Typs ID als Fragmentkennungen anerkannt.

Wenn ein Benutzeragent auf ein nicht erkanntes Element stößt, müssen die folgenden obligatorischen Kriterien erfüllt werden

* den Inhalt dieses unbekannten Elements verarbeiten
* das Attribut und seinen Wert ignorieren
* Verwenden Sie den Wert des als Standard bereitgestellten Attributs.

Wenn der Benutzeragent auf eine Entitätsreferenzdeklaration stößt, die noch nicht verarbeitet wurde, sollte sie als Zeichen verarbeitet werden (beginnend mit dem „&“-Zeichen und endend mit dem Semikolon). Während der Inhaltsverarbeitung können Zeichen oder Zeichenentitätsreferenzen, die durch den Benutzeragenten vorhersagbar, aber nicht darstellbar sind, jede alternative Wiedergabe verwenden, die eine ähnliche Bedeutung ergibt. In einem solchen Fall muss das Dokument auf eine Weise angezeigt werden, die dem Benutzer deutlich macht, dass der Aufbereitungsprozess nicht normal war. Für die Verarbeitung von Leerzeichen muss der Benutzeragent die Definition aus CSS-Zeichen [CSS2] suchen.

## XHTML-Abwärtskompatibilität

Die Abwärtskompatibilität von XHTML 1.-Dokumenten ist mit HTML 4-Benutzerprogrammen vertraut, wenn die richtigen Regeln befolgt werden. XHTML 1.1 ist vollständig kompatibel mit Ausnahme von Ruby-Anmerkungen, auch wenn sie im Allgemeinen von den HTML 4-Browsern ignoriert werden. XHTML 2.0 ist vergleichsweise weniger kompatibel, dennoch wurde das Problem bis zu einem gewissen Grad durch die Verwendung von Skripten angegangen.

## Verweise

* [Eine Geschichte von XHTML: Von den 1990er Jahren bis heute](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

