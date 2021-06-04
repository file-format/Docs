{
  "date" : "2021-02-01",
  "keywords" : [ "usdz", "usdz file", "usdz file format", "file format", "3d","usdz file download"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "USDZ - Universal Scene Description ZIP Format",
  "description":"Learn about USDZ file format and APIs that can open and create USDZ files.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2021-02-01"
}

## What is a USDZ file?

A file with .usdz is an uncompressed and unencrypetd ZIP archive for the [USD](/3d/usd/) (Universal Scene Description) file format that contains and proxies for files of other formats (such as textures, and animations) embedded within the archive and runs them directly with the USD run-time without any need of unpacking. USDZ files are packages whose design is based on the new Ar-level abstraction of a package. Usdz was registered with IANA and has media type name of model and a subtype name of vnd.usd+zip and its details can be found as on [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## USDZ File Format

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### ZIP Constraints

USDZ file format uses the ZIP file format without any `compression` and `encryption`. This was aimed by design to meet two requirements:

 * For a package already loaded into memory or as a single file on disk, the API's available in USD for accessing the data contained within the image
 * There should be no need to extract files to disc or allocate more heap storage

With USDZ, both these requirements are met as most of the image formats themselves allow internal compression schemes, resulting in compact file size.

### Layout Requirements

USDZ packages require the layout of files within the package is that the data for each file should begin at a multiple of 64 bytes from the beginning of the package. However, the package should start with a native [USD](/3d/usd/) file in case of targeting the package with a simple reference. In such a case, this first USD file is referred as the Default Layer. Clients wishing to deliver "streamable content" may wish to consider other layout constraints, as well.

## USDZ file download
Since the usdz files are packed with other high quality images and usd files, they can occupy greater disk storage. Here you can find a simple and smaller USDZ example file for download:

- [Sample.usdz](../sample.usdz)

## References

* [USDZ File Format Specifications](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)
