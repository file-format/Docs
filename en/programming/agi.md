{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AGI File - Asterisk Gateway Interface File Format",
  "description":"Learn about what is AGI file format with example and APIs that can create and open AGI files.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-10-30"
}

## What is an AGI file?

An AGI file is a script file used by the open source telephony system, Asterisk. It contains information that can be used to automate processes and Asterisk dialplan. Using AGI script files, connections can be established with relational databases such as PostgreSQL or MySQL. In addition, AGI scripts can be used to access other external resources as well. AGI scripts can turn over control of the dialplan to an external AGI script, enabling Asterisk to perform complex tasks.

## AGI File Format - More Information

AGI script files are saved as text files and can be opened in any text editor for making changes.

### Standard Pattern of AGI Communication

The AGI script loads the variables and their values sent to it by Asterisk. A common look of these variables is as follow.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

These variables are followed by a blank line sent by Asterisk, showing that the AGI script can take control of the dialplan now.

### Programming language for AGI Script Files

AGI scripts can typically be written in Perl, [PHP](/programming/php/), [C](/programming/c/), Pascal, or Bourne Shell.

## References

 * [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)
