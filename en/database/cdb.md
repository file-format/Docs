{
  "date" : "2021-06-16",
  "keywords" : [ "CDB", "extension", "cdb file", "cdb file format", "Database File Type", "Database File Format", "what is a cdb file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about CDB file format and APIs that can create and open CDB files.",
  "title" : "CDB - Constant Database File",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-06-16"
}

## What is a CDB file?
The CDB files are used in mission-critical applications like email. The CDB stands for "constant database", a fast, reliable and simple package for creating or reading constant databases. Database replacement is safe against system crashes. Users don't have to pause during a rewrite. CDB performs as an associative array (on-disk), mapping keys to values, and enables multiple values to be stored in a single key.

## CDB File Format

The CDB file format stores numbers, offsets, lengths, and hash values in little endian format as unsigned 32-bit integers. Keys and data are thought to be opaque byte strings with no special treatment. At the beginning of the database, the fixed-size header represents 256 hash tables by listing their position within the file and their length in slots. Usually the data is stored as a sequence of records, each record stores key length, data length, key, and data. There are no sorting or alignment rules. The records are followed by a set of 256 hash tables of varying lengths. Since zero is a valid length, there may be fewer than 256 hash tables physically stored in the database, but there are nothing considered to be 256 tables. Hash tables consists of a series of slots, each of which contains a hash value and a record offset. "Empty slots" have an offset of zero.

### Structure of CDB File Format

CDB database consists of an entire dataset in a single computer file. It contains three parts: 
- A fixed-size header 
- Data
- A set of hash tables. 

Lookups are available for exact keys only. Lookups act using the following algorithm:

- Hash the key.
- Determine at which hash table and slot this record should be located.
- Test the indicated slot in the hash table.

For lookups of keys with more than one values, additional values may be found by simply resuming the search at the next slot.

#### Features

CDB database structure provides several features:

##### Fast lookups
A successful lookup in a huge database normally takes just two disk accesses and an unsuccessful lookup takes only one. 
##### Low overhead
A database uses 2048 bytes, 24 bytes per record and the space for keys and data.
##### No random limits
CDB can manage any database up to 4 gigabytes. Since there are no other restrictions, the records don't even have to fit into memory. Databases are stored in a machine independent format.
##### Fast atomic database replacement
The command **cdbmake** can re-write an entire database into two orders of magnitude, faster than other hashing packages.
##### Fast database dumps
**cdbdump** can prints the contents of a database in cdbmake-compatible format.


## References ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [CDB specification](http://cr.yp.to/cdb.html)
