{
  "date" : "2020-03-16",
  "keywords" : [ "STL File", "Format", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to learn what is a STL file and APIs that can create and open them.",
  "title" : "STL File Format - Learn from File Format Experts!",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is STL file? #

STL, abbreviation for stereolithrography, is an interchangeable file format that represents 3-dimensional surface geometry. The file format finds its usage in several fields such as rapid prototyping, 3D printing and computer-aided manufacturing. It represents a surface as a series of small triangles, known as facets, where each facet is described by a perpendicular direction and three points representing the vertices of the triangle. Resultant data is used by applications to determine the cross section of the 3D shape to be built by the fabber. There is no information available in the STL file format for representation of colour, texture or other common [CAD](/cad/) model attributes.

## Brief History ##

The development of STL file format dates back to 1987. It was developed by 3D Systems for its usage in commercial 3D printers. A revised version of STL file format, known as STL 2.0,  was proposed in 2009 with updates to the file format.

## File Format Specifications ##

An STL file represents a surface geometry using facets. The facets define the surface of a 3D object and is uniquely identified by a unit normal, which is a line perpendicular to the triangle with length of 1.0, and by three vertices. There are a total of 12 numbers stored for each facet as the Normal and each vertex are specified by three coordinates each. The StL file does not contain any scale information; the coordinates are in arbitrary units.

The specifications of STL file format can be examined from following two aspects.

### Facets Orientation ###

Orientation of a facet is determined by the direction of the unit normal and the order in which the vertices are listed. The orientation of the facets is specified in two ways as follow:

* The direction of the normal is outward
* The vertices are listed in counter-colock-wise order from outside, obeying the right-hand rule. 

### Vertex to Vertex Rule ###

According to this rule, each triangle shares two vertices with each of its adjacent triangles. Thus, a vertex of one triangle cannot lie on the side of another triangle.

## File Formats ##

STL is available in ASCII as well as Binary representations for compact file format.

### STL ASCII Format ###

The ASCII version of STL file format is written in plain ASCII. However, due to its large size, the file format is not selected as preferable format for usage. The syntax of an ASCII STL file is as follow:

{{{solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
}}}

**endsolid** name

The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. A **facet normal** coordinate may have a leading minus sign; a **vertex** coordinate may not.

### STL Binary Format ###

The binary format uses the IEEE integer and floating point numerical representation. The file format is represented as follow:


|Header|80 characters
|Number of Triangles|4-byte little endian unsigned integer
|Data for each triangle|12 32-bit floating point numbers

A more elaborated view of the file format is as shown below.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## See Also ##

* [DWG](/cad/dwg/)
* [DXF](/cad/dxf/)

## References ##

* [The StL Format](http://www.fabbers.com/tech/STL_Format)
* [STL File Format for 3D Printing](https://all3dp.com/what-is-stl-file-format-extension-3d-printing/)
* [STL - by Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))