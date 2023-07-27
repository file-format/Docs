{
  "date" : "2019-10-11",
  "keywords" :[ "x3d-fil", "x3d-filformat", "vad är en x3d-fil", "fil", "x3d-exempel", "x3d-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D-bildfil",
  "description":"Läs mer om X3D-filformat och API:er som kan öppna och skapa X3D-filer.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en X3D fil?
X3D är ett [XML](/sv/web/xml/)-baserat 3D-grafikfilformat för presentation av 3D-information. Det är en modulär standard och definieras genom flera ISO-specifikationer. Formatet stöder vektor- och rastergrafik, genomskinlighet, ljuseffekter och animationsinställningar inklusive rotationer, toningar och svängningar. Det blev efterföljare till filformatet [VRML](/sv/3d/vrml/) 2001. X3D har fördelen av att koda färginformation (till skillnad från [STL](/sv/cad/stl/)) som används vid utskrift av modellen på en färg 3d skrivare. Formatet har tillägg till VRML, vilket ger möjligheten att koda scenen med en XML-syntax såväl som den Open Inventor-liknande syntaxen för VRML97 eller binär formatering.

Den abstrakta specifikationen för X3D (ISO/IEC 19775) godkändes först av ISO 2004. XML- och ClassicVRML-kodningarna för X3D (ISO/IEC 19776) godkändes först 2005.

## X3D filformat

X3D-scenfiler har en gemensam filstruktur:

* Filhuvud (antingen XML, ClassicVRML eller Compressed Binary)
* Start av X3D-rotnoden inklusive versions- och profilattribut
* En huvudsektion med komponent- och metasatser (båda valfria)
* X3D-scengrafen och dess undernoder
* Slutet på X3D-rotnoden

## Exempel på X3D-filformat

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
    <meta content#'Simple X3D example' name#'description'/>,
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

## Referenser ##

* [X3D - av Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Web3D Consortium officiella webbplats](https://www.web3d.org/)
* [X3D officiella webbplats](https://www.web3d.org/x3d/what-x3d)

