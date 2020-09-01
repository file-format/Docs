{
  "date" : "2019-12-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"Learn about GLB file format and APIs that can open and create GLB files.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2020-09-01"
}

# What is a GLB file? #

GLB is the binary file format representation of 3D models saved in the GL Transmission Format ([glTF](/3d/gltf/)). Information about 3D models such as node hierarchy, cameras, materials, animations and meshes in binary format. This binary format stores the glTF asset (JSON, .bin and images) in a binary blob. It also avoids the issue of increase in file size which happens in case of glTF. GLB file format results in compact file sizes, fast loading, complete 3D scene representation, and extensibility for further development. The format uses model/gltf-binary as MIME type.

# GLB File Format #

The content delivery methods used by glTF result in extra processing to decode the base-64 encoded binary data and also increases the file size by 33%. These delivery methods, which contributed to the formation of GLB file format, include:

* glTF JSON points to external binary data (geometry, key frames, skins), and images.
* glTF JSON embeds base64-encoded binary data, and images inline using data URIs.

GLB as a container format was introduced as binary file format for representation of glTF asset in a binary blob to avoid the issues caused by glTF. GLB file format [specifications](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) should be referred for any reader/writer implementation of the same for applications development.

### File Structure ###

GLB file format is based on little endian and its structure is as shown below:

![GLB File Structure](https://github.com/KhronosGroup/glTF/raw/master/specification/2.0/figures/glb2.png "GLB File Structure")

This shows that:

* A 12-byte preamble, entitled the header.
* One or more chunks that contains JSON content and binary data.

#### Header ####

The GLB file format header consists of three 4-byte entries:

* uint32 magic - magic equals 0x46546C67. It is ASCII string glTF, and can be used to identify data as Binary glTF
* uint32 version - indicates the version of Binary glTF container format
* uin32 length - the total length of the Binary glTF, including Header and all chunks in bytes

#### Chunks ####

Each chunk in a GLB file has the following structure:


|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - length of chunkData in bytes
* `chunkType` - indicates indicates the type of chunk
* `chunkData` - binary payload of chunk

where the chunk types are:


|# |Chunk Type|ASCII|Description|Occurrences
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Structured JSON content|1
|2.|0x004E4942|BIN|Binary buffer|0 or 1

The start and end of each chunk must be aligned to 4-byte boundary and padding should be used for this purpose.

##### Structured JSON Content #####

This should be the very first chunk of Binary glTF asset and enables the implementation to progressively retrieve resources from subsequent chunks. This also provides the capability to read only a selected subset of resources from a Binary glTF asset such as the coarsest LOD of a mesh. In order to meet the alignment requirements, this chunk must be padded with trailing Space chars (0x20).

##### Binary Buffer #####

This chunk contains the binary payload for geometry, animation key frames, skins, and images. It should be the second chunk of the Binary glTF asset and must be padded with trailing zeros (0x00) to satisfy the alignment requirements.

## References ##

* [GLB File Format Specifications - Khronos](https://wiki.fileformat.com/3D/GLTF/)
