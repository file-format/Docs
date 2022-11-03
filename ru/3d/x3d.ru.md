{
  "date" : "2019-10-11",
  "keywords" :[ "файл x3d", "формат файла x3d", "что такое файл x3d", "файл", "пример x3d", "расширение файла x3d", "расширение", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D — файл 3D-изображения",
  "description":"Узнайте о формате файлов X3D и API-интерфейсах, которые могут открывать и создавать файлы X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .X3D вариант №
X3D — это формат файла 3D-графики на основе [XML](/ru/web/xml/) для представления 3D-информации. Это модульный стандарт, определяемый несколькими спецификациями ISO. Формат поддерживает векторную и растровую графику, прозрачность, световые эффекты и настройки анимации, включая повороты, затухания и колебания. Он стал преемником файлового формата [VRML](/ru/3d/vrml/) в 2001 году. Преимущество X3D заключается в кодировании информации о цвете (в отличие от [STL](/ru/cad/stl/)), которая используется при печати модели на цветном 3д принтер. Формат имеет расширения для VRML, предоставляя возможность кодировать сцену с использованием синтаксиса XML, а также синтаксиса, подобного Open Inventor, в VRML97 или двоичного форматирования.

Абстрактная спецификация для X3D (ISO/IEC 19775) была впервые одобрена ISO в 2004 году. Кодировки XML и ClassicVRML для X3D (ISO/IEC 19776) были впервые одобрены в 2005 году.

## Формат файла X3D

Файлы сцен X3D имеют общую файловую структуру:

* Заголовок файла (XML, ClassicVRML или Compressed Binary)
* Начало корневого узла X3D, включая атрибуты версии и профиля.
* Раздел заголовка с операторами Component и Meta (оба необязательны)
* Граф сцены X3D и его дочерние узлы
* Конец корневого узла X3D

## Пример формата файла X3D

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

## Использованная литература ##

* [X3D — Википедия] (https://en.wikipedia.org/wiki/X3D)
* [Официальный сайт консорциума Web3D](http://www.web3d.org/)
* [Официальный сайт X3D] (http://www.web3d.org/x3d/what-x3d)

