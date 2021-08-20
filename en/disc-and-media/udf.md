{
  "date" : "2021-08-17",
  "keywords" : [ "udf file", "udf file format", "what is a udf file", "file", "udf example", "udf file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
   "toc" : true,
  "description" : "Learn about UDF file format and APIs that can create and open UDF files.",
  "title" : "UDF - Universal Disk Format File",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
    }
  },
  "lastmod" : "2021-08-17"
}

## What is a UDF file?
The file with .udf extension is a disc imaging format typically used for saving files on optical media; can be used for burning DVDs, CDs, and other optical media; stores a collection of files using the directory structure specified in the UDF standard; allows files to be deleted and modified on the target disc even after they have been written. The Optical Storage Technology Association set the UDF file system as a standard to form a common file system for all optical media such as for re-writable optical media and read-only media.

## UDF file format 
The UDF file format is an open vendor-neutral file system for computer data storage for a wide range of media. It has been used commonly for DVDs and newer optical disc formats. Usually, the software masters a UDF file system in a batch process and write it to optical media in a single pass. However, when it writes packets to rewritable media, the UDF allows files to be created, deleted and changed on-disc similar to a general-purpose filesystem would on removable media like flash drives or floppy disks.
### UDF Specifications
The UDF standard defines the following three file system variations:

- **Plain Build**:This is the original format supported in all UDF revisions. It was introduced in the first version of the standard, this format can be used on any type of disk that enables random read or write access, such as DVD+RW, hard disks, and DVD-RAM media. 
- **VAT build**: Used specifically for writing to write-once media. The VAT is an additional structure on the disc that allows packet writing; that is, remapping physical blocks when files or other data on the disc are modified or deleted. For write-once media, the entire disc is virtualized, making the write-once nature transparent for the user; the disc can be treated the same way one would treat a rewritable disc.
- **Spared (RW) build**: Used specifically for writing to rewritable media. It adds an extra Sparing Table to manage the faults that will eventually occur on parts of the disc that have been rewritten multiple times. This table saves track of worn-out sectors and remaps them to working ones. The defect management of UDF does not apply to systems that already implement another form of defect management, such as Mount Rainier (MRW) for optical discs, or a disk controller for a hard drive.
 



## References 

* [Windows Imaging Format - by Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)

