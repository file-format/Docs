{
  "date" : "2019-10-11",
  "keywords" :[ "x3d-Datei", "x3d-Dateiformat", "was ist eine x3d-Datei", "Datei", "x3d-Beispiel", "x3d-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D-Bilddatei",
  "description":"Erfahren Sie mehr über das X3D-Dateiformat und APIs, die X3D-Dateien öffnen und erstellen können.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine X3D-Datei?
X3D ist ein auf [XML](/de/web/xml/) basierendes 3D-Grafikdateiformat zur Darstellung von 3D-Informationen. Es ist ein modularer Standard und wird durch mehrere ISO-Spezifikationen definiert. Das Format unterstützt Vektor- und Rastergrafiken, Transparenz, Lichteffekte und Animationseinstellungen, einschließlich Drehungen, Überblendungen und Schwenks. Es wurde 2001 Nachfolger des Dateiformats [VRML](/de/3d/vrml/). X3D hat den Vorteil, dass es Farbinformationen (im Gegensatz zu [STL](/de/cad/stl/)) kodiert, die beim Drucken des Modells auf eine Farbe verwendet werden 3D Drucker. Das Format bietet Erweiterungen zu VRML und bietet die Möglichkeit, die Szene mit einer XML-Syntax sowie der Open Inventor-ähnlichen Syntax von VRML97 oder binärer Formatierung zu codieren.

Die abstrakte Spezifikation für X3D (ISO/IEC 19775) wurde erstmals 2004 von der ISO genehmigt. Die XML- und ClassicVRML-Codierungen für X3D (ISO/IEC 19776) wurden erstmals 2005 genehmigt.

## X3D-Dateiformat

X3D-Szenendateien haben eine gemeinsame Dateistruktur:

* Dateiheader (entweder XML, ClassicVRML oder Compressed Binary)
* Beginn des X3D-Wurzelknotens einschließlich Versions- und Profilattributen
* Ein Head-Abschnitt mit Component- und Meta-Anweisungen (beides optional)
* Der X3D-Szenengraph und seine untergeordneten Knoten
* Ende des X3D-Wurzelknotens

## Beispiel ##

```
<!-- -------------------- X3D header and X3D root node with profile declaration -->
<!DOCTYPE X3D PUBLIC "ISO//Web3D//DTD X3D 3.2//EN"
                     "http://www.web3d.org/specifications/x3d-3.2.dtd">
<X3D profile#'Immersive' version#'3.2'
     xmlns:xsd#'http://www.w3.org/2001/XMLSchema-instance'
     xsd:noNamespaceSchemaLocation#'http://www.web3d.org/specifications/x3d-3.2.xsd'>

<!-- -------------------- head section with included meta data -->
  <head>
    <meta content#'HelloWorld.x3d' name#'title'/>
    <meta content#'Simple X3D example' name#'description'/>
    <meta content#'30 October 2000' name#'created'/>
    <meta content#'7 August 2010' name#'modified'/>
    <meta content#'Don Brutzman' name#'creator'/>
    <meta content#'http://www.web3D.org' name#'reference'/>
    <meta content#'http://x3dGraphics.com' name#'reference'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorldTall.png' name#'image'/>
    <meta content#'http://www.web3d.org/x3d/content/examples/license.html' name#'license'/>
    <meta content#'X3D-Edit 3.2, https://savage.nps.edu/X3D-Edit' name#'generator'/>
  </head>

<!-- -------------------- the X3D scene node with X3D nodes -->
  <Scene>
    <!-- Example scene to illustrate X3D nodes and fields (XML elements and attributes) -->
    <Group>
      <Viewpoint centerOfRotation#'0 -1 0' description#'Hello world!' position#'0 -1 7'/>
      <Transform rotation#'0 1 0 3'>
        <Shape>
          <Sphere/>
          <Appearance>
            <Material diffuseColor#'0 0.5 1'/>
            <ImageTexture url#'"earth-topo.png" "earth-topo.jpg" "earth-topo-small.gif"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.png"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo.jpg"
     "http://www.web3d.org/x3d/content/examples/Basic/earth-topo-small.gif"'/>
          </Appearance>
        </Shape>
      </Transform>
      <Transform translation#'0 -2 0'>
        <Shape>
          <Text string#'"Hello" "world!"'>
            <FontStyle justify#'"MIDDLE" "MIDDLE"'/>
          </Text>
          <Appearance>
            <Material diffuseColor#'0.1 0.5 1'/>
          </Appearance>
        </Shape>
      </Transform>
    </Group>
  </Scene>

<!-- -------------------- footer, closing X3D toot element -->
</X3D>
```

## Verweise ##

* [X3D – von Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Offizielle Website des Web3D-Konsortiums](http://www.web3d.org/)
* [Offizielle X3D-Website] (http://www.web3d.org/x3d/what-x3d)

