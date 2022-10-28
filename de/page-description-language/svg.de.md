{
  "date" : "2020-03-02",
  "keywords" :[ "SVG", "Datei", "Dateiformat", "Seitenbeschreibungssprache", "Skalar" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das SVG-Dateiformat und APIs, die SVG-Dateien erstellen und öffnen können.",
  "title" :"Was ist eine SVG-Datei?",
  "linktitle" : "SVG",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2020-03-02"
}

## Was ist eine SVG-Datei? ##

Eine SVG-Datei ist eine Scalar Vector Graphics-Datei, die ein XML-basiertes Textformat verwendet, um das Erscheinungsbild eines Bildes zu beschreiben. Das Wort Skalierbar bezieht sich darauf, dass das SVG ohne Qualitätsverlust auf verschiedene Größen skaliert werden kann. Die textbasierte Beschreibung solcher Dateien macht sie auflösungsunabhängig. Es ist eines der am häufigsten verwendeten Formate zum Erstellen einer Website und zum Drucken von Grafiken, um Skalierbarkeit zu erreichen. Das Format kann allerdings nur für zweidimensionale Grafiken verwendet werden. SVG-Dateien können in fast allen modernen Browsern angezeigt/geöffnet werden, einschließlich Chrome, Internet Explorer, Firefox und Safari.

## Kurze Geschichte ##

SVG-Spezifikationen sind seit 1999 vom World Wide Web Consortium (W3C) als offener Standard verfügbar. Zuvor wurden bis 1998 ähnliche Dateiformatspezifikationen in sechs verschiedenen Formaten beim W3C eingereicht. 2011 wurde eine Aktualisierung der Spezifikationen angewendet und sie wurde auf Version 1.1 . 2016 wurde SVG 2 als neuere Version mit zusätzlichen Funktionen zu SVG 1.1 veröffentlicht.

## Dateiformatspezifikationen ##

Das SVG Document Object Model (DOM) legt die Grundlage für alle Spezifikationen und Schnittstellen, die den jeweiligen Abschnitten der Spezifikation entsprechen. SVG-Viewer müssen die SVG-DOM-Schnittstellen implementieren, wie sie in den W3C-Spezifikationen definiert sind. Sein DOM stellt mehrere Schnittstellen für verschiedene Datentypen und Elemente bereit.

### SVG-Formen ###

SVG hat einige vordefinierte Formelemente, die von Entwicklern verwendet werden können:

* Rechteck<rect>
* Kreis<circle>
* Ellipse<ellipse>
* Linie<line>
* Polylinie<polyline>
* Polygon<polygon>
* Weg<path>

Basierend auf diesen Formen und Spezifikationen sind die Funktionsbereiche von SVG wie folgt.

**Pfade** - Pfade werden verwendet, um sowohl einfache als auch zusammengesetzte Formumrisse darzustellen. Codierungen werden verwendet, um die Art des Betriebs zu definieren. Zum Beispiel wird M für Move To verwendet, L wird für Line To verwendet, Z wird verwendet, um einen Pfad zu schließen und so weiter.

**Grundformen** - Geradlinige Pfade und Pfade, die aus einer Reihe verbundener gerader Liniensegmente (Polylinien) bestehen, sowie geschlossene Polygone, Kreise und Ellipsen können gezeichnet werden. Auch Rechtecke und Rechtecke mit abgerundeten Ecken sind Standardelemente.

**Text** – Die Textdarstellung wird als XML-Zeichendaten ausgedrückt, wobei viele visuelle Effekte auf den Text angewendet werden können. Die Spezifikationen ermöglichen die Verarbeitung von bidirektionalem Text, vertikalem Text und Zeichen entlang eines gekrümmten Pfads.

**Malen** - Formen können mit einer Farbe, einem Farbverlauf oder einem Muster gefüllt und/oder umrandet werden, was die Möglichkeit bietet, sie undurchsichtig zu machen oder einen beliebigen Grad an Transparenz zu haben. Linienend-Features wie Pfeilspitzen oder Symbole, die an den Scheitelpunkten eines Polygons erscheinen, werden durch Markierungen dargestellt.

**Farbe** - SVG-Spezifikationen ermöglichen es, Farben auf alle sichtbaren SVG-Elemente anzuwenden, entweder direkt oder über Füllung, Kontur und andere Eigenschaften. Zur Angabe können unterschiedliche Farbcodierungen verwendet werden wie Schwarz oder Blau, Hex-Darstellung, Dezimal oder als Prozentwerte der Form RGB.

**Farbverläufe und Muster** - Formen in einer SVG-Datei können mit Volltonfarben, Farbverläufen oder sich wiederholenden Mustern gefüllt oder umrandet werden.

**Filtereffekte** - Es handelt sich eigentlich um eine Reihe von Grafikoperationen, die auf eine bestimmte Quellvektorgrafik angewendet werden, um ein modifiziertes Ergebnis zu erzeugen.

**Interaktivität** - Benutzer können mit SVG-Dateien interagieren, indem sie den Fokus ändern, mit der Maus klicken, das Bild scrollen oder zoomen. Die Interaktivität ermöglicht es SVG-Bildern, wie oben erwähnt, auf viele verschiedene Arten mit Benutzern zu interagieren.

**Verknüpfung** - Es ist möglich, dass SVG-Bilder Hyperlinks zu anderen Dokumenten haben. Dies wird über die XML Linking Language oder XLink erreicht. Dies ermöglicht das Erstellen bestimmter Ansichtszustände, die zum Vergrößern/Verkleinern eines bestimmten Bereichs oder zum Beschränken der Ansicht auf ein bestimmtes Element verwendet werden.

**Skripterstellung** – Ähnlich wie bei HTML sind alle Aspekte eines SVG-Dokuments für die Bearbeitung mithilfe von Skripts zugänglich. Die SVG-DOM-Objekte bieten die Anleitung, um dies mithilfe von SVG-Elementen und -Attributen zu erreichen. Skripte sind in "Skript"-Tag-Elemente eingeschlossen und können je nach Bedarf als Reaktion auf Zeiger-, Tastatur- oder Dokumentereignisse ausgeführt werden.

**Animation** - Die DOM-Elemente<animate> ,<animateMotion> und<animateColor> ermöglicht das Einfügen von Animationen für SVG-Inhalte. Dies ist natürlich nicht ohne die Verwendung von Skripten und eingebauten Timern zu erreichen. Diese Animationen können kontinuierlich sein und können sowohl in eine Schleife als auch in Wiederholungen geschaltet werden, während sie gleichzeitig auf Benutzerereignisse reagieren.

**Schriftarten** – Text in SVG kann auf externe Schriftartdateien wie Systemschriftarten verweisen. Wenn solche Schriftarten fehlen, wird Text in SVG nicht in der Ausgabe gerendert. Dies kann überwunden werden, indem die erforderlichen Glyphen in eine solche Datei als Schriftart integriert werden, die dann mit der gerendert wird<text> Element.

## Beispiele ##
Die folgenden Zeilen zeigen, wie ein Kreis mit dem SVG-Skript dargestellt wird.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

Die folgenden Codezeilen zeigen, wie man die verwendet<text> Block zum Rendern von Text in SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## Verweise ##

* [W3C SVG-Spezifikationen](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)

