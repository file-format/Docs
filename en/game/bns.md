{
  "date": "2021-10-20",
  "keywords": [
    "bns file",
    "bns file format",
    "what is a bns file",
    "file",
    "bns example",
    "Portal Bonus Map Script file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about ortal Bonus Map Script BNS file format and APIs that can create and open BNS files.",
  "title": "BNS - Portal Bonus Map Script File",
  "linktitle": "BNS",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-bns"
    }
  },
  "lastmod": "2021-10-20"
}

## What is a BNS file?

A file with .bns extension is a game script file created with Portal Map puzzle solving game that was developed by Valve. It contains text script for defining information about a Portal map which is stored as .bsp file. BNS files are used as reference to this actual map file and contains a list of challenges that are to be completed. In addition, it contains map name, comments about the map, and thumbnail image file references. A BNS file can be opened in any text editor such as Notepad++, textEdit, and Notepad.

## BNS File Format

BNS files are saved as plain text files that are human readable. These can be opened in text editors and edited as well. However, these should be carefully edited to avoid any errors in the script.

## BNS File Format Example

A BNS file may look something like the following when it is opened in a text editor such as Notepad++.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## Parts of a BNS File

In the above example,

 * `#Bonus_Map_Challenges` - Represents the name of the map.
 * `map` -  Represents the name of the map to be put in game's maps folder
 * `chapter` - Represents the chapter the map belongs to. All the chapter files are located in the VPK file by adding the name of the map in the format `map your_map_name`
 * `Image` - It contains the thumbnail of the map and is stored at the root path steam\steamapps\common\portal\portal\materials\VGUI.
 * `Comment` - Descriptive text about the map created.

## References

 * [Portal Challenge Script](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)
