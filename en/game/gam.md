{
  "date" : "2021-09-08",
  "keywords" : [ "gam file", "gam file format", "what is a gam file", "file", "gam example", "gam file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about GAM file format and APIs that can create and open GAM files.",
  "title" : "GAM - Saved Game File",
  "linktitle" : "GAM",
  "menu" : {
    "docs" : {
      "parent" : "game"
    }
  },
  "lastmod" : "2021-09-08"
}

## What is a GAM file?
A file with .gam extension are used by various video games to get engage the gamers to continue where they left off the next time the program is opened. Hence, it means that the GAM file saves the information of what a user has done at what time. These file may saved automatically by the gaming softwares or the gamers may be asked to save if they want continue the state of game where they are leaving.
## GAM file format
GAM file format is basically used to hold game data in save games. The GAM file does not store creature, item information or area, instead, it saves data on the party members and the general or global variables which affect party members.
### Structure of GAM file
The GAM file has the following structure:
- Header
- Party members
- Party member CRE file data
- NPCs (who are not in the party)
- NPC kills statistics (embedded in NPC struct)
- NPC CRE file data
- Variables (in the GLOBAL namespace)
- Journal entries
- Familiar information
- Stored Locations
- Pocket Plane Locations
- Familiar Extra


 



## References 

* [GAM file format](https://gibberlings3.github.io/iesdp/file_formats/ie_formats/gam_v2.0.htm#GAMEV2_0_Stored)

