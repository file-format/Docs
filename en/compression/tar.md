{
  "date" : "2019-10-11",
  "keywords" : [ "tar file", "tar file format", "what is a tar file", "file", "tar example", "tar file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TAR - Unix Archive File Format",
  "description":"Learn about what is a TAR file and APIs that can create and open TAR files.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a TAR file?

Files with .tar extension are archives created with Unix-based utility for collecting one or more files. Multiple files are stored in an uncompressed format with the support of adding files as well as folders to the archive. TAR utility on Unix is Command based, but files hence created are supported by most file archiving systems on almost all operating systems. It was first created in 1979 by the AT&T Bell Laboratories and subsequent versions were published with the passage of time.

## TAR File Format

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. The data sets created by tar retain information about file system parameters such as:

* Name
* Time Stamps
* Ownership
* File Access Permissions
* Directory Organization

A TAR file doesn't have any magic number. It contains a series of blocks where each block is of BLOCKSIZE bytes.

Each file archived is represented by a header block which describes the file, followed by zero or more blocks which give the contents of the file. At the end of the archive file there are two 512-byte blocks filled with binary zeros as an end-of-file marker. A reasonable system should write such end-of-file marker at the end of an archive, but must not assume that such a block exists when reading an archive. In particular GNU tar always issues a warning if it does not encounter it.

The blocks may be blockedfor physical I/O operations. Each record of n blocks (where n is set by the blocking-factor = 512-size option to tar) is written with a single "write()" operation. On magnetic tapes, the result of such a write is a single record. When writing an archive, the last record of blocks should be written at the full size, with blocks after the zero block containing all zeros. When reading an archive, a reasonable system should properly handle an archive whose last record is shorter than the rest, or which contains garbage records after a zero block.

### TAR File Header

Like any other file headers, the tar file header record contains metadata about a file and is shown in the following table.

|Field offset|Field size (Bytes)|Field
---|---|---|
|0|100|File name
|100|8|File mode
|108|8|Owner's numeric user ID
|116|8|Group's numeric user ID
|124|12|File size in bytes (octal base)
|136|12|Last modification time in numeric Unix time format (octal)
|148|8|Checksum for header record
|156|1|Link indicator (file type)
|157|100|Name of linked file

Unused fields are filled with NUL bytes. A header comprises of 257 bytes which is padded with NUL bytes to make it fill to 512 byte record.

## How to Create a TAR File

### Create TAR File on Windows

On Windows, you can use the Windows Subsystem for Linux (WSL) or third-party tools like 7-Zip to create TAR files. Here's how to do it using WSL:

 1. Install WSL if you haven't already. You can install it through the Windows Features settings.

 1. Open a WSL terminal and use the same tar command as on Linux or Unix systems to create a TAR file.

### Create TAF File on Linux from Command Line

To create a TAR file using the command line on Linux or Unix-based systems, open a terminal and use the tar command. You can create a TAR file in various compression formats (e.g., .tar.gz, .tar.bz2, .tar.xz), but here, we'll create a plain .tar file:

To create a TAR file from a single file or directory, use the following command:

```
tar -cvf archive.tar file_or_directory
```

## How to Open TAR File

### Open TAR File on Windows

You need to isntall a decompression utility on Windows OS such as 7-Zip. It is a free archiving utility that can be used to create and extract different compressed file formats. Right click your TAR file and select **Extract** option.

### Open TAR File on Mac

On a Mac, just double-click the TAR, TGZ, or TAR.GZ file to unpack it.

### Open TAR File on Linux

If you're using Linux or the Mac Terminal app, use "tar -xvf" for TAR files, or "tar -xvzf" for files ending in TGZ or TAR.GZ.

## References ##

* [TAR - By Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [TAR Basic Format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)
