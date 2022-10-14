{
  "date" : "2020-03-16",
  "keywords" :[ "IFC-Datei", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über das IFC-Dateiformat und APIs, die IFC-Dateien erstellen und öffnen können.",
  "title" :"IFC-Dateiformat",
  "linktitle" :"IFC",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine IFC-Datei?

Dateien mit der Erweiterung IFC beziehen sich auf das Dateiformat Industry Foundation Classes (IFC), das internationale Standards für den Import und Export von Gebäudeobjekten und deren Eigenschaften festlegt. Dieses Dateiformat bietet Interoperabilität zwischen verschiedenen Softwareanwendungen. Spezifikationen für dieses Dateiformat werden von buildingSMART International als Datenstandard entwickelt und gepflegt. Das ultimative Ziel des IFC-Dateiformats ist die Verbesserung der Kommunikation, Produktivität, Lieferzeit und Qualität während des gesamten Lebenszyklus eines Gebäudes.

Aufgrund der etablierten Standards für gängige Objekte in der Bauindustrie reduziert es den Informationsverlust bei der Übertragung von einer Anwendung zur anderen. IFC kann Daten für Geometrie, Berechnung, Mengen, Facility Management, Preisgestaltung usw. für viele verschiedene Berufe (Architekt, Elektro, HLK, Tragwerk, Gelände usw.) enthalten.

## Kurze Geschichte ##

Die IFC-Initiative wurde 1994 von Autodesk ergriffen, um die integrierte Anwendungsentwicklung zu unterstützen, und umfasste Unternehmen wie Honeywell, Butler Manufacturing und AT&T. 1995 wurde die Mitgliedschaft für jedermann geöffnet und der Name in International Alliance for Interoperability geändert. Die Absicht der gemeinnützigen Organisation war es, die Industry Foundation Class (IFC) als AEC-Produktmodell zu veröffentlichen. 2005 wurde der Name erneut geändert und wird jetzt von buildSMART beibehalten.

## IFC-Dateiformat ##

Das IFC-Dateiformat wurde in der Vergangenheit mehrfach geändert, um die Dateiformatspezifikationen v4. Von Zeit zu Zeit gab es mehrere kleinere Änderungen, die als Nachträge in die Spezifikationen aufgenommen wurden. Nachfolgend finden Sie eine Liste verschiedener Versionen von Dateispezifikationen, die in der Vergangenheit veröffentlicht wurden.

* IFC4 Add2 (2016)IFC4 Add1 (2015)
* IFC4 (März 2013) ifcXML2x3 (Juni 2007)
* IFC2x3 (Februar 2006) ifcXML2 für IFC2x2 add1 (RC2)
* IFC2x2 Anhang 1 (Juli 2004)ifcXML2 für IFC2x2 (RC1)
* IFC 2x2IFC 2x Anhang 1ifcXML1 für IFC2x und
* IFC2x-Nachtrag 1IFC 2xIFC 2.0IFC 1.5.1IFC 1.5

Die neuesten Versionen der IFC-Dateiformatspezifikationen sind immer auf der buildingSMART-Website verfügbar, und Entwickler sollten diese für alle Arten von Anwendungen konsultieren, die sie entwickeln möchten. Zum Zeitpunkt des Schreibens dieses Artikels sind die Spezifikationen der Version 4 die neuesten, die online verfügbar sind.

### IFC-Datendateiformate ###

Das IFF-Dateiformat unterstützt den Datenaustausch zwischen Anwendungen mit verschiedenen Formaten, wie unten aufgeführt:

**IFC:** Dies ist das standardmäßige IFC-Austauschformat und verwendet die physische STEP-Dateistruktur gemäß ISO 10303-21. Dieses Dateiformat hat die Dateierweiterung .ifc und ist das am häufigsten verwendete IFC-Format.

**IFC-XML:** Es handelt sich um eine XML-Dateiformatversion von IFC, die direkt von der sendenden Anwendung gemäß der ISO 10303-28-Struktur generiert werden kann, auch als STEP-XML bezeichnet. Das IFC-XML-Dateiformat gilt als geeignet für die Interoperabilität zwischen XML-Tools. Im Vergleich zum IFC-Dateiformat ist IFC-XML 300-400 % größer.

**IFC-ZIP:** Es ist eine [ZIP](/de/compression/zip/) komprimierte Version von IFC oder IFC-XML, wobei eine dieser Dateien das Hauptverzeichnis des Zip-Archivs ist. Dieses Format komprimiert eine .ifc-Datei um 60–80 % und eine .ifc-XML-Datei um 90–95 %.

### IFC-Architektur ###

Die IFC-Spezifikation umfasst Begriffe, Konzepte und Datenspezifikationselemente, die aus der Verwendung in Disziplinen, Gewerken und Berufen der Bau- und Facility-Management-Branche stammen. Begriffe und Konzepte verwenden die einfachen englischen Wörter, die Datenelemente innerhalb der Datenspezifikation folgen einer Namenskonvention.

die Datenelementnamen für Typen, Entitäten, Regeln und Funktionen beginnen mit dem Präfix „Ifc“ und werden mit den englischen Wörtern in CamelCase-Namenskonvention fortgesetzt (kein Unterstrich, erster Buchstabe im Wort in Großbuchstaben); die Attributnamen innerhalb einer Entität folgen der CamelCase-Namenskonvention ohne Präfix; die Eigenschaftssatzdefinitionen, die Teil dieses Standards sind, beginnen mit dem Präfix „Pset_“ und werden mit den englischen Wörtern in der CamelCase-Namenskonvention fortgesetzt; Die Definitionen von Mengensätzen, die Teil dieses Standards sind, beginnen mit dem Präfix „Qto_“ und werden mit den englischen Wörtern in der CamelCase-Namenskonvention fortgesetzt.

Die Datenschemaarchitektur von IFC definiert vier konzeptionelle Schichten, jedes einzelne Schema ist genau einer konzeptionellen Schicht zugeordnet.

**Ressourcenebene** – Die unterste Ebene umfasst alle individuellen Schemas, die Ressourcendefinitionen enthalten, diese Definitionen enthalten keine global eindeutige Kennung und dürfen nicht unabhängig von einer auf einer höheren Ebene deklarierten Definition verwendet werden;

**Kernebene** – Die nächste Ebene umfasst das Kernelschema und die Kernerweiterungsschemas, die die allgemeinsten Entitätsdefinitionen enthalten, alle auf der Kernebene oder darüber definierten Entitäten tragen eine global eindeutige ID und optional Besitzer- und Verlaufsinformationen;

**Interoperabilitätsebene** – Die nächste Ebene enthält Schemata, die Entitätsdefinitionen enthalten, die spezifisch für ein allgemeines Produkt, einen Prozess oder eine Ressourcenspezialisierung sind, die in mehreren Disziplinen verwendet werden. Diese Definitionen werden normalerweise für den domänenübergreifenden Austausch und die gemeinsame Nutzung von Konstruktionsinformationen verwendet.

**Domänenebene** – Die höchste Ebene enthält Schemata, die Entitätsdefinitionen enthalten, die Spezialisierungen von Produkten, Prozessen oder Ressourcen sind, die für eine bestimmte Disziplin spezifisch sind. Diese Definitionen werden normalerweise für den Austausch und die gemeinsame Nutzung von Informationen innerhalb einer Domäne verwendet.

## Verweise ##

* [Industry Foundation Classes – von Wikipedia] (https://en.wikipedia.org/wiki/Industry_Foundation_Classes)

