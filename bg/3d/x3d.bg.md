{
  "date" : "2019-10-11",
  "keywords" :[ "x3d файл", "x3d файлов формат", "какво е x3d файл", "файл", "x3d пример", "x3d файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - файл с 3D изображение",
  "description":"Научете за файловия формат X3D и API, които могат да отварят и създават X3D файлове.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Какво е X3D файл?
X3D е [XML](/bg/web/xml/) базиран 3D графичен файлов формат за представяне на 3D информация. Това е модулен стандарт и се дефинира чрез няколко ISO спецификации. Форматът поддържа векторни и растерни графики, прозрачност, светлинни ефекти и настройки за анимация, включително завъртане, избледняване и люлеене. Той стана наследник на файловия формат [VRML](/bg/3d/vrml/) през 2001 г. X3D има предимството да кодира информация за цвета (за разлика от [STL](/bg/cad/stl/)), която се използва по време на печат на модела върху цвят 3D принтер. Форматът разполага с разширения към VRML, предоставящи възможност за кодиране на сцената с помощта на XML синтаксис, както и подобен на Open Inventor синтаксис на VRML97 или двоично форматиране.

Абстрактната спецификация за X3D (ISO/IEC 19775) беше одобрена за първи път от ISO през 2004 г. XML и ClassicVRML кодировките за X3D (ISO/IEC 19776) бяха одобрени за първи път през 2005 г.

## X3D файлов формат

Файловете със сцени X3D имат обща файлова структура:

* Заглавка на файл (или XML, ClassicVRML, или компресиран двоичен)
* Старт на коренния възел на X3D, включително атрибути на версия и профил
* Главна секция с компонентни и мета изявления (и двете по избор)
* Графиката на X3D сцена и нейните дъщерни възли
* Край на коренния възел на X3D

## Пример за файлов формат X3D

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

## Препратки ##

* [X3D - от Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Официален уебсайт на консорциума Web3D](http://www.web3d.org/)
* [Официален уебсайт на X3D](http://www.web3d.org/x3d/what-x3d)

