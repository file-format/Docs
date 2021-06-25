{
  "date" : "2021-03-23",
  "keywords" : [ "OEBZIP", "Open eBook Publication Structure", "extension", "format", "eBook", "OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about OEBZIP file format and APIs that can create and open OEBZIP files.",
  "title" : "OEBZIP - Compressed Open eBook Publication Structure",
  "linktitle" : "OEBZIP",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-03-22"
}

## What is an OEBZIP file? ##

The OEBZIP files were introduced by the International Digital Publishing Forum (**IDPF**). Likewise, [OEB](/ebook/oeb/), these files are XML-based specification for the structure, content, and presentation of electronic books but it is in compressed or zip form.

## Technical Details of OEBZIP File Format ##

The OEBZIP provided more new functionality in the area of rendering control, including, among other things, improvements in the markup vocabulary (now a basic subset of XHTML 1.1), and widely expanded CSS support. Sustainability factors are unchanged from the earlier version.

The OEBZIP file format consists of a set of files, including a compulsory package file, which includes a manifest listing all the other component files, and a spine, which indicates logical reading order. Moreover, to text in [XML](/web/xml/), a reader for OEBZIP files must be able to render images in [JPEG](/image/jpeg/) and [PNG](/image/png/) formats. Content components in other formats may be incorporated, but fallback content must be provided in one of the basic OEB formats.
  
The OEBZIP bundle of files was used primarily as a mid-state format, with publication to end-users managed through publishers or aggregators who provided eBooks in forms suitable for different eBook viewers. Its successor version, [EPUB](/ebook/epub/) is more likely to reach end-users in a final-state format, as well as serving as a mid-state format.

## References

* [OEBPS (Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [Open eBook](https://en.wikipedia.org/wiki/Open_eBook)

