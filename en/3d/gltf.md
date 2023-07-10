{
  "date" : "2019-12-12",
  "keywords" : [ "GLTF", "file", "extension", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about GLTF files and APIs that can create and open GLTF files.",
  "title" : "GLTF - GL Transmission File Format",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a GLTF file?

glTF (GL Transmission Format) is a 3D file format that stores 3D model information in JSON format. The use of JSON minimizes both the size of 3D assets and the runtime processing needed to unpack and use those assets. It was adopted for the efficient transmission and loading of 3D scenes and models by applications. glTF was developed by the Khronos Group 3D Formats Working Group and is also described as [JPEG](/image/jpeg/) of 3D by its creators.

GLTF file format defines an extensible, common publishing format for 3D content tools and services that streamlines authoring workflows and enables interoperable use of content across the industry. The intention behind the creation of glTF file format was to define an extensible, common publishing format for 3D content tools and services that should streamline authoring workflows and enable interoperable use of content across the industry. It minimizes runtime processing by applications using WebGL and other APIs.

## Brief History of GLTF File

The first specifications for glTF file format 1.0 were announced in October 2015. This had come as a series of efforts that started in March 2012 by Khronos. The aim of these efforts were to assess the opportunities around the WebGL traction. Resultantly, the first demo of glTF format, based on the JSON format was presented at the WebGl meetup in 2012. The format was adopted by several companies from time to time including Cesium, 3D Tiles, Oculus, Microsoft, Archilogic and others.

glTF 2.0 was published on June 5, 2017 at the Web3D 2017 Conference. There is a long list of companies that adopted the glTF file format after that.

## GLTF File Format

The file format specifications for glTF 2.0 are available [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) for reference and should be consulted in any implementation related to reading/writing for support of glTF file format.

glTF defines assets as JSON files with supporting external data. It represents 3D models with the help of:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Binary files (.bin) containing geometry and animation data, and other buffer-based data
* Image files ([.jpg](/image/jpeg/), [.png](/image/png/)) for textures

Any external assets such as images are stored in external files that are referenced via URI. These URIs are stored alongside the GLB container or embedded directly into the JSON using data URIs. Each valid glTF must specify its version.

glTF has been designed to achieve small file size, fast loading, complete 3D scene representation and extensibility. These unique design goals are the main reasons for the popularity of glTF file format in 3D domain. Following are the mime types supported by the glTF file format for different file types:

* .gltf files use model/gltf+json
* .bin files use application/octet-stream
* Texture files use the official image/* type based on the specific image format. For compatibility with modern web browsers, the following image formats are supported: image/jpeg, image/png.

### JSON Encoding

glTF imposes following additional restrictions on JSON file format

To simplify client-side implementation, glTF has additional restrictions on JSON format and encoding.

1. JSON must use UTF-8 encoding without BOM.
1. All strings defined in this spec (properties names, enums) use only ASCII charset and must be written as plain text, e.g., "buffer" instead of `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Names (keys) within JSON objects must be unique, i.e., duplicate keys aren't allowed.

### URIs

Buffers and Image resources are referenced via URIs. The following two URI types must be supported by the clients.

**Data URIs:** The Data URIs are as defined by the RFC 2397 and are used by glTF to embed resources in the JSON.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## References ##

* [glTF 2.0 Specifications - Khronos](https://github.com/KhronosGroup/glTF)
* [glTF File Format - By Wikipedia](https://en.wikipedia.org/wiki/GlTF)
