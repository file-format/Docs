{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about OSU file format and APIs that can create and open OSU files.",
  "title" : "OSU File - Osu! Script File Format",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
    }
  },
  "lastmod" : "2023-01-18"
}

## What is an OSU file?

An OSU file is a game script written for osu! rhythm game. It contains information about a beatmap used in the game such as the difficulty level, the song to be played, and the timings of the hit objects to which the player has to sync with the music. It lets rhythm game players to develop custom challenges and share with the game community.

**MIME Type of OSR File Format:** x-osu-beatmap

## OSU File Format

OSU files are saved as plain text files to disc and its structure is very clearly defined in the [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) by osu!.

### Sections in OSU File

A typical OSU file has the follwoing sections.

|Section	|Description	|Content type|
---|---|---|
|[General]|	General information about the beatmap|	key: value pairs|
|[Editor]|	Saved settings for the beatmap editor|	key: value pairs|
|[Metadata]	|Information used to identify the beatmap|	key:value pairs|
|[Difficulty]	|Difficulty settings|	key:value pairs|
|[Events]|	Beatmap and storyboard graphic events|	Comma-separated lists|
|[TimingPoints]|	Timing and control points|	Comma-separated lists|
|[Colours]|	Combo and skin colours|	key : value pairs|
|[HitObjects]|	Hit objects|	Comma-separated lists|

## References

* [OSU! Rhythm Game](https://osu.ppy.sh/home)
* [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)
