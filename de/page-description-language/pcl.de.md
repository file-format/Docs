{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Erfahren Sie mehr über das PCL-Dateiformat und APIs, die PCL-Dateien erstellen und öffnen können.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PCL-Datei? ##

PCL steht für Printer Command Language, eine von Hewlett Packard (HP) eingeführte Seitenbeschreibungssprache. HP hat PCL entwickelt, um eine effiziente Möglichkeit zur Steuerung von Druckerfunktionen über viele verschiedene Druckgeräte hinweg bereitzustellen. Das Format wurde ursprünglich für HPs Nadel- und Tintenstrahldrucker entwickelt, wurde aber im Laufe der Zeit Teil verschiedener Thermo-, Matrix- und Seitendrucker. Das Format wurde mehreren verschiedenen Überarbeitungen unterzogen, was zu verschiedenen Versionen führte, wobei jede Version verbessert wurde, um den Anforderungen der Zeit in Bezug auf die Druckersteuerungsfunktionen gerecht zu werden. Heute ist PCL die am weitesten verbreitete Druckersprache auf dem Druckermarkt.

## PCL-Versionen ##

PCL-Versionen unterscheiden sich in der Funktionalität (z. B. Schriftartenunterstützung: Bitmap-Schriftarten, skalierbare Schriftarten (Intellifonts, TrueType-Schriftarten), Rastergrafik-Komprimierungsmethoden, HP-GL/2-Grafikunterstützung).

**PCL 1:** um 1980 - Die Print-and-Space-Funktionalität ist der Basissatz von Funktionen, die für eine einfache, bequeme Einzelbenutzer-Workstation-Ausgabe bereitgestellt werden.

**PCL 2:** um 1980 – EDP (Electronic Data Processing)/Transaktionsfunktionalität ist eine Obermenge von PCL 1. Funktionen wurden für das Drucken von Mehrbenutzersystemen für allgemeine Zwecke hinzugefügt.

**PCL 3**: 1984 – Die Office-Textverarbeitungsfunktionalität ist eine Obermenge von PCL 2. Funktionen wurden für die Erstellung hochwertiger Office-Dokumente und eine Erhöhung der Auflösung auf bis zu 300 dpi hinzugefügt. Es ermöglichte die Verwendung einer begrenzten Anzahl von Bitmap-Schriftarten und -Grafiken und unterstützte HP-GL. PCL 3 wurde von anderen Druckerherstellern weitgehend nachgeahmt und von diesen Unternehmen als „LaserJet Plus Emulation“ bezeichnet.
(Drucker: HP DeskJet-Produktfamilie, HP LaserJet-Seriendrucker, HP LaserJet Plus-Seriendrucker)

**PCL3+:** Wird von der DeskJet- und DesignJet-Druckerfamilie verwendet.

**PCL3c:** Wird von DeskJet- und DesignJet-Druckern verwendet.

**PCL3e**: Wird von der DeskJet- und DesignJet-Druckerfamilie verwendet. Wird jetzt auch in PhotoSmart verwendet.

**PCL3GUI**: Verwendet RTL und wird von der DeskJet- und DesignJet-Druckerfamilie verwendet.

**PCLSLEEK**: Verwendet RTL und wird von der DeskJet- und DesignJet-Druckerfamilie verwendet.

**PCL 4**: 1985 - Seitenformatierungsfunktionalität ist eine Obermenge von PCL 3. Unterstützte Makros, größere Bitmap-Schriftarten und Grafiken. (Drucker: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 – Office Publishing-Funktionalität ist eine Obermenge von PCL 4. Zu den neuen Publishing-Funktionen gehören Schriftskalierung und HP-GL/2 (Vektorgrafiken). (Drucker: HP LaserJet III)

**PCL 5e:** 1994 - Dies ist eine größere Überarbeitung, die neue Funktionen wie Adaptive Compression System, 2-Byte-Zeichenkodierung, Unterstützung für Vektorschriftarten und bidirektionale Konfigurationsbefehle enthält. Enthält logische Operationen (entspricht GDI ROPs) zur Verbesserung der Windows-Unterstützung vor dem Beschneiden von Pfaden. (Drucker: HP LaserJet 4)

**PCL 5j:** Neue Funktionen wie Unterstützung von 2-Byte-Zeichen für japanische residente skalierbare Schriftarten, vertikale Schrift, japanische Papierformate und Zeichenketten. (Drucker: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Farbunterstützung und logische Operationen wurden zu PCL5 hinzugefügt. PCL5c ist älter als PCL5e. Einige Modelle unterstützen auch Beschneidungspfade. (Drucker: HP Color LaserJet, HP PaintJet 300 XL (erster Drucker mit PCL5c), HP DeskJet 1200C/1600C (diese Modellnummern wurden wiederverwendet und die neueren Modelle sind nicht PCL 5c)

**PCL 5ce:** Unterstützt skalierbare Schriften von Agfa Microtype. (Drucker: HP 2500c Pro Drucker)

**PCL 6 / XL:** 1996 - PCL 6 oder PCL XL ist ein neues Format, das 1995 eingeführt wurde und nicht mit früheren Versionen von PCL kompatibel ist. (Drucker: HP LaserJet 5, 5M und 5N)

## PCL 6-Übersicht ##

HP führte 1996 PCL 6 ein, das die nächste Evolution der PCL-Sprache und verwandter Technologien war. Es hat folgende Komponenten:

**PCL 6 Enhanced:** bietet eine optimierte Version zum Drucken über grafische Benutzeroberflächen (GUIs) wie MS Windows und OS/2

**PCL 6 Standard:** bietet vollständige Abwärtskompatibilität mit früheren HP LaserJet-Druckern

**PCL Font Synthesis:** bietet skalierbare Schriftarten, Schriftartverwaltung und Speicherung von Formularen und Schriftarten.

Die erweiterte Version PCL XL ist näher an GDI, das viele Anwendungen verwenden. Es stellt sicher, dass weniger Übersetzungen stattfinden, was zu erhöhten WYSIWYG-Fähigkeiten und einer besseren Leistung bei Anwendungen führt, die vom erweiterten Treiber implementierte Escapes unterstützen. Die Ausgabe des Enhanced (PCL XL)-Treibers entspricht möglicherweise nicht der Ausgabe des Standardtreibers. Wenn die Ausgabe nicht wie erwartet ist, wählen Sie stattdessen den Standardtreiber (PCL5e).

Die erweiterten PCL 6-Befehle sind so konzipiert, dass sie die Grafikdruckanforderungen für GUI-basierte Anwendungen optimal erfüllen. In den meisten Fällen gibt es für jeden Grafikdruckbefehl, den eine GUI ausführen möchte, einen passenden erweiterten PCL 6-Befehl. Dies reduziert die Anzahl der Befehle, die zum Beschreiben einer Grafikseite erforderlich sind. Jeder Befehl in PCL 6 Enhanced ist so konzipiert, dass nur eine minimale Datenübertragung vom Host-PC zum Drucker erforderlich ist. Dies reduziert die Datenmenge, die zum Beschreiben einer Seite erforderlich ist.

Das Windows-Drucksystem für die meisten HP LaserJet-Drucker bietet zwei separate Treiber: Standard und Erweitert. Der Standardtreiber bietet Abwärtskompatibilität durch die Verwendung von PCL 6 Standard (PCL5e)-Befehlen, um einfachen Text oder gemischte Text- und Grafikseiten zu drucken. Der Enhanced-Treiber verwendet die PCL 6 Enhanced-Befehle, die für das Drucken komplexer Grafikseiten optimiert wurden.

## PCL 6-Klassenrevisionen ##

#### Klasse 1.1 ####

**Zeichenwerkzeuge:** Unterstützt das Zeichnen von Linien, Bögen/Ellipsen/Sehnen, (abgerundeten) Rechtecken, Polygonen, Bézierpfaden, beschnittenen Pfaden, Rasterbildern, Scanlines, Rasteroperationen.
**Farbverarbeitung:** Unterstützt 1/4/8-Bit-Paletten, RGB/Grau-Farbraum. Unterstützt benutzerdefinierte Halbtonmuster (max. 256 Muster).
**Komprimierung:** Unterstützt RLE.
**Maßeinheiten:** Zoll, Millimeter, Zehntel Millimeter.
**Papierhandhabung:** Unterstützt benutzerdefinierte oder vordefinierte Sätze von Papiertypen, einschließlich gängiger Letter, Legal, A4 usw. Kann Papier aus manueller Zufuhr, Fächern und Kassetten auswählen. Papier kann horizontal oder vertikal beidseitig bedruckt werden. Papier kann im Hochformat, Querformat oder in einer 180-Grad-Drehung der beiden ersteren ausgerichtet werden.
**Schriftart:** Unterstützt Bitmap- oder TrueType-Schriftarten, 8- oder 16-Bit-Codepunkte. Die Auswahl des Zeichensatzes verwendet einen anderen Symbolsatzcode als PCL 5. Wenn Bitmap-Schriftarten verwendet werden, sind viele Skalierungsbefehle nicht verfügbar. Wenn TrueType-Schriftarten verwendet werden, werden Deskriptoren mit variabler Länge und Fortsetzungsblöcke nicht unterstützt. Umrissschrift kann gedreht, skaliert oder geschert werden.

#### Klasse 2.0 ####

**Komprimierung:** Eine proprietäre JPEG-Komprimierung namens JetReady wurde hinzugefügt.
**Papierhandhabung:** Medien können zu verschiedenen Ausgabefächern umgeleitet werden (bis zu 256). Voreingestellte Medienformate A6 und Japanisch B6 hinzugefügt. Drittes Kassetten-Preset hinzugefügt, 248 externe Medienquellen.
**Schriftart:** Text kann vertikal geschrieben werden.

#### Klasse 2.1 ####

**Farbbehandlung:** Farbanpassungsfunktion hinzugefügt.
**Komprimierung:** Delta Row hinzugefügt.
**Papierhandhabung:** Ausrichtung, Mediengröße sind optional, wenn eine neue Seite deklariert wird. Papiersorten B5, JIS 8K, JIS 16K, JIS Exec hinzugefügt.

#### Klasse 3.0 ####

**Farbbehandlung:** Ermöglicht die Verwendung unterschiedlicher Halbtoneinstellungen für Vektor- oder Rastergrafiken, Text. Unterstützt adaptive Halbtonung.
**Protokoll:** Unterstützt PCL Passthrough, sodass PCL 5-Funktionen von PCL 6-Streams verwendet werden können. Einige PCL 6-Zustände werden jedoch nicht beibehalten, wenn diese Funktion verwendet wird.
**Schriftart:** Unterstützt PCL-Schriftarten.
**Viewer/Converter:** PCLReader (Freeware) kann jede Stufe von PCL 6 (einschließlich JetReady) auf jedem Drucker anzeigen, konvertieren oder drucken.

## Verweise ##

* [PCL – von Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

