{
  "date": "2023-09-27",
  "keywords": [
    "cfg",
    "cfg file",
    "cfg cal3d model configuration file",
    "what is a cfg file",
    "how to open cfg file",
    "file",
    "cfg file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "CFG File Format - Cal3D Model Configuration File",
  "description": "Learn about CFG Cal3D Model Configuration File format and APIs that can create and open CFG files.",
  "linktitle": "CFG Cal3D",
  "menu": {
    "docs": {
      "identifier": "misc-cfg-cal3d",
      "parent": "misc"
    }
  },
  "lastmod": "2023-09-27"
}

## What is a CFG file?

A Cal3D Model Configuration File is a text-based file used by the Cal3D library, which is an open-source toolkit for character animation. This file serves as a blueprint for assembling a three-dimensional (3D) model. It includes references to various components of the model, such as the skeleton structure, materials, animations, and more. Essentially, it acts as a central document that helps organize and define how all the parts of the 3D model fit together within the Cal3D framework.

Cal3D is a skeletal animation library often used in computer graphics and game development. To work with Cal3D models, you typically need to create a configuration file that describes the model's structure, materials, animations, and other attributes. Below is an example of what a Cal3D model configuration file might look like. 

```
<MODEL>
  <HEADER MAGIC="C3D" VERSION="1050" />

  <!-- Skeleton -->
  <SKELETON>
    <BONE ID="0" NAME="Root">
      <TRANSLATION>0.0 0.0 0.0</TRANSLATION>
      <ROTATION>0.0 0.0 0.0</ROTATION>
      <SCALE>1.0 1.0 1.0</SCALE>
    </BONE>
    <!-- Add more bone definitions here -->
  </SKELETON>

  <!-- Mesh -->
  <MESH>
    <SUBMESH>
      <MATERIAL>MATERIAL_NAME</MATERIAL>
      <VERTEX>
        <!-- Vertex data for the first vertex -->
        <POSITION>0.0 0.0 0.0</POSITION>
        <NORMAL>0.0 0.0 1.0</NORMAL>
        <TEXCOORD>0.0 0.0</TEXCOORD>
        <!-- Add more vertices here -->
      </VERTEX>
      <FACE>
        <!-- Face data for the first face -->
        <VERTEXID>0 1 2</VERTEXID>
        <!-- Add more faces here -->
      </FACE>
      <!-- Add more submeshes here -->
    </SUBMESH>
  </MESH>

  <!-- Animation -->
  <ANIMATION>
    <SKELETON>
      <!-- Define animations and keyframes here -->
    </SKELETON>
  </ANIMATION>

</MODEL>
```

## Cal3D

Cal3D is an open-source character animation library used in 3D computer graphics and game development. It provides tools and functionalities for creating and animating 3D characters or models. Cal3D is often used to bring lifelike character animations to interactive applications and games.

Key features and components of Cal3D include:

1. **Mesh:** The mesh component defines the 3D geometry of a character or object, including vertices, normals, and texture coordinates. It forms the visual representation of the model.

2. **Skeleton:** Cal3D allows the creation of a skeleton hierarchy for character models. This skeleton defines the bone structure, and each bone can be associated with a portion of the mesh. Skeletons are crucial for animating characters by manipulating bones.

3. **Materials:** Materials define how the surface of the model should appear when rendered. This includes information about textures, shaders, and other rendering properties.

4. **Animations:** Cal3D supports various animation techniques that can be applied to the skeleton. These animations define how bones move over time to create realistic character animations, such as walking, running, or performing other actions.

5. **Configuration Files:** To use Cal3D effectively, models are often accompanied by configuration files in plain text format. These files describe the model's structure, including bone hierarchy, mesh data, materials, and animation information. Configuration files serve as references for Cal3D to correctly load and interact with the model.

## File Formats Used by Cal3D

Cal3D uses several file formats for different purposes, such as storing model data, animations, and configuration information. Here are some of the common file formats used by Cal3D:

1. **Cal3D Binary Model Files (.cmf):** These files store the binary representation of 3D models, including mesh geometry, bone hierarchy, and materials. CMF files are used to efficiently load and render Cal3D models in applications.

1. **Cal3D XML Model Files (.cmx):** XML-based files that store the textual representation of Cal3D models. They contain information about the model's structure, animations, materials, and more. [CMX](/image/cmx/) files are often used for easier human-readable editing and debugging.

1. **Cal3D Animation Files (.caf):** These files store animation data, including keyframes and bone transformations. CAF files are essential for defining how characters or objects should move and animate within a Cal3D model.

1. **Cal3D Morph Target Files (.crf):** Used to define morph targets, which allow for facial expressions and other non-skeletal deformations of the mesh.

1. **Cal3D Material Files (.cfm):** These files store material information for Cal3D models. They specify how the model's surface should be shaded, including texture references, shaders, and rendering properties.

1. **Cal3D Skeleton Files (.csf):** Skeleton files store information about the bone hierarchy and structure of a Cal3D model. They define how bones are connected and parented within the skeleton.

1. **Cal3D Configuration Files (.cfg):** These plain text files serve as configuration files for Cal3D models. They contain references to various components of the model, including bone hierarchy, mesh data, materials, and animations. Configuration files help Cal3D correctly load and use the model.

1. **Image Formats:** While not specific to Cal3D, image file formats like [JPEG](/image/jpeg/), [PNG](/image/png/), [BMP](/image/bmp/), or [TGA](/image/tga/) are commonly used for textures applied to Cal3D models.

## How to open CFG file?

Programs that open CFG files include

- Cal3dViewer
- Microsoft Notepad
- Apple TextEdit
- Any text editor

## Other CFG files

Here are other file types that use the **.cfg** file extension.

**Settings**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Game**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## References
* [CAL3D](https://github.com/mp3butcher/Cal3D)