{
  "date" : "2021-03-05",
  "keywords" : [ "PDB", "Palm Digital Media", "eReader","extension", "format", "E-Book", "Digital book" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about Palm Digital Media PDB file format and APIs that can create and open PDB files.",
  "title" : "PDB - Palm Digital Media electronic book",
  "linktitle" : "PDB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
    }
  },
  "lastmod" : "2021-03-05"
}

## What is a PDB file?
The PDB Stands for Palm database. This is a format introduced by Palm Digital Media and it is widely used for smartphones and Palm devices. A version of The PDB format is known as PalmDOC eBook file is also available. The advancements of e-books has left this format behind due to the lack of support for DRM protection. It means that only royalty free text is typically available.The eReader is a freeware program in the market for viewing e-books using PDB files.

## PDB Viewing Software

The eReader is a software availble free of cost for viewing Palm Digital Media electronic books by using the pdb format. The versions are available for Palm OS, macOS, Android, IOS, Symbians, and windows smartphones. The reader displays the text of one page at a time, as paper books do. eReader supports embedded hyperlinks and images. Moreover, the Stanza application for the iPhone and iPod touch can read both encrypted and unencrypted eReader files.

The software supports bookmarks and footnotes to enable the users to mark any page with a bookmark and any part of the text with a footnote. Footnotes can later be exported as a Memo document.

On July, 2009, Barnes & Noble announced that eReader would be the preferred format to deliver e-books. Three months later, in a press release by Adobe, it was revealed Barnes & Noble would be joining forces with the software company to regulate the EPUB and PDF eBook formats. Barnes & Noble e-books are now sold mostly in EPUB format.

## Structure of PDB file

The PDB files contain:
- A PDB header
- PDB record headers  
- records

### PDB Header

The PDB header is located at the start of the file and contains meta information on the file:

| Offset |        Name         |             Type             |   Size   |
--------|---------------------|------------------------------|----------|
|  0x00  |        name         |  char (Modified ISO-8859-1)  | 32 Bytes |
|  0x20  |   file attributes   |           integer            | 2 Bytes  |
|  0x22  |       version       |           integer            | 2 Bytes  |
|  0x24  |    creation time    | 32bit integer - PDB Datetime | 4 Bytes  |
|  0x28  |  modification time  | 32bit integer - PDB Datetime | 4 Bytes  |
|  0x2c  |     backup time     | 32bit integer - PDB Datetime | 4 Bytes  |
|  0x30  | modification number |           integer            | 4 Bytes  |
|  0x34  |      app_info       |           integer            | 4 Bytes  |
|  0x38  |      sort_info      |           integer            | 4 Bytes  |
|  0x3c  |        type         |           integer            | 4 Bytes  |
|  0x40  |       creator       |           integer            | 4 Bytes  |
|  0x44  |   unique_id_seed    |           integer            | 4 Bytes  |
|  0x48  |  next_record_list   |           integer            | 4 Bytes  |
|  0x4c  |     num_records     |           integer            | 2 Bytes  |

### PDB Record Header

For each record, there is an 8-byte record header, containing:

|    name    |  type   |  size   |                                     notes                                     |
------------|---------|---------|-------------------------------------------------------------------------------|
|   offset   | integer | 4 bytes | Byte number in the PDB file (counting from zero), where the record is located |
| attributes |  byte   | 1 byte  |         Attributes of the record (delete/dirty/busy/secret/category)          |
|  UniqueID  | integer | 3 bytes |                                   Always 0                                    |

### PDB Records

The records themselves sequentially follow:

- The usual order is AppInfoArea
- SortInfoArea 
- records




## References

* [Most Common eBook Formats](https://www.the-ebook-reader.com/ebook-formats.html)
* [Comparison of e-book formats - By WikiPedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)
* [PDB (Palm OS) - By WikiPedia](https://en.wikipedia.org/wiki/PDB_(Palm_OS))