{
  "date" : "2021-07-07",
  "keywords" : [ "INI", "extension", "file", "format", "system", "Initiation", "directory extension", "programs", "computer", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "INI - Initiation File Format",
  "description":"Learn about INI file format and APIs that can create and open INI files.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-07-07"
}

## What is an INI file? ##

An INI file is a message configuration document for computer programs that contain public keys for characteristics and sections that organize the attributes in a framework and grammar. These system file format configuration documents get their name from the MS-DOS operating system's directory extension INI, which stands for initiation. It popularised this form of software setup. Many programs on other software applications use various file name additions, such as [CONF](/system/conf) and [CFG](/system/cfg), although the format has established an unofficial standard in many situations of configuration.

## Brief History ##

Initially, Windows' principal program configuration technique was a text file format that consisted of lines of text with one crucial pair per line, divided into sections. Device drivers, typefaces, and starting launchers were all stored in this format. Individual settings were also commonly stored in INI files by apps. 
Up until Windows 3.1x, the format was supported on 16-bit Microsoft Windows platforms. Beginning with Windows 95, Microsoft began to encourage developers to use the Windows Registry instead of INI files for configuration.

## Technichal Specification ##

### Keys/Properties ###

The key/property is the most basic element of an INI file. An equals symbol (=) separates the name and value of each key. To the left of the equals sign is where the name displays. The equal symbol and semicolon are discreet letters in the Windows system hence cannot be used in the key. Any character can be used in the value.

```
name=value
```

### Sections ###

The section comment appears in square brackets ([]) on its own line. After the section definition, all keys are linked to that section. Sections finish at the very next section designation or the document's end; there is no specific "end of section" separator. Sections cannot be stacked; they can only be named once and are not required to be linked.

```
[section]
a=a
b=b
```

### Changing features ###

The INI file format does not have a globally accepted definition. Many computer applications include functions in addition to those already mentioned. The list below includes some common characteristics that may or may not be included in any individual program.

* Comments
* Escape characters 
* Duplicate names 


## INI Example ##

The sample INI file looks as follow:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Reference ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)