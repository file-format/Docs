{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "X3D - 3D Image File",
  "description":"Learn about X3D file format and APIs that can open and create X3D files.",
  "linktitle" : "X3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

X3D is an [XML](/web/xml/) based 3D graphics file format for presentation of 3D information. It is a modular standard and is defined through several ISO specifications. The format supports vector and raster graphics, transparency, lighting effects, and animation settings including rotations, fades, and swings. It became successor of [VRML](/3d/vrml/) file format in 2001. X3D has the advantage of encoding colour information (unlike [STL](/cad/stl/)) that is used during printing the model on a colour 3D printer. The format features extensions to VRML, providing the capability to encode the scene using an XML syntax as well as the Open Inventor-like syntax of VRML97 or binary formatting.

The abstract specification for X3D (ISO/IEC 19775) was first approved by the ISO in 2004. The XML and ClassicVRML encodings for X3D (ISO/IEC 19776) were first approved in 2005.

## X3D File Structure ##

X3D scene files have a common file structure:

* File header (either XML, ClassicVRML, or Compressed Binary)
* Start of the X3D root node including version and profile attributes
* A head section with Component and Meta statements (both optional)
* The X3D Scene graph and its child nodes
* End of the X3D root node

## Example ##

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

## References ##

* [X3D - By Wikipedia](https://en.wikipedia.org/wiki/X3D)
* [Web3D Consortium official website](http://www.web3d.org/)
* [X3D official website](http://www.web3d.org/x3d/what-x3d)
