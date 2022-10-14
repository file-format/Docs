{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf-Datei", "amf-Dateiformat", "Dateiformat", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das AMF-Dateiformat und APIs, die AMF-Dateien öffnen und erstellen können.",
  "title" :"AMF - Datei für additive Fertigung",
  "linktitle" :"AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine AMF-Datei?
Eine AMF-Datei besteht aus Richtlinien für die Beschreibung von Objekten, die von Additive Manufacturing-Prozessen verwendet werden sollen. Es enthält eine Öffnung<amf> XML-Tag und endet mit a</amf> Element. Davor steht eine XML-Deklarationszeile, die die XML-Version und Kodierung der Datei angibt. Die Deklarationen können Angaben zu Maßeinheiten enthalten, und wenn solche Angaben fehlen, werden Millimeter als Standardeinheit verwendet.


## AMF-Dateiformat
Das Dateiformat für additive Fertigung (**AMF**) definiert offene Standards für die Objektbeschreibung, um von additiven Fertigungsverfahren wie dem 3D-Druck verwendet zu werden. CAD-Programme verwenden das AMF-Dateiformat, indem sie Informationen wie Geometrie, Farbe und Material der Objekte verwenden. AMF unterscheidet sich vom STL-Format, da das Seitenformat keine Farben, Materialien, Gitter und Konstellationen unterstützt.



### Elemente einer AMF-Datei

Die fünf Elemente der obersten Ebene, die mit definiert sind<AMF> Tags sind wie unten beschrieben. Das Vorhandensein eines einzelnen Objektelements ist ein Muss für eine voll funktionsfähige AMF-Datei.

`<object> ` - Das Objektelement definiert ein oder mehrere Materialvolumen, von denen jedes mit einer Material-ID zum Drucken verknüpft ist. Mindestens ein Objektelement muss in der Datei vorhanden sein. Zusätzliche Objekte sind optional.

`<material> ` - Das optionale Materialelement definiert ein oder mehrere Materialien zum Drucken mit einer zugehörigen Material-ID. Wenn kein Materialelement enthalten ist, wird ein einzelnes Standardmaterial angenommen.

`<texture> ` - Das optionale Texturelement definiert ein oder mehrere Bilder oder Texturen für die Farb- oder Texturabbildung, jedes mit einer zugehörigen Textur-ID.

`<constellation> ` - Das optionale Konstellationselement kombiniert hierarchisch Objekte und andere Konstellationen in einem relativen Muster zum Drucken.

`<metadata> ` - Das optionale Metadatenelement gibt zusätzliche Informationen über die in der Datei enthaltenen Objekte und Elemente an.

## AMF-Beispiel

Nachfolgend sehen Sie ein Beispiel für eine AMF-Datei, die in eine [Text](/de/word-processing/txt/)-Datei kopiert und zum Öffnen als komprimierte [ZIP](/de/compression/zip/)-Datei gespeichert werden kann.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Verweise

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [AMF-Spezifikationen auf ISO](https://www.iso.org/standard/67472.html)

