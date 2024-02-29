{
  "date": "2019-10-11",
  "keywords": [
"فایل x3d",
"فرمت فایل x3d",
"فایل x3d چیست",
"فایل",
"مثال x3d",
"پسوند فایل x3d",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X3D - فایل تصویری سه بعدی",
  "description": "درباره فرمت فایل X3D و API هایی که می توانند فایل های X3D را باز کرده و ایجاد کنند، بیاموزید.",
  "linktitle": "X3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-x3d"
}
},
  "lastmod": "2019-09-10"
}

## فایل X3D چیست؟
X3D is an [XML](/web/xml/) based 3D graphics file format for presentation of 3D information. It is a modular standard and is defined through several ISO specifications. The format supports vector and raster graphics, transparency, lighting effects, and animation settings including rotations, fades, and swings. It became successor of [VRML](/3d/vrml/) file format in 2001. X3D دارای مزیت رمزگذاری اطلاعات رنگی است (برخلاف [STL](/cad/stl/)) که در حین چاپ مدل بر روی چاپگر سه بعدی رنگی استفاده می شود. این فرمت دارای پسوندهایی برای VRML است که قابلیت رمزگذاری صحنه را با استفاده از نحو XML و همچنین دستور Open Inventor مانند VRML97 یا قالب‌بندی باینری ارائه می‌دهد.

The abstract specification for X3D (ISO/IEC 19775) was first approved by the ISO in 2004. کدهای XML و ClassicVRML برای X3D (ISO/IEC 19776) اولین بار در سال 2005 تایید شدند.

## فرمت فایل X3D

فایل های صحنه X3D یک ساختار فایل مشترک دارند:

* هدر فایل (XML، ClassicVRML، یا باینری فشرده)

* شروع گره ریشه X3D شامل ویژگی های نسخه و نمایه

* بخش سر با کامپوننت و عبارات متا (هر دو اختیاری)

* نمودار صحنه X3D و گره های فرزند آن

* انتهای گره ریشه X3D


## نمونه فرمت فایل X3D

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
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'-fa/>
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

## منابع ##

* [X3D - توسط Wikipedia](https://en.wikipedia.org/wiki/X3D)

* [وب سایت رسمی کنسرسیوم Web3D] (https://www.web3d.org/)

* [وب سایت رسمی X3D] (https://www.web3d.org/x3d/what-x3d)


