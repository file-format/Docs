{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about .pak file and APIs that can create and open PAK files.",
  "title" : "PAK File Format- Video Game Package File",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak",
      "parent" : "game"
    }
  },
  "lastmod" : "2021-10-27"
}

## What is a PAK file?

A PAK file is a package file created by different video games to archive game data. Essentially, it's a game file format. This can include multiple game elements such as graphics, textures, sounds, objects, along with other game data. The archive is mostly saved as .zip file and can be extracted with popular decompression software such as WinZip and WinRAR. Examples of video games using PAK files include Quake, Hexen, Crysis, and Half-Life.

## PAK File Format - More Information

In most cases, PAK files are saved in [ZIP file format](/compression/zip/). But different applications may use different file format for storing these files.


## How to Open PAK files?

You can open PAK files with applications such as [PakExplorer](https://www.quaketerminus.com/tools.shtml) and [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**-------------------------------------------------------------------------------------------------------------------------**

## PAK File Format - Simutrans Object File

A file with .pak extenion is a [Simutrans](https://www.simutrans.com/en/) transportation simulation game file format. It contains objects used in the simulation such as user made graphics and data contents. It can have several different objects such as game vehicles, buildings, terrain, etc. PAK files are generated using MakeObject, a utility that compiles .dat files and .png pictures for creating these simulation objects. Simutrans lets the players to run a successful transport system by constructing and managing transportation systems for passengers, mail and goods by land

## How to Create PAK Files?

Simutrans has listed sample examples for creating PAK files on Windows and Linux OS.

### Windows OS

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## References

 * https://simutrans-germany.com/wiki/wiki/en_doPak
 * https://en.wikipedia.org/wiki/Simutrans
