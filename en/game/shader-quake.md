{
   "date":"2023-10-11",
   "keywords":[
      "shader",
      "shader file",
      "shader quake 3 engine shader file",
      "how to open a shader file",
      "file",
      "shader file extension",
      "extension",
      "file"
   ],
   "author":{
      "display_name":"Shakeel Faiz"
   },
   "draft":"false",
   "toc":true,
   "title":"SHADER File Format - Quake 3 Engine Shader File",
   "description":"Learn about SHADER Quake 3 Engine Shader file format and APIs that can create and open SHADER files.",
   "linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
         "parent":"game"
      }
   },
   "lastmod":"2023-10-11"
}

## What is a SHADER file?

The SHADER file format is used in **Quake 3 engine** to define shaders for textures and materials in game. Shaders are used to specify how a surface should be rendered, including its appearance, reflectivity, transparency and other visual properties. 

## Quake 3 Engine SHADER File

Here is a basic overview of structure and syntax of a Quake 3 engine shader file:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

In a Quake 3 engine shader file, you can define multiple shaders, each with its own set of properties and stages. These shaders are used to define appearance of different textures and materials in game world. The engine uses this information to render surfaces with specified visual effects and behaviors.

Shader files in Quake 3 engine are simple text files that contain instructions for how textures and materials should appear in game. These files can be opened and edited with a regular text editor and are typically found in **"/scripts"** directory within a game's .PK3 package.

## Quake 3 Engine

The Quake 3 engine is a highly influential and versatile game engine developed by id Software. It was first introduced with release of game "Quake III Arena" in 1999 and has since been used in various other games. The engine is known for its advanced graphics, multiplayer capabilities and modifiability.

Here are some key features and aspects of Quake 3 engine:

1.  **Graphics Engine:** The Quake 3 engine was renowned for its cutting-edge graphics technology at time. It introduced advanced features such as curved surfaces, shaders and dynamic lighting, which were groundbreaking in late 1990s.
    
2.  **Multiplayer Focus:** Quake 3 Arena was primarily designed as a multiplayer first-person shooter. The engine's networking code and support for online multiplayer gaming were exceptional, making it a popular choice for competitive online play.
    
3.  **Modifiability:** The Quake 3 engine is known for its modifiability. id Software released engine source code under open-source GNU General Public License (GPL). This encouraged creation of numerous mods and custom maps, leading to a vibrant modding community.
    
4.  **Scripted Gameplay:** The engine used a script-based system to define game rules and behavior, making it relatively easy for modders and mappers to create custom game modes and unique experiences.
    
5.  **Support for Custom Content:** Quake 3's engine supported custom content, including textures, models and sound files, which allowed for a high degree of customization in user-created maps and mods.
    
6.  **Level Design:** The engine used a brush-based level design system, where maps were constructed by carving out spaces from solid brushes. This approach was well-documented and user-friendly for level designers.


Over years, Quake 3 engine has been used as basis for many other games and mods, including "Return to Castle Wolfenstein," "Star Wars Jedi Knight II: Jedi Outcast," and "Urban Terror," among others. It left a lasting legacy in world of game development and helped shape first-person shooter genre. While newer and more advanced engines have since emerged, Quake 3 engine continues to be respected for its contribution to gaming industry.

## How to open SHADER file?

Programs that open or reference SHADER files include

- **id Software Quake 3** (Paid) for (Windows, Mac, Linux)
- Microsoft Notepad
- Notepad++
- Any text editor

## Other SHADER files

Here are other file types that use the **.shader** file extension.

**Game Files**
- [SHADER - Godot Engine Shader File](/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/game/shader-quake/)
- [SHADER - Unity Shader Asset](/game/shader-unity/)

## References
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)
