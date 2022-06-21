{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about FZP file format and APIs that can create and open FZP files.",
  "title" : "FZP File Format - Fritzing XML Part Description File",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
    }
  },
  "lastmod" : "2022-06-20"
}

## What is a FZP file?

An FZP file is an XML file created by [Fritzing](https://fritzing.org/) electronic circuit prototyping and design application. It contains information about the part's properties, connectors, and buses in [XML](/web/xml/) file format. FPZ files can not be used independently in Fritzing. Instead, they are imported as part of FZPZ archive file.

## FZP File Format - More Information

FZP files are XML files that contain information about the part's properties, connectors, and buses. In addition to these, FZP files also contain information about the title, description, author and date of publishing of the FZP file. When a Fritzing part file is exported, the Fritzing app creates a the [FZPZ](/compression/fzpz/) compressed archive that contains an FZP file and four [SVG](/image/svg/) files.

The [FZP file format specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md) are available on Github by Fritzing.

## FZP File Structure Example

A typical FZP file has the following XML structure.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## References

* [FZP File Format Specifications](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [New parts with fzpz extension](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)
