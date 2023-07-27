{
  "date" : "2022-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about TRM file format and APIs that can create and open TRM files.",
  "title" : "TRM File Format - Oracle Trace Map File",
  "linktitle" : "TRM",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-08-24"
}

## What is Oracle TRM file?

A TRM file is a metadata file format used by Oracle 11g relational database management system (RDBMS). It is stored alongside the Oracle Trace files ([.trc](/database/trc/)) and contains structural information about the trace file. The purpose of TRM file is to facilitate for searching and navigation the records using the metadata informaiton. Oracle software can be used to open TRM files.

## TRM File Format

TRM files are saved in Oracle's proprietary file format and the TRM file format details are not available publicly. A typical TRC file contains Oracle process SID, the process name, and the OS process number. The TRM files contain detailed metadata information about these TRC files for searching and navigation.

## References ##

* [What is .trm file in oracle 11g?](https://forums.oracle.com/ords/apexds/post/what-is-trm-file-in-oracle-11g-0659)
