{
  "date" : "2021-01-21",
  "keywords" : [ "ai file", "ai file format", "what is a ai file", "file", "ai example", "ai file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AI - Adobe Illustrator Artwork File",
  "description":"Learn about AI file format and APIs that can create and open AI files.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-01-21"
}

## What is an AI file?

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## AI File Format

AI is Adobe Illustrator's proprietary file format and uses the dual path approach similar to PGF for saving EPS-compatible files. The [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) provide a detailed developer's reference for internal details of this file format. All The documents (files) created by Adobe Illustrator are PostScript language documents and has two main parts conforming to the Document Structuring Conventions: a `prolog` and a `script`.

### Prolog

The prolog section encapsulates information required for interpretation of the file. An example would be the bounding box that contains all the marks on the page.  It also contains resources information such as fonts and procedure definitions. These resources are logically grouped into sets called procsets and contain explicit methods for initializing and terminating their procedures.

### Script

Graphic elements on the page are described by the script. A script contains references to the operators and procedures in the prolog, along with operands and data. The three logical sections of a script include:

 * Setup Sequence - that initializes and activates the resources defined in the prolog
 * Sequence of descriptive operators
 * Trailer that deactivates resources

Operators in the script are sequences of graphic elements written in the language defined by procsets in the prolog. These sequences consist of collections of data elements, graphic attribute definitions, and calls to the procedures defined in the procsets.

### Object Tags

Object tags are used to attach custom information to an Adobe Illustrator art object. Tags consist of a:

 * Tag identifier
 * Tag type
 * Data

## References
* [Adobe Illustrator File Format Specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [AI File Format by PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)
