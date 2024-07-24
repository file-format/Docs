{
  "date" : "2024-07-22",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BSP File - Quake or Source Engine Game Map File - What is .bsp file and how to open it?",
  "description" : "Learn about BSP Quake or Source Engine Game Map File and how to open it.",
  "linktitle" : "BSP",
  "menu" : {
    "docs" : {
      "identifier" : "game-bsp",
      "parent" : "game"
    }
  },
  "lastmod" : "2024-07-22"
}

## What is a BSP file?

A **BSP file** is a crucial component in video game development, used to store map data for various game engines, including the Quake and Source engines. In the Quake engine, `.bsp` files serve as containers for map geometry, textures, and entity data. These files are created when maps designed in Quake’s level editor are compiled, allowing the game to render and utilize these maps during gameplay. This format encapsulates the layout and visual elements of the game environment, ensuring that the game engine can efficiently load and display the map.

Similarly, in the Source engine, `.bsp` files are used to store map data for games like Half-Life 2 and Counter-Strike: Source. Maps for these games are designed using tools such as the Hammer Editor, and the resulting `.bsp` files contain essential information about the map's geometry, textures, and entities. These files are essential for the Source engine to render the levels accurately during gameplay. The `.bsp` file format is binary, which means it is not easily readable or editable by hand but is optimized for use by the game engine to ensure smooth performance and accurate representation of the game environment.

## BSP File Format - More Information

BSP stands for Binary Space Partitioning, a technique used by game engines to efficiently manage and render 3D environments. The core idea behind BSP is to break down complex polygons into simpler, convex sets. This partitioning helps the engine handle and render intricate 3D maps more efficiently by simplifying the calculations needed to display the map. By dividing the space into manageable sections, the engine can quickly determine which parts of the map are visible and need to be rendered, thus improving performance and reducing rendering time.

## Structure of a BSP File

A `.bsp` file is organized into several sections called "lumps," which are chunks of data described in the file's header. Each lump serves a specific purpose:

-   **Entities**: Defines objects and their properties within the map, such as lights, spawn points, or items.
-   **Nodes**: Structures used to organize and partition the map's geometry, aiding in efficient rendering and collision detection.
-   **Vertices**: Points that define the corners of the polygons making up the map’s geometry.
-   **Planes**: Flat surfaces that form the boundaries of the map’s geometry, helping to partition the space.
-   **Leaves**: Subdivisions of the map's space, which help in managing visibility and rendering.
-   **Visibility**: Information that helps the engine determine which parts of the map are visible from different locations.
-   **Faces**: Surfaces of the polygons that make up the map’s geometry.
-   **Textures**: Visual elements applied to the surfaces to give them their appearance.


## Creating and Compiling BSP Files

BSP files are binary files, which means they are stored in a format that is optimized for performance rather than human readability. Developers create and compile these files from `.MAP` files, which contain the raw map data. Tools such as Q3Map2 and Irrlicht are commonly used for this purpose. Additionally, id Software provides tools like GtkRadiant and DarkRadiant, which are specifically designed for creating and editing BSP files.

## Use in Quake Game Engines

Several Quake game engines utilize BSP files to handle map data:

-   **id Tech 1 (Doom Engine)**: The original engine by id Software, which used a form of BSP for its levels.
-   **Quake Engine**: The engine used for the original Quake game, also based on BSP technology.
-   **id Tech 2 (Quake II Engine)**: Improved upon the original Quake engine with enhanced BSP features.
-   **id Tech 3 (Quake III Arena)**: Introduced further advancements in BSP handling and rendering.
-   **id Tech 4 (Doom 3)**: Continued the use of BSP technology with additional improvements for more complex and detailed environments.

## Differences Between Quake and Source Engine BSP Files

Valve’s Source engine, which powers games like _Half-Life 2_, _Left 4 Dead_, and _Team Fortress 2_, evolved from the Quake engine. As a result, it continues to use `.bsp` files for storing map data, similar to the Quake engine. However, the Source engine employs its own version of the `.bsp` format, which differs from the original Quake format. Consequently, programs designed to decompile Quake BSP files (i.e., tools that convert binary data into a human-readable format) may not be effective with Source BSP files due to differences in file structures and data formats between the two engines.

The Source engine’s `.bsp` file format includes modifications and enhancements tailored to its rendering and game mechanics, making it distinct from the Quake BSP format. In Source engine games, BSP files are stored within the game’s `.GCF` (Game Cache File) archives. Notably, Source engine BSP files do not include descriptive text for the map, which was sometimes present in Quake’s BSP files. Additionally, Source engine BSP files do not contain the AI navigation files used by non-player characters (NPCs) to navigate the map; instead, these AI navigation files are typically stored separately and guide NPCs through the game environment.

## How to open a BSP file

To open a `.bsp` file, follow these steps:

1.  **Game Engine**: Load the file directly within the game engine it was designed for. For example, use the Source engine for maps from Source games or the Quake engine for Quake maps.
    
2.  **Editor Tools**: Use level editors like Hammer Editor (for Source engine maps) or GtkRadiant (for Quake maps) to view and edit `.bsp` files.
    
3.  **Decompilers**: Use decompiling tools (such as BSPTwoMap or Quake BSP decompilers) to convert `.bsp` files into a more editable format like `.map`. Note that compatibility may vary between different engines.
    
4.  **Viewers**: Use map viewers or visualizers specific to the game engine, which can display the map without editing capabilities.

## References
* [Binary space partitioning](https://en.wikipedia.org/wiki/Binary_space_partitioning)
