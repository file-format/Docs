{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Berichtsdefinitionssprachdatei",
  "keywords" :[ "rdl", "Berichtsdefinitionssprache", "XmlTextWriter", "XSD", "RDL-Element"],
  "description":"Erfahren Sie mehr über das RDL-Dateiformat, das eine XML-Darstellung einer SQL Server Reporting Services-Berichtsdefinition ist.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## Was ist eine RDL-Datei? ##

Die RDL (Report Definition Language) ist ein von Microsoft festgelegter Maßstab für die Definition von Berichten. Eine RDL-Datei besteht aus einem oder mehreren RDL-Elementen. Während ein RDL-Element aus seinem Datentyp und seiner Kardinalität besteht. Ein Element kann einfach oder komplex sein. Das einfache Element hat keine untergeordneten Elemente oder Attribute, während ein komplexes Element untergeordnete Elemente und optionale Attribute hat.

## RDL-XML-Schemadefinition
Eine XML Schema Definition (XSD)-Datei validiert die RDL-Datei. Das Schema definiert die Regeln dafür, wo RDL-Elemente in einer RDL-Datei vorkommen können. Ein RDL-Element kann einfach oder komplex sein. Ein einfaches Element hat keine untergeordneten Elemente oder Attribute und ein komplexes Element hat untergeordnete Elemente und optional Attribute.

## RDL erstellen
Da RDL von Natur aus offen und erweiterbar ist, können viele Anwendungen und Tools erstellt werden, die RDL-Dateien basierend auf ihrem XML-Schema generieren. Eine der einfachsten Möglichkeiten zum Erstellen von RDL aus einer Anwendung besteht darin, die Microsoft .NET Framework-Klassen des **System.Xml**-Namespace und des System.Linq-Namespace zu verwenden. Insbesondere die **XmlTextWriter**-Klasse kann zum Schreiben von RDL verwendet werden. Mit **XmlTextWriter** können Sie in jeder .NET Framework-Anwendung eine vollständige Berichtsdefinition von Anfang bis Ende generieren. Entwickler können auch benutzerdefinierte Berichtselemente mit benutzerdefinierten Eigenschaften hinzufügen, um die RDL zu erweitern.

## RDL-Typen
Die folgende Tabelle listet die Typen und Attribute auf, die in RDL-Elementen verwendet werden.

|Typ|Beschreibung|
---|---|
|Binär |Eine Eigenschaft mit einem Base-64-codierten Binärwert.|
|Boolean| Eine Eigenschaft mit true oder false als Wert des Objekts. Sofern nicht anders angegeben, ist der Wert eines weggelassenen optionalen booleschen Objekts False.|
|Datum |Eine Eigenschaft mit einem vollständig angegebenen Datums- oder Datumszeitwert, angegeben im ISO8601-Datumsformat: JJJJ-MM-TT[THH:MM[:SS[.S]]].|
|Enum |Eine Eigenschaft mit einem Zeichenfolgentextwert, der einer aus einer Liste ausgewiesener Werte sein muss.|
|Float |Eine Eigenschaft mit einem Gleitkommawert. Als optionales Dezimaltrennzeichen wird ein Punkt (.) verwendet.|
|Integer |Eine Eigenschaft mit einem Integer-Wert (int32).|
|Sprache |Eine Eigenschaft mit einem Textwert, der einen Sprach- und Kulturcode enthält, z. B. "en-us" für US-Englisch. Der Wert muss entweder eine bestimmte Sprache oder eine neutrale Sprache sein, für die im Microsoft .NET Framework eine Standardsprache definiert ist.|
|Name |Eine Eigenschaft mit einem Zeichenfolgentextwert. Namen müssen innerhalb des Namensraums des Elements eindeutig sein. Wenn nicht angegeben, ist der Namespace für ein Element das innerste enthaltende Objekt, das einen Namen hat.|
|NormalizedString |Eine Eigenschaft mit einem normalisierten String-Textwert.|
|Größe |Ein Größenelement muss eine Zahl enthalten (mit einem Punkt als optionales Dezimaltrennzeichen). Der Zahl muss ein Bezeichner für eine CSS-Längeneinheit wie cm, mm, in, pt oder pc folgen. Ein Leerzeichen zwischen der Nummer und dem Bezeichner ist optional. Weitere Informationen zu Größenbezeichnern finden Sie unter Referenz zu CSS-Werten und -Einheiten. In RDL beträgt der Höchstwert für Größe 160 Zoll. Die Mindestgröße beträgt 0 Zoll.|
|String |Eine Eigenschaft mit einem String-Textwert.|
|UnsignedInt |Eine Eigenschaft mit einem vorzeichenlosen Ganzzahlwert (uint32).|
|Variant |Eine Eigenschaft mit einem beliebigen einfachen XML-Typ.|

## RDL-Datentypen
In RDL definiert die DataType-Enumeration den Datentyp eines Attributs, Ausdrucks oder Parameters. Die folgende Tabelle zeigt, wie CLR-Datentypen RDL-Datentypen entsprechen.

|CLR-Typ(en) |Entsprechender Datentyp|
---|---|
|Boolean| Boolesch|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Einzeln, Doppelt |Float|
|Zeichenfolge, Zeichen, GUID, Zeitspanne |Zeichenfolge|


## Verweise ##

- [Berichtsdefinitionssprache (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Berichtsdefinitionssprache (SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

