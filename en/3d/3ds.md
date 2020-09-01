{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about 3DS file format and APIs that can open and create 3DS files.",
  "title" : "3DS",
  "linktitle" : "3DS",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

A file with 3DS extension represents 3D Sudio (DOS) mesh file format used by Autodesk 3D Studio. Autodesk 3D Studio has been in 3D file format market since 1990s and has now evolved to 3D Studio MAX for working with 3D modeling, animation and rendering. A 3DS file contains data for 3D representation of scenes and images and is one of the popular file formats for 3D data import and export. It considers information like camera locations, Mesh data, lighting information, viewport configurations, smoothing group data, bitmap references and attributes to create vertices and polygons for rendering a scene.

# What is 3DS file? #

At its base, 3DS is a binary file format and follows a predefined structure for storing and retrieving of data. The binary file format enables the 3DS file format faster smaller as compared to text-based file formats. Data inside a 3DS file is stored in the form of chunks.

### Chunk ###

Each chunk in a 3DS file is a block of data that contains an ID, length of the block for location of next block and the data itself. The chunk ID lets 3DS file format readers to skip the blocks that they don't recognize. It also helps in extensibility of the format. Each chunk stores information related to shapes, lighting and viewing information that together render the scene. Chunks are arranged in a hierarchical structure in a 3DS file and resemble XML Document Object tree in representation.

**Chunk ID:** The first two bytes of a chunk represent a chunk identifier that lets the file reader decide whether to consider it during reading or skip it.

**Length of the chunk:** The Chunk ID is followed by a 4-bytes integer (in little-endian) that stands for the length of the chunk. This length also includes the length of the data, the length of its sub-blocks and the 6-bytes header.

**Payload:** The length of chunk is followed by actual bytes of data for the chunk, followed by its sub-chunks in the same hierarchical structure that can be extended to several levels deep.

#### Structure ####

The hierarchical structure of a simple chunk is as shown below:

**A Chunk**

|start|end|size|name
--- | --- | --- | ---
|0|1|2|Chunk ID
|2|5|4|Next Chunk

Chunks have a hierarchy imposed on them that is identified by its ID. A 3ds file has the Primary chunk ID 4D4Dh. This is always the first chunk of the file. With in the primary chunk are the main chunks.

**Main Chunks**

|id|Description
--- | ---
|3D3D|Start of object mesh data.
|B000|Start of keyframer data.

The Next Chunk pointer after the ID block points to the next Main chunk.
Directly after a Main chunk is another chunk. This could be any other type of chunk allowable within its main chunks scope.
For the Mesh description (3D3D) they could be any multiples of.

**Subchunks of 3D3D - Mesh Block**


|id|Description
--- | ---
|1100|unknown
|1200|Background Colour.
|1201|unknown
|1300|unknown
|1400|unknown
|1420|unknown
|1450|unknown
|1500|unknown
|2100|Ambient Colour Block
|2200|fog?
|2201|fog?
|2210|fog?
|2300|unknown
|3000|unknown
|4000|Object Block
|7001|unknown
|AFFF|unknown

**Subchunks of 4000 - Object Description Block**
The first item of Subchunk 4000 is an ASCIIZ string of the objects name.
Remember an object can be a mesh, a light or a camera.

|id|Description
--- | ---
|4010|unknown
|4012|shadow?
|4100|Triangular Polygon Object
|4600|Light
|4700|Camera

## References ##

* [Geometry File Formats - Autodesk](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2015/ENU/3DSMax/files/GUID-566E59EE-8221-4AC6-824B-5062C5AE0B32-htm.html)
* [3DS - By Wikipedia](https://en.wikipedia.org/wiki/.3ds)
