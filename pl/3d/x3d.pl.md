{
  "date" : "2019-10-11",
  "keywords" :["plik x3d", "format pliku x3d", "co to jest plik x3d", "plik", "przykład x3d", "rozszerzenie pliku x3d","rozszerzenie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - plik obrazu 3D",
  "description":"Poznaj format plików X3D i API, które mogą otwierać i tworzyć pliki X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Czym jest plik X3D?
X3D to oparty na [XML](/pl/web/xml/) format pliku grafiki 3D do prezentacji informacji 3D. Jest to norma modułowa, zdefiniowana w kilku specyfikacjach ISO. Format obsługuje grafikę wektorową i rastrową, przezroczystość, efekty świetlne i ustawienia animacji, w tym obroty, zanikanie i wahania. W 2001 roku stał się następcą formatu pliku [VRML](/pl/3d/vrml/). X3D ma tę zaletę, że koduje informacje o kolorze (w przeciwieństwie do formatu [STL](/pl/cad/stl/)), który jest używany podczas drukowania modelu na kolorowym drukarka 3d. Format zawiera rozszerzenia VRML, zapewniając możliwość kodowania sceny przy użyciu składni XML, a także składni VRML97 podobnej do Open Inventor lub formatowania binarnego.

Abstrakcyjna specyfikacja dla X3D (ISO/IEC 19775) została po raz pierwszy zatwierdzona przez ISO w 2004 roku. Kodowanie XML i ClassicVRML dla X3D (ISO/IEC 19776) zostało po raz pierwszy zatwierdzone w 2005 roku.

## Format pliku X3D

Pliki scen X3D mają wspólną strukturę plików:

* Nagłówek pliku (XML, ClassicVRML lub skompresowany plik binarny)
* Początek węzła głównego X3D, w tym atrybuty wersji i profilu
* Sekcja nagłówka z instrukcjami Component i Meta (oba opcjonalne)
* Wykres sceny X3D i jego węzły potomne
* Koniec węzła głównego X3D

## Przykład formatu pliku X3D

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

## Bibliografia ##

* [X3D – z Wikipedii](https://en.wikipedia.org/wiki/X3D)
* [Oficjalna strona Web3D Consortium](http://www.web3d.org/)
* [Oficjalna witryna X3D](http://www.web3d.org/x3d/what-x3d)

