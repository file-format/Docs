{
  "date" : "2019-12-13",
  "keywords" :[ "ppt-Datei", "ppt-Dateiformat", "was ist eine ppt-Datei", "Datei", "ppt-Beispiel", "ppt-Dateierweiterung", "Erweiterung", "Format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das PPT-Dateiformat und APIs, die PPT-Dateien erstellen und öffnen können.",
  "title" :"PPT - PowerPoint-Dateiformat",
  "linktitle" :"PPT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine PPT-Datei?

Eine Datei mit der Erweiterung PPT stellt eine PowerPoint-Datei dar, die aus einer Sammlung von Folien zur Anzeige als Diashow besteht. Es gibt das Binärdateiformat an, das von Microsoft PowerPoint 97-2003 verwendet wird. Eine PPT-Datei kann mehrere unterschiedliche Arten von Informationen enthalten, z. B. Text, Aufzählungszeichen, Bilder, Multimedia und andere eingebettete OLE-Objekte. Microsoft entwickelte ab 2007 ein neueres Dateiformat für PowerPoint, bekannt als [PPTX](/de/presentation/pptx/), das auf Office OpenXML basiert und sich von diesem binären Dateiformat unterscheidet. Mehrere andere Anwendungsprogramme wie OpenOffice Impress und Apple Keynote können ebenfalls PPT-Dateien erstellen.

## Kurze Geschichte ##

Microsoft führte das PPT-Dateiformat mit der Veröffentlichung von PowerPoint im Jahr 1987 ein. Das stabile Binärformat wurde als Standard in PowerPoint 97-2003 für Windows freigegeben. Das binäre Dateiformat wird zum Lesen und Schreiben auch von den neuesten Versionen von PowerPoint unterstützt, einschließlich PowerPoint 2016.

## Dateiformatspezifikationen ##

Seit seiner Einführung wurde das PPT-Dateiformat mehrfach überarbeitet, um neue Funktionen und Verbesserungen hinzuzufügen. Die neuesten verfügbaren Versionsspezifikationen sind die der Revision 6.0, die im August 2018 veröffentlicht wurden und nicht mit der tatsächlichen Produktnummer des PPT-Dateiformats gemischt werden sollten, da Microsoft keine Änderungen mehr für dieses Format bereitstellt.

### Überblick über Dateiformate ###

Einige der Schlüsselkomponenten eines PPT-Dateiformats sind wie folgt:

#### Folien ####

Benutzerdaten wie Formen, Text, Animationen und Medien werden einer Präsentation innerhalb einer Folie hinzugefügt. Eine Präsentation kann eine oder mehrere Folien enthalten, die beim Ausführen einer Präsentation als Diashow angezeigt werden. Eine Präsentation enthält Masterfolien und Titelmasterfolien, die als Vorlage für die allgemeinen visuellen Eigenschaften von Präsentationsfolien dienen. Es gibt auch eine Masterfolie für Notizen und eine Masterfolie für Handzettel, die einem ähnlichen Zweck dienen und gemeinsame visuelle Eigenschaften für alle Notizfolien und alle gedruckten Handzettel bereitstellen.

#### Formen ####

Formen sind Objekte, mit denen Benutzer einer Folie eine Vielzahl von Inhalten in Form von Platzhalterformen, Bildern und Diagrammen hinzufügen können. Formen auf einer Masterfolie definieren gemeinsame Daten für Gruppen von Formen.

#### Platzhalter Formen ####

Dies sind spezielle Platzhalter, die als Container für eine Vielzahl von Objekten dienen. Verschiedene Platzhalterformen können verwendet werden, um Hinweise zum Einfügen bestimmter Arten von Formen wie Tabellen oder Diagrammen zu geben. Innerhalb einer Folie übernimmt eine Platzhalterform die visuellen Eigenschaften einer Hauptfolienmaster, Titelmasterfolie oder Notizmasterfolie.

#### Externe Objekte ####

Externe Objekte wie eingebettetes und verknüpftes Audio, verknüpftes Video, eingebettete und verknüpfte OLE-Objekte und Hyperlinks können in eine Folie eingebettet werden. Diese Objekte können verwendet werden, um verknüpfte Objekte für den Zugriff auf externe Ressourcen während einer Diashow zu aktivieren.

### Dateiformatstrukturen ###

PowerPoint-Binärdateiformate bestehen aus folgenden Streams, um die gesamte Dokumentstruktur und Daten darzustellen.

* Aktueller Benutzerstrom
* PowerPoint-Dokumentenstrom
* Bilder-Stream
* Zusammenfassende Informationen und zusammenfassende Dokumentinformationen (optional)

Die vollständigen Spezifikationen für das DOC-Dateiformat finden Sie unter [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) und sollten konsultiert werden in Bezug auf die in den folgenden Abschnitten genannten Details.

#### Aktueller Nutzerstream ####

Es speichert den letzten Benutzer, der das Dokument geöffnet hat, und sein Name muss "Aktueller Benutzer" sein.

#### PowerPoint-Dokumentenstream ####

Zeichnet alle Informationen zu einer PowerPoint-Präsentation auf und erklärt deren Layout und Inhalt. Es ist ein erforderlicher Stream, dessen Name „PowerPoint-Dokument“ lauten MUSS. Der Inhalt dieses Streams wird durch eine Folge von Datensätzen der obersten Ebene angegeben. Partielle Sortierbeschränkungen für die Datensatzsequenz sind in den Datensätzen PersistDirectoryAtom und UserEditAtom angegeben.

Als Containerdatensätze sind die Datensätze DocumentContainer, MainMasterContainer (Abschnitt 2.5.3), HandoutContainer (Abschnitt 2.5.8), SlideContainer (Abschnitt 2.5.1) und NotesContainer (Abschnitt 2.5.6) jeweils die Wurzel eines Baums von Containerdatensätzen und Atomaufzeichnungen. Innerhalb eines Containerdatensatzes können andere Datensätze vorhanden sein, die nicht explizit als untergeordnete Datensätze aufgeführt sind. Unbekannte Datensätze werden identifiziert, wenn das recType-Feld der RecordHeader-Struktur (Abschnitt 2.3.1) einen Wert enthält, der nicht durch die RecordType-Enumeration (Abschnitt 2.13.24) angegeben ist. Diese unbekannten Aufzeichnungen MÜSSEN, falls sie angetroffen werden, ignoriert werden und KÖNNEN <1> aufbewahrt werden. Unbekannte Datensätze können ignoriert werden, indem recLen-Bytes vom Ende der RecordHeader-Struktur nach vorne gesucht werden.

Jedes Mal, wenn dieser Stream geschrieben wird, können neue Datensätze der obersten Ebene, eine Benutzerbearbeitung, an den vorhandenen Stream angehängt werden, oder der gesamte Inhalt des Streams kann durch eine aktualisierte Folge von Datensätzen der obersten Ebene ersetzt werden. Wenn nicht der gesamte Strom ersetzt wird, können alle zuvor existierenden Datensätze der obersten Ebene, die eine vorherige Benutzerbearbeitung umfassten, durch die nachfolgend angehängten Datensätze der obersten Ebene, die die aktuelle Benutzerbearbeitung umfassen, obsolet gemacht werden.

#### Bilderstream ####

Dies ist ein optionaler Stream, der Daten zu den in einer PowerPoint-Präsentation enthaltenen Bildern enthält. Sein Name MUSS "Bilder" lauten. Der Inhalt dieses Streams wird durch den OfficeArtBStoreDelay-Datensatz angegeben, wie in [MS-ODRAW] Abschnitt 2.2.21 angegeben.

#### Zusammenfassender Informationsstrom ####

Es führt Statistiken über das Dokument gemäß dem Microsoft Office-Standard. Der Name des zusammenfassenden Informationsstroms muss "\005SummaryInformation" lauten, wobei \005 das Zeichen mit dem Wert 0x0005 ist, nicht das Zeichenfolgenliteral "\005". Dieser Stream SOLLTE für verschlüsselte Dokumente weggelassen werden. Der Inhalt dieses Streams ist in Abschnitt 2.3.3.2.1 von [MS-OSHARED] angegeben.

#### Dokumentzusammenfassung Informationsstrom ####

Ein optionaler Stream, dessen Name „\005DocumentSummaryInformation“ sein MUSS, wobei \005 das Zeichen mit dem Wert 0x0005 ist, nicht das Zeichenfolgenliteral „\005“. Dieser Stream KANN <2> für verschlüsselte Dokumente weggelassen werden. Die Inhalte dieses Streams sind in [MS-OSHARED] Abschnitt 2.3.3.2.2 angegeben.

#### Verschlüsselter zusammenfassender Informationsstrom ####

Ein optionaler Stream, dessen Name „EncryptedSummary“ lauten MUSS. Dieser Stream existiert nur in einem verschlüsselten Dokument. Der Inhalt dieses Streams ist in Abschnitt 2.3.5.4 von [MS-OFFCRYPTO] angegeben.

#### Speicherung digitaler Signaturen ####

Ein optionaler Speicher, dessen Name „_xmlsignatures“ lauten MUSS. Es KANN weggelassen und ignoriert werden. Der Inhalt dieses Speichers ist in Abschnitt 2.5.2 von [MS-OFFCRYPTO] angegeben.

#### Benutzerdefinierter XML-Datenspeicher ####

Ein optionaler Speicher, dessen Name „MsoDataStore“ lauten MUSS. Der Inhalt des Speichers ist in [MS-OSHARED] Abschnitt 2.3.6 angegeben.

#### Signaturen-Stream ####

Ein optionaler Stream, dessen Name "_signatures" sein MUSS. Es sollte weggelassen werden und kann ignoriert werden. Der Inhalt dieses Streams ist in Abschnitt 2.5.1 von [MS-OFFCRYPTO] angegeben.

## Verweise ##

* [PPT-Dateiformatspezifikationen](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Gemeinsame Office-Datentypen und Objektstrukturen](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Kryptografiestruktur für Office-Dokumente](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint-Dateiformate](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

