{
  "date" : "2019-10-11",
  "keywords" :[ "x3d-bestand", "x3d-bestandsindeling", "wat is een x3d-bestand", "bestand", "x3d-voorbeeld", "x3d-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D-beeldbestand",
  "description":"Meer informatie over X3D-bestandsindelingen en API's die X3D-bestanden kunnen openen en maken.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een X3D-bestand?
X3D is een op [XML](/nl/web/xml/) gebaseerd 3D-grafisch bestandsformaat voor de presentatie van 3D-informatie. Het is een modulaire standaard en wordt gedefinieerd door verschillende ISO-specificaties. Het formaat ondersteunt vector- en rasterafbeeldingen, transparantie, lichteffecten en animatie-instellingen, waaronder rotaties, vervagingen en schommelingen. Het werd de opvolger van het [VRML](/nl/3d/vrml/) bestandsformaat in 2001. X3D heeft het voordeel kleurinformatie te coderen (in tegenstelling tot [STL](/nl/cad/stl/)) die wordt gebruikt tijdens het afdrukken van het model op een kleur 3D-printer. Het formaat bevat uitbreidingen op VRML, waardoor de scène kan worden gecodeerd met behulp van een XML-syntaxis en de Open Inventor-achtige syntaxis van VRML97 of binaire opmaak.

De abstracte specificatie voor X3D (ISO/IEC 19775) werd voor het eerst goedgekeurd door de ISO in 2004. De XML- en ClassicVRML-coderingen voor X3D (ISO/IEC 19776) werden voor het eerst goedgekeurd in 2005.

## X3D-bestandsindeling

X3D-scènebestanden hebben een gemeenschappelijke bestandsstructuur:

* Bestandskop (ofwel XML, ClassicVRML of Compressed Binary)
* Start van het X3D-rootknooppunt inclusief versie- en profielattributen
* Een kopsectie met Component- en Meta-statements (beide optioneel)
* De X3D-scènegrafiek en de onderliggende knooppunten
* Einde van het X3D-rootknooppunt

## Voorbeeld van X3D-bestandsindeling

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

## Referenties ##

* [X3D - Door Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Officiële website van het Web3D Consortium](http://www.web3d.org/)
* [X3D officiële website](http://www.web3d.org/x3d/what-x3d)

