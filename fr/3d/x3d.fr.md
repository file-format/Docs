{
  "date" : "2019-10-11",
  "keywords" :[ "fichier x3d", "format de fichier x3d", "qu'est-ce qu'un fichier x3d", "fichier", "exemple x3d", "extension de fichier x3d","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X3D - Fichier d'image 3D",
  "description":"En savoir plus sur le format de fichier X3D et les API qui peuvent ouvrir et créer des fichiers X3D.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Qu'est-ce qu'un fichier X3D ?
X3D est un format de fichier graphique 3D basé sur [XML](/fr/web/xml/) pour la présentation d'informations 3D. Il s'agit d'une norme modulaire définie par plusieurs spécifications ISO. Le format prend en charge les graphiques vectoriels et raster, la transparence, les effets d'éclairage et les paramètres d'animation, y compris les rotations, les fondus et les balançoires. Il est devenu le successeur du format de fichier [VRML](/fr/3d/vrml/) en 2001. X3D a l'avantage d'encoder les informations de couleur (contrairement à [STL](/fr/cad/stl/)) qui sont utilisées lors de l'impression du modèle sur une couleur Imprimante 3D. Le format comporte des extensions de VRML, offrant la possibilité d'encoder la scène à l'aide d'une syntaxe XML ainsi que la syntaxe de type Open Inventor de VRML97 ou le formatage binaire.

La spécification abstraite pour X3D (ISO/IEC 19775) a été approuvée pour la première fois par l'ISO en 2004. Les codages XML et ClassicVRML pour X3D (ISO/IEC 19776) ont été approuvés pour la première fois en 2005.

## Format de fichier X3D

Les fichiers de scène X3D ont une structure de fichier commune :

* En-tête de fichier (soit XML, ClassicVRML ou binaire compressé)
* Début du nœud racine X3D, y compris les attributs de version et de profil
* Une section d'en-tête avec des instructions Component et Meta (toutes deux facultatives)
* Le graphique Scène X3D et ses nœuds enfants
* Fin du nœud racine X3D

## Exemple de format de fichier X3D

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

## Références ##

* [X3D - Par Wikipédia](https://en.wikipedia.org/wiki/X3D)
* [Site officiel du Consortium Web3D](http://www.web3d.org/)
* [Site officiel de X3D] (http://www.web3d.org/x3d/what-x3d)

