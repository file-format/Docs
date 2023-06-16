{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about 4DL file format and APIs that can create and open 4DL files.",
  "title" : "4DL - 4th Dimension Database Log File",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2023-06-14"
}

## What is a 4DL file?

A 4DL log file is utilized to record modifications made to a 4D database (.4DD) file. This file is stored alongside the database file and shares a similar filename. Its purpose is to accurately track and maintain a comprehensive record of the updates implemented within the database. A [4DD file](/database/4dd/), as compared to the 4DL file, is mainly associated with the 4th Dimensions by the 4D Inc.

## 4DL File Format - More Information

Typically, multiple 4DL files are stored together with a 4DD file. Thus the first version of the log file may be named as 0001.4dl, but the lateral versions of the log files will be saved as 0002.4dl, 0003.4dl, and so on. Now, if the log file itself undergoes 3 subsequent saves, it will be labeled as "db1[0005-0003].4dl."

## References

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))