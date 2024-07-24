{
  "date" : "2024-07-22",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MDX File - Warcraft 3 Model File - What is .mdx file and how to open it?",
  "description" : "Learn about MDX Warcraft 3 Model File and how to open it.",
  "linktitle" : "MDX",
  "menu" : {
    "docs" : {
      "identifier" : "3d-mdx",
      "parent" : "3d"
    }
  },
  "lastmod" : "2024-07-22"
}

## What is an MDX file?

An MDX file is a model file used in Blizzard Entertainment's game "Warcraft 3." These files contain 3D models, including meshes, textures, animations, and other data necessary for rendering characters, buildings, and other objects within the game. Here's a detailed breakdown of the MDX file format in the context of Warcraft 3:

## Structure of an MDX File

1.  **Header**

    The header typically contains metadata about the model, such as the version of the file format and other general information.
1.  **Vertices**
    
    This section contains the 3D coordinates of the model's vertices. Vertices are the points in 3D space that make up the model's mesh.
1.  **Normals**
    
    Normals are vectors that are perpendicular to the surface of the model at each vertex. They are used for lighting calculations.
1.  **Texture Coordinates**
    
    These coordinates map the 2D textures onto the 3D model.
1.  **Faces**
    
    Faces (or polygons) define how vertices are connected to form the 3D shape. Typically, models are made up of triangles or quads.
1.  **Bones**
    
    Bones are used for skeletal animation, allowing the model to move in a lifelike manner.
1.  **Animations**
    
    This section includes the data for animating the model, such as keyframes and bone transformations.
1.  **Materials**
    
    Materials define the appearance of the model's surface, including textures, colors, and shading properties.
1.  **Geosets**
    
    Geosets are collections of vertices, normals, and faces that make up parts of the model. Each geoset can have its own material.
1.  **Attachments**
    
    These are points on the model where other objects can be attached, like weapons or effects.
1.  **Events**
    
    Events can trigger specific actions or effects during the model's animation, like sound effects or particle emissions.

## Tools for Editing MDX Files

-   **Warcraft 3 Model Editor**: Tools like the Warcraft 3 Model Editor (also known as War3ModelEditor) allow you to view and edit MDX files.
-   **MDLX Converter**: This tool converts MDX files to and from the MDL format, which is a human-readable text format.

## MDX vs. MDL

-   **MDX**: Binary format, more compact and efficient for the game engine to read.
-   **MDL**: Text format, easier for humans to read and edit.

## Converting MDX to MDL

1.  **Open the MDLX Converter**.
2.  **Load your MDX file** into the converter.
3.  **Convert** the file to MDL format for easier editing.
4.  **Edit** the MDL file using a text editor.
5.  **Convert** the file back to MDX using the converter.

## Example Use Case

If you want to customize a character model in Warcraft 3, you would:

1.  **Extract** the MDX file from the game files.
2.  **Convert** it to MDL for easier editing.
3.  **Make the necessary changes** to the model, such as modifying vertices, textures, or animations.
4.  **Convert** the edited MDL file back to MDX.
5.  **Import** the modified MDX file back into the game.

## How to open an MDX file

Opening an MDX file, especially for a game like Warcraft 3, usually involves using specific tools designed for working with game models. You can open and edit an MDX file with following tools.

-   **Warcraft 3 Model Editor (War3ModelEditor)**
-   **MDLX Converter**
-   **Blender (with MDX Import/Export plugin)**
-   **Notepad++ (or any text editor, if converting to MDL)**

## References
* [MDX - Blizzard Entertainment](https://en.wikipedia.org/wiki/MDX)
