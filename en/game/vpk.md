{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about Unreal Static Meshes VPK file format and APIs that can create and open VPK files.",
  "title" : "VPK File - Unreal Static Meshes File",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
    }
  },
  "lastmod" : "2023-01-16"
}

## What is a VPK file?

A .vpk file is a file format used by the **Source Engine**, a game engine developed by Valve Corporation. VPK files are used to package game content, such as models, textures, and sounds, and are commonly used in games like Team Fortress 2, Left 4 Dead, and Counter-Strike: Global Offensive. The files can be opened and extracted using a variety of tools, such as GCFScape and VPK Tool.

## VPK File Format - More Information

VPK files are stored to disc as binary files. A single vpk file can be a part of a VPK package or can act as an independent raw VPK file. Information that can be stored inside a VPK file includes maps, materials, game content, and choreography scenes.

### How to Create VPK File?

There are several ways to create a .vpk file, depending on the available tools.

1. `Using the VPK tool:` This is a command-line tool that can be used to create and extract VPK files. A VPK file can be created using the following command:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
This will create a VPK file from the specified directory, and save it as the output file specified.

1. `Using the Hammer Editor:` The Hammer Editor is a tool included with the Source SDK that can be used to create and edit levels for games that use the Source engine. It also includes the ability to create VPK files, by right-clicking on a folder in the "File System" tab and select "Create VPK"

1. `Using Valve's VPK creator:` This is a tool developed by Valve that is used to package and distribute game content. This tool can be used to create VPK files and also it is the official tool for creating VPK files.

## References

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK Developer's Resources](https://developer.valvesoftware.com/wiki/GCF)
