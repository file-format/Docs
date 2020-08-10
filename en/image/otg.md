{
  "date" : "2020-01-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OTG",
  "linktitle" : "OTG",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2020-01-10"
}

An OTG file is a drawing template that is created using the OpenDocument standard that follows the OASIS Office Applications [1.0 specification](http://www.oasis-open.org/committees/download.php/12572/OpenDocument-v1.0-os.pdf). It represents the default organization of drawing elements for a vector image that can be used to further enhance the contents of the file. OTF files are like any other OpenDocument format based files that are based on XML format to represent the contents of the document. OTF files can be viewed by opening them in any text or standard XML editor.

## OTG File Format Specifications ##
OTG file format is based on the OpenDocument XML format that has well-established schema. The structure of each component of an OpenDocument format is represented by an element that has associated attributes and is common for all the document types such as text document, spreadsheet, or a drawing file. OTG, being a drawing template, extensively utilizes the Graphics Content specifications that includes:

  * Enhanced Page Features for Graphical Applications
  * Drawing Shapes
  * Frames
  * 3D Shapes
  * Custom Shape
  * Presentation Shapes
  * Presentation Animations
  * SMIL Presentation Animations
  * Presentation Events
  * Present Text Fields
  * Presentation Document Content

### Enhanced Page Features for Graphical Applications ###
#### Handout Master ####

Handout Master element is a template for automatically generating the handout pages for applications that support printing such pages.
The attributes that may be associated with the `<style:handout-master>` element are:

|Layout|Attribute|Description
---|---|---|
|Presentation Page Layout|presentation:presentation-page-layout-name|Links to `<style:presentation-page-layout>` attribute
|Page Layout|`style:page-layout-name` | Specifies a page layout which contains the sizes, border and orientation of the handout master page.
|Page Style|`draw:style-name`|Assigns an additional formatting attributes to a handout masterpage by assigning a drawing page style.|
|Header Declaration| `presentation:use-header-name`| Specifies the name of the header field declaration that is used for all header fields which are displayed on the handout master page.
|Footer Declaration| presentation:use-footer-name|Specifies the name of the footer field declaration that is used for all footer fields that are displayed on the handout master page.
|Date and Time Declaration|use-date-time-name|Specifies the name of the date-time field declaration that is used for all date-time fields that are displayed on the handout master page.

### Drawing Shapes ###
OpenDocument format supports several drawing shapes that can be used by any type of document.

|Shape|Associated Attributes| elements
---|---|---|
Rectangle - `<draw:rect>`|Position, Size, Style, Layer, Z-Index, ID, Caption ID, Text anchor, table background, draw end position, Round corners|Title, Long Description, Event Listeners, Glue Points, Text
Line `<draw:line>`|Style, Layer, Z-Index, ID, Caption ID and Transformation, Text anchor, table background, draw end position, Start point, End Point|Title, Long Description, Event Listeners, Glue Points, Text
Polyline `<draw:polyline>`| Position, Size, View box, Style, Layer, Z-Index, ID, Caption ID and Transformation, Text anchor, table background, draw end position, Points| Title, Long Description, Event Listeners, Glue Points, Text
Polygon `<draw:polygon>`|Position, Size, View box, Style, Layer, Z-Index, ID, Caption ID and Transformation, Text anchor, table background, draw end position, Points|Title, Long Description, Event Listeners, Glue Points, Text
|Regular Polygon `<draw:regular-polygon>`|Position, Size, Style, Layer, Z-Index, ID, Caption ID and Transformation, Text anchor, table background, draw end position, Concave, Corners, Sharpness|Title, Long Description, Event Listeners, Glue Points, Text
|Paht `<draw:path>`|Position, Size, View box, Style, Layer, Z-Index, ID, Caption ID and Transformation,Text anchor, table background, draw end position, Path data| Title, Long Description, Event Listeners, Glue Points, Text

### Frames ###
A frame, in a drawing document is a rectangular container that contains text boxes, images or objects. Frames support additional features such as contours, image maps, and hyperlinks. A frame may contain an object as well as an image, thus allowing to have multiple renditions of an object. The applications render respective element based on the best support.

Frames can contain:
  * Text boxes
  * Objects represented either in the OpenDocument format or in a object specific binary format
  * Images
  * Applets
  * Plug-ins
  * Floating frames

  A frame is contained in a document as shown below.

  ```
  <define name="draw-frame">
    <element name="draw:frame">
      <ref name="common-draw-shape-with-text-and-styles-attlist"/>
      <ref name="common-draw-position-attlist"/>
      <ref name="common-draw-rel-size-attlist"/>
      <ref name="common-draw-caption-id-attlist"/>
      <ref name="presentation-shape-attlist"/>
      <ref name="draw-frame-attlist"/>
      <zeroOrMore>
        <choice>
        <ref name="draw-text-box"/>
        <ref name="draw-image"/>
        <ref name="draw-object"/>
        <ref name="draw-object-ole"/>
        <ref name="draw-applet"/>
        <ref name="draw-floating-frame"/><ref name="draw-plugin"/>
        </choice>
      </zeroOrMore>
      <optional>
        <ref name="office-event-listeners"/>
      </optional>
      <zeroOrMore>
        <ref name="draw-glue-point"/>
      </zeroOrMore>
      <optional>
        <ref name="draw-image-map"/>
      </optional>
      <optional>
        <ref name="svg-title"/>
      </optional>
      <optional>
        <ref name="svg-desc"/>
      </optional>
      <optional>
        <choice>
          <ref name="draw-contour-polygon"/><ref name="draw-contour-path"/>
        </choice>
      </optional>
    </element>
  </define>
  ```

## References ##
* [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
* [OpenDocument Format - Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)
