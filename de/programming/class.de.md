{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class", "was ist eine Klassendatei", "wie man eine Klassendatei öffnet", "Erweiterung", "Datei", "Klassendatei", "Klassendateiformat", ".class-Erweiterung ", "Klassendatei in Java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Klasse - Java-Klassendateiformat",
  "description":"Erfahren Sie mehr über Klassendateiformate und APIs, die Klassendateien erstellen und öffnen können.",
  "linktitle" :"Klasse",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Was ist eine Klassendatei?

Eine **Klassendatei in Java** ist die kompilierte Ausgabe der Klasse [.java](/de/programming/java/), die tatsächlich von einer Java Virtual Machine (JVM) ausgeführt wird. Klassendateien können sowohl einzeln ausgeführt werden als auch als Bündel zusammen mit anderen Paketdateien Teil einer [JAR](/de/programming/jar/)-Datei sein. Diese können mit dem Befehl **`javac`** über die Befehlszeilenschnittstelle erstellt werden. Einige Java-IDEs wie [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) und NetBeans bieten Erstellungs-.class-Ausgabedateien aus dem Java des Projekts Dateien.

## Klassendateiformat

Eine Java-Klassendatei besteht aus Bytecode, der Zwischencode ist, der von JVM ausgeführt werden soll. Eine Klassendatei besteht aus einem Strom von 8-Bit-Bytes, und Multibyte-Datenelemente werden immer in Big-Endian-Reihenfolge gespeichert.

### ClassFile-Struktur

Die Klassendateistruktur ist wie unten gezeigt.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
wo:

* u1 = vorzeichenlose Ein-Byte-Menge
* u2 = vorzeichenlose Zwei-Byte-Menge
* u4 = vorzeichenlose Vier-Byte-Menge

Details der .class-Dateistruktur werden auch in Oracle [Klassendateiformat](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) erklärt und können von verwiesen werden Entwickler als Referenz. Eine Zusammenfassung dieser Felder ist wie folgt.

* `magic` - Das magische Element liefert die magische Nummer, die das Klassendateiformat identifiziert; es hat den Wert 0xCAFEBABE.
* `minor_version`, `major_version` - Die Werte der Elemente minor_version und major_version sind die Neben- und Hauptversionsnummern dieser Klassendatei.
* „constant_pool_count“ – Der Wert des Elements „constant_pool_count“ ist gleich der Anzahl der Einträge in der Tabelle „constant_pool“ plus eins. Ein Constant_Pool-Index gilt als gültig, wenn er größer als Null und kleiner als Constant_Pool_Count ist, mit Ausnahme von Konstanten vom Typ Long und Double.
* „constant_pool[]“ – „constant_pool“ ist eine Tabelle von Strukturen (§4.4), die verschiedene Zeichenfolgenkonstanten, Klassen- und Schnittstellennamen, Feldnamen und andere Konstanten darstellen, auf die in der ClassFile-Struktur und ihren Unterstrukturen verwiesen wird. Das Format jedes Constant_pool-Tabelleneintrags wird durch sein erstes "Tag"-Byte angezeigt.
* `access_flags` - Der Wert des Elements access_flags ist eine Maske von Flags, die verwendet werden, um Zugriffsberechtigungen und Eigenschaften dieser Klasse oder Schnittstelle zu kennzeichnen.
* `this_class` - Der Wert des Elements this_class muss ein gültiger Index in der Tabelle constant_pool sein.
* `super_class` - Für eine Klasse muss der Wert des Elements super_class entweder null sein oder ein gültiger Index in der Tabelle constant_pool sein.
* „interfaces_count“ – Der Wert des Elements „interfaces_count“ gibt die Anzahl direkter Superschnittstellen dieser Klasse oder dieses Schnittstellentyps an.
* `interfaces[]` - Jeder Wert im Interface-Array muss ein gültiger Index in der constant_pool-Tabelle sein.
* `fields_count` - Der Wert des Elements fields_count gibt die Anzahl der field_info-Strukturen in der Feldertabelle an.
* `fields[]` - Jeder Wert in der fields-Tabelle muss eine field_info-Struktur sein, die eine vollständige Beschreibung eines Feldes in dieser Klasse oder Schnittstelle gibt.
* „methods_count“ – Der Wert des Elements „methods_count“ gibt die Anzahl der method_info-Strukturen in der Methodentabelle an.
* `methods[]` - Jeder Wert in der Methodentabelle muss eine method_info-Struktur sein, die eine vollständige Beschreibung einer Methode in dieser Klasse oder Schnittstelle gibt. Wenn keines der Flags ACC_NATIVE und ACC_ABSTRACT im Element access_flags einer method_info-Struktur gesetzt ist, werden auch die Java Virtual Machine-Anweisungen geliefert, die die Methode implementieren.
* `attributes_count` - Der Wert des Elements attributes_count gibt die Anzahl der Attribute (§4.7) in der Attributtabelle dieser Klasse an.
* `attributes[]` - Jeder Wert der Attribute-Tabelle muss eine attribute_info-Struktur sein.




## Verweise

* [Das Klassendateiformat](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

