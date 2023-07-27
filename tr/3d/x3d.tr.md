{
  "date" : "2019-10-11",
  "keywords" :[ "x3d dosyası", "x3d dosya biçimi", "x3d dosyası nedir", "dosya", "x3d örneği", "x3d dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - 3D Görüntü Dosyası",
  "description":"X3D dosya formatı ve X3D dosyalarını açıp oluşturabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## X3D dosyası nedir?
X3D, 3D bilgilerin sunumu için [XML](/tr/web/xml/) tabanlı bir 3D grafik dosyası formatıdır. Modüler bir standarttır ve çeşitli ISO spesifikasyonları ile tanımlanır. Biçim, vektör ve raster grafikleri, saydamlığı, aydınlatma efektlerini ve döndürmeler, solmalar ve salınımlar dahil olmak üzere animasyon ayarlarını destekler. 2001'de [VRML](/tr/3d/vrml/) dosya biçiminin halefi oldu. X3D, modeli bir renk üzerine yazdırırken kullanılan renk bilgilerini kodlama avantajına sahiptir ([STL](/tr/cad/stl/))'den farklı olarak) 3 boyutlu yazıcı. Biçim, VRML'ye uzantılar içerir ve sahneyi bir XML sözdizimi ve VRML97'nin Open Inventor benzeri sözdizimi veya ikili biçimlendirme kullanarak kodlama yeteneği sağlar.

X3D (ISO/IEC 19775) için soyut belirtim, ilk olarak 2004 yılında ISO tarafından onaylandı. X3D (ISO/IEC 19776) için XML ve ClassicVRML kodlamaları ilk olarak 2005 yılında onaylandı.

## X3D Dosya Biçimi

X3D sahne dosyalarının ortak bir dosya yapısı vardır:

* Dosya başlığı (XML, ClassicVRML veya Sıkıştırılmış İkili)
* Sürüm ve profil öznitelikleri dahil olmak üzere X3D kök düğümünün başlangıcı
* Bileşen ve Meta ifadeleri içeren bir başlık bölümü (her ikisi de isteğe bağlıdır)
* X3D Scene grafiği ve alt düğümleri
* X3D kök düğümünün sonu

## X3D Dosya Biçimi Örneği

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

## Referanslar ##

* [X3D - Wikipedia Tarafından](https://en.wikipedia.org/wiki/X3D)
* [Web3D Konsorsiyumu resmi web sitesi](https://www.web3d.org/)
* [X3D resmi web sitesi](https://www.web3d.org/x3d/what-x3d)

