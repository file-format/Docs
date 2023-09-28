{
  "date": "2023-09-27",
  "keywords": [
    "cfg",
    "cfg file",
    "cfg wesnoth markup language file",
    "what is a cfg file",
    "how to open cfg file",
    "file",
    "cfg file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "CFG File Format - Wesnoth Markup Language File",
  "description": "Learn about CFG Wesnoth Markup Language File format and APIs that can create and open CFG files.",
  "linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
      "parent": "game"
    }
  },
  "lastmod": "2023-09-27"
}

## What is a CFG file?

CFG file is also known as the **"Wesnoth Markup Language" (WML)**. It is a custom markup language used primarily in the game "Battle for Wesnoth", which is a turn-based strategy game. WML is used to define and customize various aspects of the game, including scenarios, campaigns, units, and more. It is a way for modders and developers to create content for the game.

It is written in a format that resembles a combination of XML and simple scripting. Here is overview of some common elements and structures you might find in a WML file:

1.  **Tags:** WML uses tags to define different elements in the game. Tags are enclosed in angle brackets. For example:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    
2.  **Attributes:** Within tags, you can define attributes to specify properties or values associated with the element. In the example above, "type" and "hitpoints" are attributes.
    
3.  **Arrays and Arrays of Arrays:** You can create arrays of data and even arrays of arrays to define lists of units, terrain types, or other game elements.
    
4.  **Conditional Statements:** WML supports conditional statements to control the flow of the game. For example:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    
5.  **Loops:** You can use loops to iterate through lists of items or perform actions repeatedly.
    
6.  **Includes:** You can include other WML files within a main WML file to organize and modularize your content.
    
7.  **Event Handlers:** You can define event handlers to trigger actions when specific events occur in the game.
    

Here is a simplified example of a WML file that defines a custom unit:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## The Battle for Wesnoth

"The Battle for Wesnoth" is a popular and open-source turn-based strategy game. It is available for multiple platforms, including Mac, Windows, Linux, and more. Developed by a dedicated community of volunteers, the game is known for its deep and engaging gameplay, as well as its rich fantasy world.

Key features of "The Battle for Wesnoth" include:

1.  **Fantasy Setting:** The game is set in a fantasy world with various races, including humans, elves, dwarves, orcs, and more. The game's lore and storytelling are an integral part of its appeal.
    
2.  **Turn-Based Strategy:** Gameplay is turn-based, where players take their time to plan and execute their moves on hexagonal grids. It combines tactical combat with strategic decision-making.
    
3.  **Campaigns:** The game offers a wide range of single-player campaigns, each with its own storyline, characters, and challenges. Players can explore different narratives and scenarios.
    
4.  **Multiplayer:** "Wesnoth" supports online multiplayer, allowing players to compete against each other in strategic battles. Multiplayer modes include cooperative play and competitive matches.

## How to open CFG file?

CFG files, which are commonly associated with the Wesnoth Markup Language (WML) used in "The Battle for Wesnoth" game, can be easily edited using any standard text editor. These files contain human-readable code written in WML, which defines various aspects of the game, including scenarios, units, and campaigns.

While you can use any text editor to modify CFG files, some advanced text editors like Emacs and Vi have WML syntax highlighting plugins available. These plugins provide helpful color-coding and formatting to make it easier for users to distinguish different elements and structures within the WML code. 

Programs that open or reference CFG files include

- The Battle for Wesnoth (Free) for (Windows, MAC, Linux)
- Microsoft Notepad

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

## References
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)