{
  "date" : "2019-10-11",
  "keywords" :[ "CGM", "Computer Graphics Metafile", "File", "Extension", "File Format", "Vector Graphics", "Metafile Descriptor"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CGM-Dateiformat",
  "description":"Erfahren Sie mehr über das CGM-Dateiformat und APIs, die CGM-Dateien erstellen und öffnen können.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Was ist eine CGM-Datei? ##

Computer Graphics Metafile (CGM) ist ein kostenloses, plattformunabhängiges, internationales Standard-Metadateiformat zum Speichern und Austauschen von Vektorgrafiken (2D), Rastergrafiken und Text. CGM verwendet einen objektorientierten Ansatz und viele Funktionsvorgaben für die Bilderzeugung. CGM verwendet diese objektorientierten Eigenschaften zum Umformen grafischer Elemente zum Rendern eines Bildes. Eine Metadatei enthält notwendige Informationen, die andere Dateien definieren. Bei CGM enthält eine textbasierte Quelldatei alle grafischen Elemente, die später in eine Binärdatei kompiliert werden können. Grundsätzlich ist CGM eine Möglichkeit, den Austausch von grafischen 2D-Daten unabhängig von einer bestimmten Plattform oder einem bestimmten Gerät zu erleichtern.

Das CGM-Format stellt verschiedene Elemente bereit, um Funktionen auszuführen und Objekte zu kennzeichnen, um geometrische Grundelemente und grafische Informationen anzupassen. Obwohl CGM durch andere Formate ersetzt wurde, um Grafiken auf Webseiten anzuzeigen, da es von Webseiten nicht gut unterstützt wird, ist es immer noch sehr beliebt bei industriellen, luftfahrttechnischen und anderen technischen Anwendungen. Obwohl das World Wide Web Consortium mit WebCGM einen alternativen Ansatz für die Verwendung von CGM im Web entwickelt hat. Die primäre CGM-Implementierung war eine Veranschaulichung der Abfolge grundlegender Operationen des Graphical Kernel Systems (GKS). Es wurde in professionellen Designs nicht viel übernommen, aber weitgehend durch andere Formate wie DXF und SVG ersetzt.

## Geschichte ##

CGM wurde 1987 zu einem internationalen Standard (ISO 8632-1987) und wurde auch in Großbritannien von BSI und den USA von ANSI als nationaler Standard übernommen. Nach einer Reihe von Änderungen im Jahr 1991 wurde 1992 ein überarbeiteter CGM-Standard veröffentlicht (ISO 8632:1992). Im Jahr 2001 entwickelte das World Wide Web Consortium WebCGM mit erweiterten Funktionen zur Verwendung mit Webseiten. 2007 wurde die zweite Version von WebCGM veröffentlicht und die dritte Version wurde 2010 mit erweiterten Funktionen veröffentlicht.

## CGM-Dateiformat ##

Computergraphik-Metadateien sind im Grunde Datenbanken für graphische Informationen und stellen die Mittel zum Erfassen, Speichern und Übertragen graphischer Daten bereit. Folglich muss gleichzeitig mit der Ausführung einer Anwendung in einem Metadateiformat eine grafische Systemkomponente zum Erstellen der Datenbank vorhanden sein. In den meisten Fällen ist diese Komponente der Metafile-Generator. Daneben besteht Bedarf an einer weiteren Komponente, die grafische Daten in einer Metadatei abrufen, interpretieren und wiedergeben kann. Diese Notwendigkeit wird durch das Vorhandensein eines Metadatei-Interpreters erfüllt. Die folgende Abbildung zeigt die Arbeitsumgebung der grafischen Metadatei.

Die Beziehung von CGM zu anderen Komponenten eines typischen Grafiksystems ist in der obigen Abbildung dargestellt. Aus der Figur ist auch ersichtlich, dass die Funktionalität der Metadatei nicht von der endgültigen Geräteausgabe abhängt.

Im Allgemeinen gibt es zwei Kategorien von Metadateien: **Abschnittsaufnahme** und **Bildaufnahme**. Die primäre Funktionalität der Bildaufnahme-Metadatei ist die Aufnahme von geräteunabhängigen, mehrfachen Bilddefinitionen. Während Sitzungserfassungs-Metadateien die Systemschnittstelle verwenden, um den Ausgabedialog in einem grafischen System zu erfassen. CGM gehört zur Kategorie der statischen Bildaufnahme-Metadateien. CGM bietet eine übersichtliche Anordnung von Komponenten mit einer zweistufigen Struktur.

1. Metadatei-Deskriptor
1. Ein Pool logisch unabhängiger Bilder

Jedes Bild ist eine Sammlung von Bilddeskriptoren und ein Bildkörper, der eine Bilddefinition enthält. Der Metafile-Deskriptor definiert beschreibende Informationen, die gleichermaßen für alle Bilder dieser Metadatei gelten. Diese Informationen helfen dem Interpreter, eine Metadatei korrekt zu parsen und die Ressourcen zu erkennen, die für die korrekte Wiedergabe eines Bildes erforderlich sind. Obwohl der Bilddeskriptor auch die beschreibenden Informationen einschließt, kann er doch nur das Bild erkennen, in dem sich der Deskriptor befindet. In diesem Dateiformat ist jede Bilddefinition in sich abgeschlossen und logisch souverän. Sie sind unabhängig von allen anderen Bilddefinitionen in einer Datei. Unmittelbar nach der Interpretation des Meta-Deskriptors können Bilder zufällig abgerufen und interpretiert werden. Die Änderung des Zustands vorheriger Bilder hat keine Auswirkung auf deren Nachfolger. Diese Bildunabhängigkeit ist ein weiteres herausragendes Merkmal von CGM. CGM besteht aus einem Koordinatenraum, bei dem es sich um kartesische 2D-Koordinaten handelt, die als virtuelle Gerätekoordinaten bezeichnet werden und durch Zahlen oder Genauigkeiten dargestellt werden können, die den Bereich und die Granularität darstellen. CGM spezifiziert sowohl die direkte Farbauswahl als auch die indexbasierte Auswahl. Im ersteren besteht der Farbspezifizierer aus einem RGB-Tripel, während später der Farbspezifizierer einen Index in eine Farbtabelle anzeigt.

CGM matches the needs of both communication-dependent as well as performance-dependent applications. Centralized and distributed graphics systems can use CGM in an unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
