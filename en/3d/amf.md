{
  "date" : "2019-10-11",
  "keywords" : [ "amf", "amf file", "amf file format", "file format", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about AMF file format and APIs that can open and create AMF files.",
  "title" : "AMF - Additive Manufacturing File",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an AMF file?
An AMF file consists of guidelines for objects description in order to be used by Additive Manufacturing processes. It contains an opening <amf> XML tag and ends with a </amf> element. This is preceded by an XML declaration line specifying the XML version and encoding of the file. The declarations can include measurement units information and, in the absence of such information, millimetres are used as default unit.


## AMF File Format
Additive Manufacturing file format (**AMF**) defines open standards for objects description in order to be utilized by additive manufacturing processes such as 3D Printing. CAD programs use the AMF file format by making use of the information such as geometry, color and material of the objects. AMF is different than STL format as the lateral does not support color, materials, lattices, and constellations.



### Elements of an AMF File

The five top level elements defined with the <AMF> tags are as detailed below. The presence of a single object element is must for a fully functional AMF file.

`<object>` - The object element defines a volume or volumes of material, each of which are associated with a material ID for printing. At least one object element must be present in the file. Additional objects are optional.

`<material>` - The optional material element defines one or more materials for printing with an associated material ID. If no material element is included, a single default material is assumed.

`<texture>` - The optional texture element defines one or more images or textures for color or texture mapping, each with an associated texture ID.

`<constellation>`  - The optional constellation element hierarchically combines objects and other constellations into a relative pattern for printing.

`<metadata>` - The optional metadata element specifies additional information about the object(s) and elements contained in the file.

## AMF Example

Following is an example of AMF file that can be copied to a [text](word-processing/txt/) file and saved as compressed [zip](/compression/zip/) file for opening.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## References

 * [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
 * [AMF specifications on ISO](https://www.iso.org/standard/67472.html)
