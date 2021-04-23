{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about B3D file format; used in blitz3d games and APIs that can open and create B3D files.",
  "title" : "B3D - Blitz3D Entity Model File",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2021-04-19"
}

## What is a B3D file?
A file with .b3d extension is a model file used by Blitz3D which may contain video game models for characters, buildings, terrain and other objects. The Blitz3D is a programming language used to create **blitz3d games**. Blitz3D is a powerful, flexible and easy-to-use programming language designed for the sole purpose of writing video games. The developers can create action packed 3D games, 2D puzzlers, adventures, RPGS, whatever just by using Blitz3D. The Blitz3D is based on the BASIC programming language; which is also easy to learn and use. These all facts are making Blitz ideal for beginners and more experienced programmers alike. Although it features are considered somewhat antiquated than found in most modern 3D engines, Blitz3D continues to be used by many game programmers worldwide.

## Brief history of Blitz3D
The Blitz3D was basically released for Microsoft Windows operating system in September 2001, to compete with other similar game-development languages. Blitz3D was an upgraded version over the earlier 2D engine BlitzBasic, which extended its command-set with the addition of an API for a DirectX 7-based 3D engine. The Blitz3D users should also compare BlitzMax, which is a later engine by BlitzBasic. The BlitzMax is a complex but more powerful version of Blitz3D, which supports object-oriented programming languages. It is an updated graphics API to better suit Unicode characters, OpenGL, and exporting to OSX and Linux instead of only Windows.

## How to open B3D file? ##

If you are not being able to open the B3D file on your computer; there may be many causes. The most important cause is that B3D supported softwares are not installed on your device. In this case you need to see the following points as a guideline:

- Install the well suited software to run the file.
- If still you are facing difficulty to open the .b3d file; you must check the version of the software and see either that is supporting .b3d files or not. Some files can be supported by the old version and some by the latest one so, must check the details.
- After installing the appropriate verion of software make sure that it is set as the default application to open B3D files.

### Softwares that can open the B3D files ###
The B3D files can be opened in the following softwares:

|Operating System| Software|
---|---|
|Microsoft Windows|Blitz Research Blitz3D, Ultimate Unwrap 3D with Blitz3D plug-in, Irrlicht, Blender|
|MacOS|Irrlicht, Blender|
|Linux|Irrlicht, Blender|

## B3D Example
A b3d file which contain 1 TEXS chunk, 1 BRUS chunk and 1 NODE chunk, will look like this:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
A simple, non-animating and non-textured mesh will look like this:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## References
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)
