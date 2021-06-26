{
  "date" : "2020-11-11",
  "keywords" : [ "BAK", "extension", "file", "file format", "BAK File Type", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about BAK file format and APIs that can create and open BAK files.",
  "title" : "BAK File Format - Database Backup File",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2020-12-04"
}

## What is a BAK file?

A file with .bak extension is usually a backup file that is used by different software tools to store backups of data. From database perspective, a BAK file is used by Microsoft SQL Server for storing the contents of a database. All the data and files associated with the database are stored in this file format to be retrieved in case the database may become corrupt or invalid for any reason. The backup files can be stored and indexed on other servers for safety purpose. Several applications can create BAK files such as SQL Server Management Studio, Transact-SQL, and Windows PowerShell.

## BAK File Format

The internal details of a BAK file are not known but it is widely assumed that it is based on the Microsoft Tape Format (MTF). [MTF specifications](https://library.conholdate.app/view/jwAHlkZkKqF6yeqxe/mtf-file-format-specifications.pdf) are available and can be referenced for understanding the structure of the file. The document provides details about MTF storage for anyone who has a general knowledge about storage management operations, tape drives, and file systems.

### Data Sets

A data set is a collection of objects written to a storage media (tape, optical disk, etc.) during data backup or restore. Data sets comprise of multiple media in case of large volume of data.

### Fundamental Elements of MTF

An MTF file consists of some fundamental elements that constitute its building blocks. These elements are:

#### Descriptor Blocks

Descriptor blocks (DBLK) are used for format control and constitute the primary foundations of an MTF file. A single MTF file defines multiple DBLKs for each unique role. Each DBLK is a variable length block of data that is divided into following four parts:

 * `Common Block Header` - Fixed length structure that is common to all DBLKs. This is the only Block Header which is required.
 * `DBLK Type Information` - Fixed Length block specific to the type of DBLK being defined
 * `Operating System Data` - Specific data that is defined based on the type of DBLK and Operating systems
 * `DBLK Information` - Variable length DBLK specific information that cannot be saved with the Fixed Length DBLK information.

 {{< figure src="../bak.png" alt="Microsoft SQL Backup File Format" >}}

#### Data Stream

Data streams in a MTF file are used for data encapsulation and alignment. It comprises of a Stream Header, followed by the Stream Data. A stream header can encapsulate only a single type of Stream Data.

{{< figure src="../bak_datastream.png" alt="Microsoft SQL Backup File Format" >}}

#### FileMarks

A filemark is used for logical separation and quick access within a media. Filemarks are emulated by device driver or by use of the Soft Filemark Descriptor block in case the device being used does not provide filemarks.

## References ##

* [Microsoft Tape Format](https://library.conholdate.app/view/jwAHlkZkKqF6yeqxe/mtf-file-format-specifications.pdf)
