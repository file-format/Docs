{
  "date" : "2019-10-11",
  "keywords" :[ "файл x3d", "формат файлу x3d", "що таке файл x3d", "файл", "приклад x3d", "розширення файлу x3d", "розширення", "формат" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - файл 3D зображення",
  "description":"Дізнайтеся про формат файлу X3D та API, які можуть відкривати та створювати файли X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Що таке файл X3D?
X3D — це формат файлу 3D-графіки на основі [XML](/uk/web/xml/) для представлення 3D-інформації. Це модульний стандарт, який визначається кількома специфікаціями ISO. Формат підтримує векторну та растрову графіку, прозорість, світлові ефекти та параметри анімації, включаючи обертання, зникання та коливання. Він став наступником формату файлів [VRML](/uk/3d/vrml/) у 2001 році. X3D має перевагу кодування інформації про колір (на відміну від [STL](/uk/cad/stl/)), яка використовується під час друку моделі на кольоровому 3D принтер. Цей формат має розширення для VRML, надаючи можливість кодувати сцену за допомогою синтаксису XML, а також синтаксису VRML97, схожого на Open Inventor, або двійкового форматування.

Абстрактна специфікація для X3D (ISO/IEC 19775) була вперше схвалена ISO в 2004 році. Кодування XML і ClassicVRML для X3D (ISO/IEC 19776) були вперше затверджені в 2005 році.

## Формат файлу X3D

Файли сцен X3D мають загальну файлову структуру:

* Заголовок файлу (XML, ClassicVRML або Compressed Binary)
* Початок кореневого вузла X3D, включаючи атрибути версії та профілю
* Головний розділ із операторами Component і Meta (обидва необов’язкові)
* Граф сцени X3D та його дочірні вузли
* Кінець кореневого вузла X3D

## Приклад формату файлу X3D

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

## Посилання ##

* [X3D - Вікіпедія](https://en.wikipedia.org/wiki/X3D)
* [Офіційний веб-сайт консорціуму Web3D](https://www.web3d.org/)
* [Офіційний веб-сайт X3D](https://www.web3d.org/x3d/what-x3d)

