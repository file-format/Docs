{
  "date" : "2020-01-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "X - DirectX 2.0 File Format",
  "description":"Learn about DirectX X file format and APIs that can open and create DirectX X files.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2020-01-11"
}

## What is a X file?

A file with .x extension refers to [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D Graphics legacy file format that was introduced with Microsoft DirectX 2.0. It was used for 3D graphics rendering in games and specifies the structures for meshes, textures, animations, and user-defined objects. It has been deprecated since 2014 as the Autodesk FBX file format serves better as a more modern format. X is template-driven and is free of any usage knowledge. You can open DirectX X files using Microsoft DirectX and common text editors.

## X File Format

The [X file reference](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) contains reference information for the API elements that are used to work with DirectX .x files. The format provides low-level data primitives that are used by other applications to define higher-level primitives through data templates. DirectX 6.0 introduced interfaces and methods that enable reading from and writing to .x files. DirectX 3.0 introduced a binary version of this file format.

The [X file format reference](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) defined by DirectX 9 contains reference information for .x files in Binary as well as Text Encodings.

### Binary Encoding

The [binary format](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) defines the DirectX X format as a tokenized representation of the text format. These tokens can be standalone to give grammatical structure or can be record-bearing tokens supplying the necessary data.

#### Header

The binary header can be read and write using the following definitions.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### Text Encoding

DirectX .x files don't depend on the way how the file is used and is not specific to any application. This template-driven approach allows the .x file format to be used by any client application.


#### Header

The variable-length header is compulsory and must be at the beginning of the data stream. The header contains the following data.

|Type	|Sub Type	|Size	|Contents	|Content Meaning|
---|---|---|---|---|
|Magic Number (required)| |		4 bytes	|xof |
|Version Number (required)	|Major Number	|2 bytes	|03	|Major version 3|
| |Minor Number	|2 bytes	|02	|Minor version 2|
|Format Type (required)|		|4 bytes	|"txt "	|Text File|
| | | |"bin "|	Binary File|
| | | |"tzip"|	MSZip Compressed Text File|
| | | |"bzip"|	MSZip Compressed Binary File|
|Float size (required)| |4 bytes|	0064|	64-bit floats|
| | | |0032	|32-bit floats|


## References

 * [X Files Legacy](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
 * [DirectX 9 File Format Reference](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)
