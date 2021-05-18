{
  "date" : "2021-03-23",
  "keywords" : [ "OEB", "Open eBook Publication Structure", "extension", "format", "E-Book", "OEBPS","IDPF"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about OEB file format and APIs that can create and open OEB files.",
  "title" : "OEB - Open eBook Publication Structure",
  "linktitle" : "OEB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-03-22"
}

## What is an OEB file?
The OEB files were introduced by the International Digital Publishing Forum (**IDPF**). More formally, the OEB files are also known as **OEBPS**. These files are XML-based specification for the structure, content and presentation of electronic books. This fileformat has been superseded by the [EPUB](https://docs.fileformat.com/ebook/epub/) format.

## Technical details of OEB file format
The OEB file format consists of a set of files, including a compulsory package file, which includes a manifest listing all the other component files and a spine, which indicates logical reading order. Moreover, to text in XML, a reader for OEB files must be able to render images in JPEG and PNG formats. Content components in other formats may be incorporated, but fallback content must be provided in one of the basic OEB formats.

The OEBPS 1.2 was a tightly coupled update to the prior version (OEBPS 1.0.1). It provided modern functionality in the area of rendering control, including, among other things, enhancements in the markup vocabulary (now a genuine subset of XHTML 1.1), and greatly expanded CSS support. Sustainability factors are unchanged from the earlier version.
  
The OEB bundle of files was used primarily as a mid-state format, with publication to end-users managed through publishers or aggregators who provided ebooks in forms suitable for different ebook viewers. Its successor version, EPUB_2, is more likely to reach end-users as a final-state format, as well as serving as a middle-state format.

## References

* [OEBPS (Open Ebook Forum Publication Structure) 1.2](https://www.loc.gov/preservation/digital/formats/fdd/fdd000171.shtml)
* [Open eBook](https://en.wikipedia.org/wiki/Open_eBook)

