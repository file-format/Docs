{
  "date" : "2019-10-11",
  "keywords" :[ "file x3d", "formato file x3d", "cos'è un file x3d", "file", "esempio x3d", "estensione file x3d", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - File immagine 3D",
  "description":"Scopri il formato di file X3D e le API che possono aprire e creare file X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file X3D?
X3D è un formato di file di grafica 3D basato su [XML](/it/web/xml/) per la presentazione di informazioni 3D. È uno standard modulare ed è definito attraverso diverse specifiche ISO. Il formato supporta grafica vettoriale e raster, trasparenza, effetti di luce e impostazioni di animazione tra cui rotazioni, dissolvenze e oscillazioni. È diventato il successore del formato di file [VRML](/it/3d/vrml/) nel 2001. X3D ha il vantaggio di codificare le informazioni sul colore (a differenza di [STL](/it/cad/stl/)) che vengono utilizzate durante la stampa del modello su un colore stampante 3d. Il formato presenta estensioni a VRML, fornendo la capacità di codificare la scena utilizzando una sintassi XML, nonché la sintassi simile a Open Inventor di VRML97 o la formattazione binaria.

La specifica astratta per X3D (ISO/IEC 19775) è stata approvata per la prima volta dall'ISO nel 2004. Le codifiche XML e ClassicVRML per X3D (ISO/IEC 19776) sono state approvate per la prima volta nel 2005.

## Formato file X3D

I file di scena X3D hanno una struttura di file comune:

* Intestazione del file (XML, ClassicVRML o binario compresso)
* Inizio del nodo radice X3D inclusi versione e attributi del profilo
* Una sezione principale con le istruzioni Component e Meta (entrambe facoltative)
* Il grafico della scena X3D e i suoi nodi figli
* Fine del nodo radice di X3D

## Esempio di formato file X3D

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

## Riferimenti ##

* [X3D - Di Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Sito ufficiale del Consorzio Web3D](http://www.web3d.org/)
* [sito ufficiale di X3D](http://www.web3d.org/x3d/what-x3d)

