{
  "date" : "2020-03-16",
  "keywords" : [ "IGES File", "File Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about IGES file format and APIs that can create and open IGES files.",
  "title" : "IGES File Format",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2020-07-28"
}

## What is an IGES file?

A file with .iges extension is used to exchange design information between computer-aided design (CAD) applications. IGES stands for Initial Graphics Exchange Specifications. Information exchanged using IGES includes circuit diagram, wireframe, freeform surface, or solid modeling representations. IGES finds its applications in traditional engineering drawings, models analysis, and manufacturing functions. The format can exchange both 2D or 3D design information between CAD programs. IGES files can be opened with several CAD applications such as Autodesk and CADSoftTools ABViewer. There are also several APIs available to open and convert IGES files programmatically.

## File Format

IGES files are in ASCII text format and can be opened in any text editor to view the contents of the file. Textual information in an IGES file is represented in "Hollerith" format. A common IGES file can contain thousands of lines to represent the 2D or 3D information that can be exchanged as per this format. An IGES file is split into five sections, denoted by the specific upper case letter in the 73rd column. Those sections are `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P), and `Terminate` (T) sections. The Data Entry and Parameter Data sections are commonly abbreviated DE and PD, respectively.

### File Header

The Start and Global sections contain basic information about:
 * Name of the file and its source
 * Delimiters for the Parameter Data section
 * Author of the file, and other general information.

Start and Global sections from the example document on Wikipedia are as follow.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Data Entry (DE) and Parameter Data (PD) Section

#### Data Entry Section
An IGES file consists of several entities that contains the information on the basic data of the IGES file format. An entity contains information about different elements of an IGES data format and is used for drawing.  More commonly used entities include:
 * Circular Arc
 * Composite Curve
 * Conic Arc
 * Plane
 * Line

These are just a few and there are around 150 different entities in in IGES. Each entity is identified by a Type number such as:
 * CIRCULAR ARC(Type 100)
 * LINE (Type 110)

##### Entity Properties

Each declared entity has the following properties.

|Field Name|Description|
---|---|
|Entity Type |This is the type of entity being described. For example, 116 describes a Point entity.|
|PD pointer |This gives the location for this entities data in the Parameter Data section. This location is simply the line number inside the PD section that has the first line of this entity data.|
|Structure |Zero or pointer to definition entity. Not applicable for most entities|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 No pattern specified (default) * 1 Solid * 2 Dashed * 3 Phantom * 4 Centerline * 5 Dotted|
|Level| Specifies levels to be associated with this entity. Allows entity to appear on more than one level|
|View| Specifies viewing options. These are: 0 Indicates equal visibility and characteristics in all views. Default Pointer to the View entity (Type 410) that it can be viewed from Reference a View Visible Associativity entity (Type 402, Form 3)
|Transformation Matrix pointer| References a transformation matrix entity (Type 124) or is zero by default (no transformation)|
|Label Display Associativity| References a Label Display Associativity (Type 402, Form 5) which defines how the entity label appears.|
|Status Number| Contains four sections of two numbers. 1-2: Blank status. Either 00 for normal or 01 for blanked. 3-4: Subordinate entity switch: is 00 for independent, 01 for physically dependent, 02 for logically dependent, and 03 for both. 5-6: Entity Use flag: is either 00 for Geometry, 01 for annotation, 02 for definition, 03 for Other, 04 for Logical, 05 for 2D parametric, and 06 for Construction geometry. Finally, 7-8 is the hierarchy, where 00 indicates global top down (use this entity’s characteristics), 01 is global defer(do not use this entity’s characteristics), and 02 is use hierarchy property(use Hierarchy Entity (Type 406, Form 10)to determine characteristics of hierarchical grouping).|
|Sequence Number| Specified by D#, where # is the line number for this section (not from the top of the file). This is also used to point to this Data Entry entity.|
|Entity Type| it is specified twice per entity listing|
|Line Weight Number| Specifies thickness when displaying entity. Smallest is 1, 0 is default|
|Color Number| Specifies the entity color. Allowed integer values are: 0 No color (default) 1 Black 2 Red 3 Green 4 Blue 5 Yellow 6 Magenta 7 Cyan 8 White|
|Parameter Line Count Number| Specifies the number of lines this entity takes up in the Parameter Data Section|
|Form Number| Indicates the form, or the representation of this entity. Changes how the parameter data is interpreted. Default is 0|
|Reserved Field| Not used|
|Reserved Field| Not used|
|Entity Label| Application specified identifier- right justified|
|Subscript Number| Numeric qualifier for the entity label. Both together form a unique identifier for the entity|
|Sequence Number See above. |This will be D#+1, as each entity is specified on two lines.|

#### Parameter Data Section
The Data Entries section is followed by the Parameter Data section. It lists the data for each respective entry and lists parameters for the entity based on the delimiters specified in the Global section (usually commas to separate parameters and a semi-colon to end the listing).


## References
 * [IGES by WikiPedia](https://en.wikipedia.org/wiki/IGES)
