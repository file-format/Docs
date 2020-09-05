{
  "date" : "2020-03-16",
  "keywords" : [ "DXF File", "File Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DXF file format and APIs that can create and open DXF files.",
  "title" : "DXF File Format",
  "linktitle" : "DXF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is a DXF file? #

DXF, Drawing Interchange Format, or Drawing Exchange Format, is a tagged data representation of AutoCAD drawing file. Each element in the file has a prefix integer number called a group code. This group code actually represents the element that follows and indicates the meaning of a data element for a given object type. DXF makes it possible to represent almost all user-specified information in a drawing file.

DXF file format was developed by Autodesk as CAD data file format for data interoperability between AutoCAD and other applications. Thus, data can be imported from other formats to DXF to AutoCAD as per the DXF file format interoperability specifications.

## Brief History ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. Initial versions of AutoCAD only support ASCII file format of DXF. With the release 10 of AutoCAD (and above) in 1988, support for both ASCII as well as binary DXF file format was introduced in AutoCAD. In the earlier stages, Autodesk didn't share any file format specifications and due to this, correct imports of DXF files was not easy. However, Autodesk now publishes the DXF specifications and available to general public.

## File Format Specifications ##

DXF file format uses the group code and value pairs to arrange the contents into sections. Each section is composed of records where each record consists of a group code and data item. Each group code and value are on their own line in the DXF file. Each section starts with a group code 0 followed by the string, SECTION. This is followed by a group code 2 and a string indicating the name of the section (for example, SECTION1). Each section is composed of group codes and values that define its elements. A section ends with a 0 followed by the string ENDSEC.

DXF file format considers objects different from entities. Objects have no graphical representation here but entities have it. Thus, entries in DXF are referred to have as graphical objects while objects objects are referred to as non-graphical objects. The BLOCK and ENTITIES sections of DXF file contain Entities and the use of group codes in these two sections is identical. End of an entity is indicated by the next 0 group, which begins the next entity or indicates the end of the section.

### File Structure ###

Sections in a DXF file are arranged in the following order:

|Section|Basic description
---|---|
|Header|This section contains general information about the drawing. It’s like the Settings functionality in your phone, which contains the different variables associated with the drawing and its associated values. For example, the Header section will define which AutoCAD version the DXF file uses (the $ACADVER variable) or the unit used to measure angles in the file (the $AUNITS variable)
|Classes|The CLASSES section holds the information for application-defined classes whose instances appear in the BLOCKS, ENTITIES, and OBJECTS sections of the database.
|Tables|This section contains definitions for several different tables, each of which contains a number of different symbol entries. For example the [line type](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2016/ENU/AutoCAD-Core/files/GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF-htm.html) table (LTYPE) defines the pattern of dashes, dots, text and symbols in the DXF file and how they’re scaled. Here is a complete list of tables found in this section: <ul><li>Application ID (APPID) table</li><li>Block Record (BLOCK_RECORD) table</li><li>Dimension Style (DIMSTYPE) table</li><li>Layer (LAYER) table</li><li>Linetype (LTYPE) table</li><li>Text style (STYLE) table</li><li>User Coordinate System (UCS) table</li><li>View (VIEW) table</li><li>Viewport configuration (VPORT) table</li></ul>
|Blocks|This section contains the graphical objects and drawing entities that make up each block reference in the drawing.
|Entities|This section contains the actual object data and graphical entities of the drawing. This can include raw data – for example, a circle entity is defined by its thickness, the center point, its radius and extrusion direction.
|Objects|Here, you’ll find the the non-graphical parts of the drawing. For example, AutoCAD dictionaries are stored here.

## References ##

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF by Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)
