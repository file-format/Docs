{
  "date" : "2020-01-11",
  "keywords" :[ "x-Datei", "x-Dateiformat", "was ist eine x-Datei", "Datei", "x-Beispiel", "x-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0-Dateiformat",
  "description":"Erfahren Sie mehr über das DirectX X-Dateiformat und APIs, die DirectX X-Dateien öffnen und erstellen können.",
  "linktitle" :"X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Was ist eine X-Datei?

Eine Datei mit der Erweiterung .x bezieht sich auf [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics Legacy-Dateiformat, das mit Microsoft DirectX 2.0 eingeführt wurde. Es wurde zum Rendern von 3D-Grafiken in Spielen verwendet und gibt die Strukturen für Meshes, Texturen, Animationen und benutzerdefinierte Objekte an. Es ist seit 2014 veraltet, da das Autodesk FBX-Dateiformat besser als moderneres Format dient. X ist Template-getrieben und frei von jeglichem Nutzungswissen. Sie können DirectX X-Dateien mit Microsoft DirectX und gängigen Texteditoren öffnen.

## X-Dateiformat

Die [X-Dateireferenz](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) enthält Referenzinformationen für die verwendeten API-Elemente mit DirectX .x-Dateien arbeiten. Das Format stellt Datengrundelemente auf niedriger Ebene bereit, die von anderen Anwendungen verwendet werden, um Grundelemente auf höherer Ebene durch Datenvorlagen zu definieren. DirectX 6.0 führte Schnittstellen und Methoden ein, die das Lesen und Schreiben in .x-Dateien ermöglichen. DirectX 3.0 führte eine binäre Version dieses Dateiformats ein.

Die von DirectX 9 definierte [X-Dateiformatreferenz](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) enthält Referenzinformationen für .x Dateien sowohl in Binär- als auch in Textkodierungen.

### Binäre Kodierung

Das [Binärformat](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) definiert das DirectX X-Format als eine tokenisierte Darstellung des Textformats. Diese Token können eigenständig sein, um eine grammatikalische Struktur zu geben, oder sie können datensatztragende Token sein, die die notwendigen Daten liefern.

#### Header

Der binäre Header kann mit den folgenden Definitionen gelesen und geschrieben werden.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Textentschlüsselung

DirectX .x-Dateien hängen nicht davon ab, wie die Datei verwendet wird, und sind nicht spezifisch für eine Anwendung. Dieser vorlagengesteuerte Ansatz ermöglicht die Verwendung des .x-Dateiformats durch jede Client-Anwendung.


#### Header

Der Header mit variabler Länge ist obligatorisch und muss am Anfang des Datenstroms stehen. Der Header enthält die folgenden Daten.

|Typ |Untertyp |Größe |Inhalt |Bedeutung des Inhalts|
---|---|---|---|---|
|Magische Zahl (erforderlich)| | 4 Bytes |xof |
|Versionsnummer (erforderlich) |Hauptnummer |2 Bytes |03 |Hauptversion 3|
| |Minor-Nummer |2 Bytes |02 |Minor-Version 2|
|Formattyp (erforderlich)| |4 Bytes |"txt " |Textdatei|
| | | |"bin "| Binärdatei|
| | | |"zip"| Komprimierte MSZip-Textdatei |
| | | |"bzip"| Komprimierte MSZip-Binärdatei|
|Schwimmergröße (erforderlich)| |4 Bytes| 0064| 64-Bit-Gleitkommazahlen|
| | | |0032 |32-Bit-Gleitkommazahlen|


## Verweise

* [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9-Dateiformatreferenz](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

