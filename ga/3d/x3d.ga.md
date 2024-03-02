{
  "date": "2019-10-11",
  "keywords": [
"Comhad x3d",
"Formáid comhaid x3d saor in aisce,",
"Cad é an comhad x3d saor in aisce,",
"comhad",
"Sampla x3d",
"Síneadh comhad x3d saor in aisce,",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "X3D - Comhad Íomhá 3D",
  "description": "Foghlaim faoi fhormáid comhaid X3D agus APIs is féidir comhaid X3D a oscailt agus a chruthú.",
  "linktitle": "X3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-x3d"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad X3D ann?
X3D is an [XML](/web/xml/) based 3D graphics file format for presentation of 3D information. It is a modular standard and is defined through several ISO specifications. The format supports vector and raster graphics, transparency, lighting effects, and animation settings including rotations, fades, and swings. It became successor of [VRML](/3d/vrml/) file format in 2001. Tá sé de bhuntáiste ag X3D faisnéis datha a ionchódú (murab ionann agus [STL](/cad/stl/)) a úsáidtear le linn an tsamhail a phriontáil ar phrintéir datha 3D. Tá síntí ar VRML san fhormáid, rud a sholáthraíonn an cumas an radharc a ionchódú ag baint úsáide as comhréir XML chomh maith le comhréir VRML97 cosúil le Open Aireagóir nó formáidiú dénártha.

The abstract specification for X3D (ISO/IEC 19775) was first approved by the ISO in 2004. Faomhadh na hionchóduithe XML agus ClassicVRML do X3D (ISO/IEC 19776) den chéad uair in 2005.

## Formáid Comhaid X3D

Tá struchtúr comhaid coitianta ag comhaid radhairc X3D:

* Ceanntásc comhaid (XML, ClassicVRML, nó Dénártha Comhbhrúite)

* Tús an fhréamh nód X3D lena n-áirítear leagan agus tréithe próifíl

* Ceann ceann le ráitis Comhpháirte agus Meta (an dá cheann roghnach)

* An graf Radharc X3D agus a nóid linbh

* Deireadh an fhréamh nód X3D


## X3D Sampla Formáid Comhaid

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
    <meta content#'http://www.web3d.org/x3d/content/examples/HelloWorld.x3d' name#'identifier'-ga/>
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

## Tagairtí ##

* [X3D - Le Vicipéid]( https://ga.wikipedia.org/wiki/X3D)

* [láithreán gréasáin oifigiúil Web3D Consortium](https://www.web3d.org/)

* [láithreán gréasáin oifigiúil X3D](https://www.web3d.org/x3d/what-x3d)


