{
  "date": "2019-12-12",
  "keywords": [
    "CBC",
    "extension",
    "file",
    "format",
    "Comic books",
    "Comic Books File Format",
    "eBook"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about CBC file format and APIs that can create and open CBC files.",
  "title": "CBC - Comic Book Collection File Format",
  "linktitle": "CBC",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-cbc"
    }
  },
  "lastmod": "2021-03-03"
}

## What is a CBC file?

A file with .cbc extension is a compressed collection of Comic Book files for eBooks and contains [CBZ](/ebook/cbz/) and [CBR](/ebook/cbr/) files. It is used by [Calibre](https://calibre-ebook.com/), an eBook conversion application, which is a cross-platform open-source e-book manager and lets you manage your ebooks and convert these to different formats. A CBC file contains a .txt file, comics.txt, that lists other files which are part of the archive. Several applications are available online that can convert CBC files to [AZW3](/ebook/azw3/), [EPUB](/ebook/epub/), [FB2](/ebook/fb2/), [MOBI](/ebook/mobi/), [TXT](/word-processing/txt/), [PDF](/pdf/), and other popular file formats.

## CBC File Format

CBC files are compressed archives that contain CBZ, CBR, and a text file for listing the contents. The text file, comics.txt is UTF8 encoded and contains a list of the CBC files to be used by readers for organizing their collections. A CBC file has usually several attributes that allow the organization of this collection such as Comic, Category, Publisher, Series, Edition, and Artist.

Contents of a sample CBC file are listed as follows:

 * comics.txt - Text file that contains list of CBR and CBZ files
 * 1.cbz
 * 2.cbz
 * 3.cbz
 * CBZ file(s)

where the comics.txt file lists the contents as follows:

 * 1.cbz: First Chapter
 * 2.cbz: Second Chapter
 * 3.cbz: Third Chapter

Readers process the comics.txt file and generate the table of contents based on the provided data.

## References

* [Calibre](https://calibre-ebook.com/)
