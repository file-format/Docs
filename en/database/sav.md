{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about SAV file format and APIs that can create and open SAV files.",
  "title" : "SAV - SPSS Data File",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-06-14"
}

## What is a SAV file?
SAV file is a data file created by Statistical Package for the Social Sciences(SPSS), which is an application widely used by market researchers, health researchers, survey companies, government, education researchers, marketing organizations, data miners for statistical analysis. The SAV saved in a proprietary binary format and consists of a dataset as well as a dictionary that represent the dataset, saves data by rows and columns.

## SAV File Format
The SAV file format has become relatively stable but we can't say it static. Backwards and forwards compatibility is optionaly available where necessary, but not maintained properly. The data in an SAV file is categorized into following sections: 

### File header
It consists of 176 bytes. The first 4 bytes indicate the string **$FL2** or **$FL3** in the character encoding used for the file. The last three bytes represent that the data in the file is compressed using **ZLIB**. The next 60-byte string begins **@(#) SPSS DATA FILE** and also determines the operating system and SPSS version that created the file. The header then continues with six digit fields, containing the number of variables per observation and a digit code for compression, and ends with character data indicating creation date and time and a file label.
### Variable descriptor records
The record contains a fixed sequence of fields, classifing the type and name of the variable together with formatting information used by SPSS. Each variable record may optionally contain a variable label of up to 120 characters and up to three missing-value specifications.
### Value labels
The value labels are optional and stored in pairs of records with integer tags 3 and 4. The first record which is tag 3 has a sequence of pairs of fields, each pair containing a value and the associated value label. The second record which is tag 4, represents which variables the set of values/labels applies to.
### Documents
Single or multiple records with integer tag 6. Optional documentation. contains 80-character lines.
### Extension records
Single or multiple records with integer tag 7. Extension records provide information that can be ignored safely, but preserved, in many situations, enables for files written by newer software to preserve backward compatibility. Extension records have integer subtype tags.
### Dictionary terminator
Only record with integer tag 999. It separates dictionary from data observations.
### Data observations
It is considered as data is in observation order, e.g. all variable values for the first observation, followed by all values for the second observation, etc. The format of the data record varies depending on the compression code in the file header record. The data portion of a .sav file can be uncompressed: 
- **code 0**: compressed by bytecode 
- **code 1**: compressed using ZLIB compression
 






## References ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)
