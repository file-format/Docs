{
  "date": "2022-05-25",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about FMPSL file format and APIs that can create and open FMPSL files.",
  "title": "FMPSL File Format - FileMaker Pro 12 Snapshot Link File",
  "linktitle": "FMPSL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-fmpsl"
    }
  },
  "lastmod": "2022-05-25"
}

## What is an FMPSL file?

An FMPSL file is a snapshot file of database created with FileMaker Pro 12. It stores the queried results from the database along with other information such as visual layout and visible information. The FMPSL file can be used to restore all this data in another instance of FileMaker Pro database. This file format was introduced with the launch of FileMaker Pro v 12. Prior to this version, the snapshot links were introduced as FPSL file format in FileMaker Pro v 11. FMPSL files can be opened with FileMaker Pro Advanced software. Other file formats supported by FileMaker Pro include [FP5](/database/fp5/), [FP7](/database/fp7/), and [FMP12](/database/fmp12/).

## FMPSL File Format

The internal file format details of FMPSL files is not available publicly for developer's reference.

### How to Save Records as FMPSL file?

Data from FileMaker Pro database can be saved as snapshot link file using the following steps.

 1. Search the records from database that are required to be saved as a snapshot link file.
 1. Using the Send Record As Snapshot Link option from menu, save the file by entering a filename.
 1. Use the Records being browsed to save the entire found set of records.

The generated snapshot file will be saved to disc with the specified name.

## References

 * [Convert Earlier Versions of FileMaker Pro File Formats to FMP12 File Format](https://fmhelp.filemaker.com/help/16/fmp/en/index.html#page/FMP_Help/converting-files.html)
 * [Save Records as a Snapshot Link File](https://fmhelp.filemaker.com/help/12/fmp/en/html/import_export.17.5.html)
