{
  "date" : "2021-08-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ODM - OpenDocument Master Document File",
  "description":"Learn about ODM file format and APIs that can create and open ODM files.",
  "linktitle" : "ODM",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
    }
  },
  "lastmod" : "2021-08-04"
}

## What is an ODM file?

A file with .odm extension is an OpenDocument Master document file that contains one or more [.odt](/word-processing/odt/) files linked in it. These subdocuments are all combined in the single master document. This makes it easy to manage all the linked files from the single master document. Master document files can be created with Apache OpenOffice Writer or OpenDocument Word Processor. ODM files can be exported to single ODT file using the export option from within the OpenOffice Writer application.

## ODM File Format - More Information

ODM files are save as text files that can be opened in OpenOffice Writer. A single ODM file consists of multiple sections which are linked to the .odt subdocuments. This allows multiple writers to edit their ODT documents which are linked in the master ODM file. Thus, the master ODM file gets updated as every writer updates his respective sections.

ODM files may also include a table of contents and an index. Each time a Master document is opened, the master document writer asks for updating the links. It is must to say yes in order for the content to be shown properly.

## References

* [Master Documents](https://wiki.openoffice.org/wiki/Documentation/UserGuide/Writer/MasterDoc)
* [Creating one file from a master document and its subdocuments](https://wiki.openoffice.org/wiki/Documentation/OOo3_User_Guides/Writer_Guide/Creating_one_file_from_a_master_document)
