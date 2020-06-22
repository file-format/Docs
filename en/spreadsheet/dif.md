{
  "date" : "2019-12-10",
  "keywords" : [ "DIF", "file", "extension", "file format", "Data Interchange File", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Your file format guide to know what is a DIF file and APIs that can create and open them.",
  "title" : "What is a DIF file?",
  "linktitle" : "DIF",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
    }
  },
  "lastmod" : "2019-12-10"
}

# What is a DIF file? #

DIF stands for Data Interchange Format that is used to import/export spreadsheets data between different applications. These include Microsoft Excel, OpenOffice Calc, StarCalc and many others. It stores data contained in a single spreadsheet which is the only limitation of this file format.

## Brief History ##

The DIF file format was developed by Software Arts, Inc. in the early 1980s. The file format specifications for DIF were included in VisiCalc which was the first spreadsheet program for personal computers. These specifications were copyrighted in 1981 and was a registered trademark of Software Arts Products Corp.

## DIF File Format ##

DIF store spreadsheet contents in ASCII text file that allows it to be viewed and edited with a text editor. The format owns its place in data serialization formats list for its characteristics of data interchange. A DIF file consists of 2 sections; a header and data.

Everything in DIF is represented by a 2- or 3-line chunk. Headers get a 3-line chunk; data, 2.

* Header chunks start with a text identifier that is all caps, only alphabetic characters, and less than 32 letters. The following line must be a pair of numbers, and the third line must be a quoted string.
* Data chunks start with a number pair and the next line is a quoted string or a keyword.

### Values ###

A value occupies two lines, the first a pair of numbers and the second either a string or a keyword. The first number of the pair indicates type:

* −1 – directive type, the second number is ignored, the following line is one of these keywords:
** BOT – beginning of tuple (start of row)
** EOD – end of data
* 0 – numeric type, value is the second number, the following line is one of these keywords:
** V – valid
** NA – not available
** ERROR – error
** TRUE – true boolean value
** FALSE – false boolean value
* 1 – string type, the second number is ignored, the following line is the string in double quotes

### Header chunk ###

The header chunk of a DIF file comprises of an identifier line followed by the two lines of a value. The numeric values in header chunks use just an empty string instead of the validity keywords. The details of these header chunks are as follow.

* TABLE - a numeric value follows of the version, the disused second line of the value contains a generator comment
* VECTORS - the number of columns follows as a numeric value
* TUPLES - the number of rows follows as a numeric value
* DATA - after a dummy 0 numeric value, the data for the table follow, each row preceded by a BOT value, the entire table terminated by an EOD value

### Example ###

Following example shows the contents of a simple worksheet and its equivalent DIF representation.


|Name|Age
---|---|
|Bob|34
|Sheetal|22

```
TABLE
0,1
"EXCEL"
VECTORS
0,3
""
TUPLES
0,2
""
DATA
0,0
""
-1,0
BOT
1,0
"Name"
1,0
"Age"
-1,0
BOT
1,0
"Bob"
0,34
V
-1,0
BOT
1,0
"Sheetal"
0,22
V
-1,0
EOD
```

## References ##

* [ DIF - By Wikipedia](https://en.wikipedia.org/wiki/Data_Interchange_Format)
