{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DDS File Format- DirectDraw Surface Image File",
  "description":"Learn about DDS file format and APIs that can create and open DDS files.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2022-04-02"
}

## What is a DDS file?

A DDS file is a raster image file that utilizes the DirectDraw Surface (DDS) container format. It stores uncompressed and compressed (DXTn) textures and implements different types for storing different types of data. It also supports several different type of data such as single layer textures, textures with mipmaps, cube maps, volume maps and texture arrays. This enables the DDS files to store video game texture unit models in addition to digital photos and Windows desktop backgrounds. DDS file format was developed by Microsoft to be used with DirectX SDK.

## DDS File Format

DDS files are saved as binary files and can be used with DirectX SDK. It utilizes the power of DirectX to develop real-time rendering applications such as 3D games.

### DDS File Layout

The [DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) has been documented by Microsoft in detail. A binary DDS file contains the following information.

 * A DWORD (magic number) containing the four character code value 'DDS ' (0x20534444).
 * A description of the data in the file.

The DDS_HEADER describes the data and the DDS_PIXELFORMAT describes the pixel format. These both replace the deprecated DDSURFACEDESC2, DDSCAPS2 and DDPIXELFORMAT DirectDraw 7 structures.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

The [programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) further elaborates the technical details of this file format.

## References

* [DDS - By Wikipedia](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX File Format Technical Reference Manual](http://qzx.com/pc-gpe/pcx.txt)
