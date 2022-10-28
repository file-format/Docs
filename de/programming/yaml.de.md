{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml", "was ist eine yaml-Datei", "wie man eine yaml-Datei öffnet", "Erweiterung", "Datei", "yaml-Datei", "yaml-Dateiformat", ".yaml-Erweiterung" , "yaml vs. json" , "YAML-Dateibeispiel", "docker yaml-Dateibeispiel"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" Erfahren Sie mehr über das YAML-Dateiformat und APIs, die eine YAML-Datei erstellen und öffnen können.",
  "title" :"YAML-Dateiformat",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Was ist eine YAML-Datei? ##

**YAML-Datei** besteht aus einer Sprache YAML (YAML Ain't Markup Language), die eine Unicode-basierte Datenserialisierungssprache ist; Wird für Konfigurationsdateien, Internet-Messaging, Objektpersistenz usw. verwendet. YAML verwendet die Erweiterung .yaml für seine Dateien. Seine Syntax ist unabhängig von einer bestimmten Programmiersprache. Grundsätzlich ist YAML für die menschliche Interaktion konzipiert und funktioniert gut mit modernen Programmiersprachen. Die Unterstützung für die Serialisierung beliebiger nativer Datenstrukturen hat die Lesbarkeit der YAML-Dateien verbessert, aber den Parsing- und Dateigenerierungsprozess etwas komplizierter gemacht.

## Kurze Geschichte ##

YAML wurde erstmals 2001 vorgeschlagen und von Clark Evans, Ingy döt Net und Oren Ben-Kiki entwickelt. YAML wurde zuerst als "Yet Another Markup Language" bezeichnet, um seinen Zweck als Auszeichnungssprache anzuzeigen. Es wurde später als "YAML Aint Markup Language" umbenannt, um seinen Zweck als datenorientiert anzuzeigen.


## YAML-Dateiformat ##

Die YAML-Datei besteht aus den folgenden Datentypen

- **Skalare**: Skalare sind Werte wie Strings, Integers, Booleans usw.
- **Sequenzen**: Sequenzen sind Listen, bei denen jedes Element mit einem Bindestrich (-) beginnt. Listen können auch verschachtelt werden.
- **Mappings**: Mapping gibt die Möglichkeit, Schlüssel mit Werten aufzulisten.

### Syntax ###

- **Whitespace**: Whitespace-Einrückungen werden verwendet, um die Verschachtelung und die Gesamtstruktur anzuzeigen.

„Yaml
Name: John Smith
Kontakt:
Zuhause: 1012355532
Büro: 5002586256
die Anschrift:
Straße: |
123 Tornado-Gasse
Suite 16
Stadt: East Centerville
Zustand: KS
```

- **Kommentare**: Kommentare beginnen mit dem "#"-Symbol.

„Yaml
# Dies ist ein YAML-Kommentar
```

- **Listen**: Bindestrich (-) wird verwendet, um Listenmitglieder anzugeben, wobei jedes Mitglied in einer separaten Zeile steht. Listenelemente können auch in eckige Klammern ([...]) eingeschlossen werden, wobei Elemente durch Kommas (,) getrennt werden.

„Yaml
  - A
  - B
  - C
```

„Yaml
[A, B, C]
```

- **Assoziatives Array**: Ein assoziatives Array wird von geschweiften Klammern ({...}) umgeben. Die Schlüssel und Werte werden durch einen Doppelpunkt (:) und jedes Paar durch ein Komma (,) getrennt.

„Yaml
  {name: John Smith, age: 20}
```

- **Strings**: Strings können mit oder ohne Anführungszeichen (") oder einfachen Anführungszeichen (') geschrieben werden.

„Yaml
Beispielzeichenfolge
"Beispielzeichenfolge"
'Beispielzeichenfolge'
```

- **Skalarer Blockinhalt**: Skalarer Inhalt kann in Blocknotation geschrieben werden, indem man Folgendes verwendet:
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

„Yaml
Daten: |
YAML
(YAML ist keine Auszeichnungssprache)
ist eine Datenserialisierungssprache
```

„Yaml
Daten: ?
YAML (YAML ist keine Auszeichnungssprache)
ist eine Datenserialisierungssprache
```

- **Mehrere Dokumente**: Mehrere Dokumente werden in einem einzelnen Stream durch drei Bindestriche (---) getrennt. Bindestriche geben den Beginn des Dokuments an. Bindestriche werden auch verwendet, um Anweisungen vom Dokumentinhalt zu trennen. Das Ende des Dokuments wird durch drei Punkte (...) angezeigt.

„Yaml
  ---
Dokument 1
  ---
Dokument 2
...
```

- **Typ**: Um den Werttyp anzugeben, werden doppelte Ausrufezeichen (!!) verwendet.

„Yaml
a: !!float 123
b: !!str 123
```

- **Tag**: Um einer Notiz ein Tag zuzuweisen, wird ein kaufmännisches Und (&) verwendet und um auf diesen Knoten zu verweisen, wird ein Sternchen (*) verwendet.

„Yaml
Name: John Smith
Rechnungsempfänger: &id01
Straße: |
123 Tornado-Gasse
Suite 16
Stadt: East Centerville
Zustand: KS

Versandadresse: *id01
```

- **Direktiven**: YAML-Dokumenten können Direktiven in einem Stream vorangestellt werden. Direktiven beginnen mit einem Prozentzeichen (%), gefolgt vom Namen und den durch Leerzeichen getrennten Parametern.

„Yaml
%YAML 1.2
  ---
Dokumentinhalt
```
## Beispiel für eine YAML-Datei
Hier sehen Sie unten ein **Beispiel für eine Docker-YAML-Datei**:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs. JSON
Grundsätzlich wurden sowohl JSON als auch YAML entwickelt, um ein für Menschen lesbares Datenaustauschformat bereitzustellen. Das YAML ist als Obermenge des JSON-Formats realisiert. Das bedeutet, dass wir JSON mit einem YAML-Parser parsen können. Obwohl die praktische Umsetzung dieser Theorie wenig knifflig ist. Daher werden im Folgenden einige grundlegende Unterschiede zwischen YAML und JSON aufgeführt:

|YAML| JSON|
---|---|
|Komplexer und zeitaufwändiger Prozess zum Parsen serialisierter Daten |Parsen Sie JSON-serialisierte Daten schnell und einfach mit ihrem einfacheren Design|
|Weniger Community-Unterstützung| Größere Community-Unterstützung und Popularität|
|Unterstützt Kommentare| Unterstützt keine Kommentare|
|Fähigkeit, Verweise auf andere Datenobjekte zu verwenden| Unmöglich, komplexe Strukturen mit Objektreferenzen zu serialisieren|
|Hierarchie wird durch doppelte Leerzeichen gekennzeichnet. Tabulatorzeichen sind nicht erlaubt|Objekte und Arrays werden in geschweiften und eckigen Klammern angegeben.|
|String-Anführungszeichen sind optional, es werden jedoch einfache und doppelte Anführungszeichen unterstützt.|Strings müssen in doppelten Anführungszeichen stehen.|
|Root-Knoten kann jeder der gültigen Datentypen sein|Root-Knoten muss entweder ein Array oder ein Objekt sein.|


## Verweise ##

- [YAML - Wikipedia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

