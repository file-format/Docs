{
  "date" : "2019-10-11",
  "keywords" :[ "file x3d", "format file x3d", "apa itu file x3d", "file", "contoh x3d", "ekstensi file x3d", "ekstensi", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - File Gambar 3D",
  "description":"Pelajari tentang format file X3D dan API yang dapat membuka dan membuat file X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file X3D?
X3D adalah format file grafik 3D berbasis [XML](/id/web/xml/) untuk penyajian informasi 3D. Ini adalah standar modular dan ditentukan melalui beberapa spesifikasi ISO. Formatnya mendukung grafik vektor dan raster, transparansi, efek pencahayaan, dan pengaturan animasi termasuk rotasi, pemudaran, dan ayunan. Itu menjadi penerus format file [VRML](/id/3d/vrml/) pada tahun 2001. X3D memiliki keunggulan pengkodean informasi warna (tidak seperti [STL](/id/cad/stl/)) yang digunakan selama pencetakan model pada warna pencetak 3D. Format ini menampilkan ekstensi ke VRML, menyediakan kemampuan untuk menyandikan adegan menggunakan sintaks XML serta sintaks VRML97 atau pemformatan biner seperti Open Inventor.

Spesifikasi abstrak untuk X3D (ISO/IEC 19775) pertama kali disetujui oleh ISO pada tahun 2004. Pengkodean XML dan ClassicVRML untuk X3D (ISO/IEC 19776) pertama kali disetujui pada tahun 2005.

## Format File X3D

File adegan X3D memiliki struktur file yang umum:

* File header (baik XML, ClassicVRML, atau Compressed Binary)
* Mulai dari simpul akar X3D termasuk atribut versi dan profil
* Bagian kepala dengan pernyataan Komponen dan Meta (keduanya opsional)
* Grafik Adegan X3D dan node anaknya
* Akhir dari simpul akar X3D

## Contoh Format File X3D

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

## Referensi ##

* [X3D - Oleh Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Situs web resmi Konsorsium Web3D](http://www.web3d.org/)
* [Situs web resmi X3D](http://www.web3d.org/x3d/what-x3d)

