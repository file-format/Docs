{
  "date" : "2019-10-11",
  "keywords" :[ "soubor x3d", "formát souboru x3d", "co je soubor x3d", "soubor", "příklad x3d", "přípona souboru x3d", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D obrazový soubor",
  "description":"Další informace o formátu souboru X3D a rozhraních API, která mohou otevírat a vytvářet soubory X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor X3D?
X3D je formát 3D grafického souboru založený na [XML](/cs/web/xml/) pro prezentaci 3D informací. Jedná se o modulární standard a je definován prostřednictvím několika specifikací ISO. Formát podporuje vektorovou a rastrovou grafiku, průhlednost, světelné efekty a nastavení animací včetně rotací, vyblednutí a výkyvů. V roce 2001 se stal nástupcem formátu souboru [VRML](/cs/3d/vrml/). X3D má výhodu v kódování barevné informace (na rozdíl od [STL](/cs/cad/stl/)), která se používá při tisku modelu na barvu. 3D tiskárna. Tento formát obsahuje rozšíření VRML, které poskytuje možnost kódovat scénu pomocí syntaxe XML, stejně jako syntaxe VRML97 podobné Open Inventoru nebo binárního formátování.

Abstraktní specifikace pro X3D (ISO/IEC 19775) byla poprvé schválena ISO v roce 2004. Kódování XML a ClassicVRML pro X3D (ISO/IEC 19776) bylo poprvé schváleno v roce 2005.

## Formát souboru X3D

Soubory scén X3D mají společnou strukturu souborů:

* Záhlaví souboru (buď XML, ClassicVRML nebo komprimované binární)
* Začátek kořenového uzlu X3D včetně atributů verze a profilu
* Sekce hlavy s příkazy Component a Meta (obojí volitelné)
* Graf X3D scény a jeho podřízené uzly
* Konec kořenového uzlu X3D

## Příklad formátu souboru X3D

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

## Reference ##

* [X3D – z Wikipedie](https://en.wikipedia.org/wiki/X3D)
* [Oficiální stránky Web3D Consortium](https://www.web3d.org/)
* [oficiální webové stránky X3D](https://www.web3d.org/x3d/what-x3d)

