---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI File Format
linktitle: MYI
description: Learn about MYI file format and APIs that can create and open MYI files.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## What is an MYI File? ##

MYI is also known as the MySQL MyISAM Index file. It is used to store indexes for the MyISAM table by MySQL. MySQL database index defines the structure of the table and contains the control mechanism to check the integrity of tables.

## MYI File Format ##

MYI file has two parts, the header, and the key values.

### MYI Header ###

The header contains information about options, file sizes, and keys. The keys in MySQL are created with a command like

```sql
CREATE [UNIQUE] INDEX.
```

The files that read and write MYI files are in the ./myisam directory. It has the following files:

- mi_open.c: This file contains the routines that write each section of the header.
- mi_create.c: This file has the routines that call mi_open.c routines.
- myisamdef.h: This file has the structure definitions.

The header has the following sections:

- state: The state is written by mi_open.c, mi_state_info_write(). This structure occurs once in the file.
- base: The base is written by mi_open.c, mi_base_info_write(). The MI_BASE_INFO is the corresponding structure for the base in myisamdef.h. This structure occurs once in the file.
- keydef: The keydef is written by mi_open.c, mi_keydef_write(). The MI_KEYDEF is the corresponding structure for the keydef in myisamdef.h. It is a multiple-occurrence structure that appears for each index.
- recinfo: The recinfo is written by mi_open.c, mi_recinfo_write(). The MI_COLUMNDEF is the corresponding structure for the recinfo in myisamdef.h. It is a multiple occurrence structure that appears once of each field that appears in a key.

### Key Values ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. A normal block is at least 65% full and is typically 80% full.

The myisamdef.h file contains the following information expressed in constants. The maximum number of keys is 32 (MI_MAX_KEY) and the maximum number of segments in a key is 16 (MI_MAX_KEY_SEG). The maximum length of the key is 500 (MI_MAX_KEY_LENGTH). The maximum length of the block is 16384 (MI_MAX_KEY_BLOCK_LENGTH).

## References ##

- [The .MYI File](https://dev.mysql.com/doc/internals/en/the-myi-file.html)
