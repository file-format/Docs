{
  "date" : "2023-05-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CPIO File - Unix CPIO Archive File Format",
  "description":"Learn to know what is a CPIO file and APIs that can create and open CPIO files.",
  "linktitle" : "CPIO",
  "menu" : {
    "docs" : {
      "identifier" : "compression-cpio",
      "parent" : "compression"
    }
  },
  "lastmod" : "2023-05-10"
}

## What is a CPIO file?

A CPIO file is an  archive file created in Unix's Copy In Copy Out (CPIO) format. It is similar to the TAR file format other than that it is uncompressed. CPIO files can store device files, symbolic links and extended file attributes.

## CPIO File Format

A CPIO archive is created as a binary file that is not human-readable. It stores the collection of files and directories. The contents of a CPIO archive is identified with metadata information such as file names, permissions, ownership, and timestamps. This metadata information is also stored in the archive file for lateral access by the system.

## Format of CPIO Archive

A CPIO file comprises of one or more concatenated member files. Each file in the archive consists of a header optionally followed by file contents as mentioned in the header. The archive contains another header at the end that is described by an empty file named TRAILER!!.

### Types of CPIO Archives

There are two types of CPIO archives. These different only in the style of the header.

* ASCII Archives - These CPIO archives have a printable header that becomes part of the CPIO archive if the archive itself consists of ASCII files
* Binary Archives - These CPIO archives have binary headers.

## Working with CPIO Archive

### How to Create CPIO Archives?

You can create a CPIO on Unix-like systems using the **cpio** command. The following command will find all files and directories in a the current directory and its subdirectories. This output is then pipe to the cpio command that will generate a new CPIO archive named archive.cpio.

```
find . -depth -print | cpio -ov > archive_cpio.cpio
```
### How to Extract Files from CPIO Archives?

The following command extracts the files from an existing archive.

```
cpio -id < archive_cpio.cpio
```
It will read the archive.cpio file from standard input and extract the files to the current directory.


## References

* [CPIO - By Wikipedia](https://en.wikipedia.org/wiki/Cpio)
* [CPIO File Format](https://www.ibm.com/docs/en/zos/2.2.0?topic=formats-cpio-format-cpio-archives)
