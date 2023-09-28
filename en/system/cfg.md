{
  "date" : "2021-06-29",
  "keywords" : [ "CFG", "extension", "file", "format", "system", "configuration", "settings", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CFG - File Format",
  "description":"Learn about CFG file format and APIs that can create and open CFG files.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-06-29"
}

## What is a CFG file? ##

A file with a .cfg extension is a type of "settings" file. It is a popularly used file type and used to store information regarding configuration and settings for computer programs. Most types of CFG files are stored in text format and should not be opened manually, instead, they should be opened using a text editor. However, there are different types of CFG files, that differ in the format with which the information is stored. The features that CFG files offer vary from application to application. Some computer applications enable the users to modify, or develop their configuration files syntax by the use of graphical interferences, while others only allow modifications using a text editor. After modifying these files, the users can instruct the application to read these files again and apply the modifications to the system. 


## CFG File Format ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. The format that these files are stored and used in each of these operating systems vary. Most systems used and store these files in a human-readable and editable plain text format, while others store in it a more complex format, depending on the files usage and the operating system’s requirement.

In Unix and Unix-like operating systems, most CFG files several different format styles for CFG files are used, however, the most common format is an easily readable plain text format, and almost all of the formats allow comments to be made and edited. The most common file extensions for CFG files in these operating systems are CNF, CONF, CF, and INI. 

In MS-DOS operating system there was initially only one configuration file format, namely, plain-text, however, MS-DOS 6, brought with it the introduction of an INI configuration file format.

macOS uses a standard property list format style configuration file.

In Microsoft Windows, Plain text INI style configuration files were an important source of storing and editing information, however, a new database system was introduced in 1993, leading to a decrease in the use of configuration files in Microsoft Windows after 1993.


## CFG Example ##

A sample CFG file can be seen below:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

## Other CFG files

Here are other file types that use the **.cfg** file extension.

**Settings**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Game**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)
