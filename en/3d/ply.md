{
  "date" : "2019-12-12",
  "keywords" : [ "PLY", "file", "extension", "format", "3D file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is a PLY file and APIs that can create and open them.",
  "title" : "What is a PLY file?",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a PLY file?

PLY, Polygon File Format, represents 3D file format that stores graphical objects described as a collection of polygons. The purpose of this file format was to establish a simple and easy file type that is general enough to be useful for a wide range of models. PLY file format comes as ASCII as well as Binary format for compact storage and for rapid saving and loading. The file format is used by different applications that provide support for 3D files reading.

Objects in a PLY format are described by a collection of vertices, faces and other elements, along with properties such as colour and normal direction that can be attached to these elements. Other properties that can also be stored with the object include:

* Surface normals
* texture coordinates
* transparency
* range data confidence
* properties for the front and back of a polygon

An object represented by PLY format can be the result of various sources such as hand-digitized objects, polygon objects from modelling applications, range data, triangles from marching cubes, terain data and radiosity models.

## Brief History

The PLY format was developed in in 1990's by Greg Turk and others in the Stanford graphics lab and that is why it is also known as Stanford Triangle Format. The file format has version 1.0 since then and no further modifications were done.

## PLY File Format

A simple PLY object consists of collection of elements for representation of the object. It consists of a list of (x,y,z) triples of a vertices and a list of faces that are actually indices into the list of vertices. Vertices and faces are two examples of elements and majority of the PLY file consists of these two elements. New properties can also be created and attached to the elements of an object, but these should be added in such a way that old programs do not break when these new properties are encountered. Such properties can be discarded by reading applications as well. Moreover, new elements can be created and properties can be defined with this element  as well.

### File Structure

The file structure of a PLY file format is as follow:

|Field
---|
|File Header
|Vertex List
|Face List
|List of other elements

#### Example Structure

We will use the following example below in our subsequent discussion for various parts of a PLY file format.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### File Header

PLY file format header consists of ASCII text for both the ASCII as well as the binary format.  The start and end of header section is identified by ply and end-header keywords. The start of header has the magic word ply which is used for recognition of PLY file format by readers. The next line shows the version number for this file. Comments in a PLY file format start with comment keyword at the start of each comment line.

#### Element Keyword

The element keyword then tells what's inside the file. It is followed by properties for that specific element type where each property has its property type and order specified as shown below:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

In this particular example, the specific vertex element has 3 properties of type float with their order specified.

#### Types of Data Types

There are two type of data types that a property may have.

`Scalar`: The scalar data types are as shown below:


|#Name|#Type|#Number of Bytes
|char|character|1
|uchar|unsigned character|1
|short|short integer|2
|ushort|unsigned short integer|2
|int|Integer|4
|uint|unsigned Integer|4
|float|single-precision float|4
|double|double precision float|8

`List`: There is a special form of property definitions that uses the list data type. An example of this is from the cube file above:

`property list uchar int vertex_index`

This means that the property "vertex_index" contains first an unsigned char telling how many indices the property contains, followed by a list containing that many integers. Each integer in this variable-length list is an index to a vertex.

## References ##

* [PLY File Format](http://paulbourke.net/dataformats/ply/)
* [PLY - By Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))
