{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about OSZ file format and APIs that can create and open OSZ files.",
  "title" : "OSZ File - osu! Beatmap File Format",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
    }
  },
  "lastmod" : "2021-09-08"
}

## What is an OSZ file?

An OSZ file is a compressed file format used by the rhythm game osu! to store beatmap data. Beatmaps are essentially levels for the game, and they include information such as the song, the beat timing, and the placement of hit objects on the game screen. OSZ files allow for easy distribution of beatmaps and are typically downloaded from the internet and imported into the game. OSU! also has the [OSR](/game/osr/) file format that is a game replay file and can be replayed by game players.

**MIME Type of OSR File Format:** x-osu-replay

## OSZ File Format

The internal file format details of OSZ file types are not available publicly. It contains [ZIP](/compression/zip/)-compressed data that has information to play the music, show graphics, and display players about the events when they must interact with the game.

## How to Create OSZ File?

OSU! has detailed instructions for [creating OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files) and OSK files.  The following steps can be used to create an OSZ file using OSU!.

1. Open a beatmap via the editor.
1. From the top menu, select File > Export package....
1. The .osz archive will be placed in the Exports folder inside the osu! folder.

## References

* [OSU! Rhythm Game](https://osu.ppy.sh/home)
