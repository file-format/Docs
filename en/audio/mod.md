{
  "date" : "2021-08-04",
  "keywords" : [ "mod", "mp3", "file", "extension", "format", "what is mod file format", "music", "mod file format", "mod vs MP3", "mod file format specification"],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MOD file format and APIs that can create, convert and open MOD files.",
  "title" : "MOD - Music Module File",
  "linktitle" : "MOD",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-08-04"
}

## What is an MOD file?
A file with .mod extension is a music module file created by using the standard music module format, which is based on the **Amiga module format** developed by Karsten Obarski and released with the **Ultimate Soundtracker** software for the Commodore Amiga system. Similar to a [MIDI](/audio/midi) file, it consists of note patterns and sound samples, representing different instruments that are played back according to the notes. MOD files are particularly used in video games as background music and in the **demoscene** computer art subculture.
## MOD file format
The MOD is a computer file format used its basic function is to represent music, and it was the first module file format. MOD files use the .mod file extension, except on the **Amiga** which reads a file's header to determine filetype, so it doesn't rely on filename extensions. A MOD file consists of a set of various instruments in the form of samples, a number of patterns specifying how and when the samples are to be played, and a list of what patterns to play in what order.
### Specification
A MOD file pattern is actually designed in a sequencer user interface as a table with one column per channel, So this table has four columns (one for each Amiga hardware channel. Each column has 64 rows).

A cell in the table can cause one of the following actions to happen on its column's channel when its row's time is reached:

- Start an instrument playing a new note in this channel at a given volume, possibly with a special effect applied on it
- Change the volume or special effect being applied to the current note
- Change pattern flow; jump to a specific song or pattern position or loop inside a pattern
- Do nothing; any existing note playing in this channel will continue to play

An instrument is a single sample along with an optional specification of which portion of the sample can be repeated to hold a solid note.
### Timing
The minimum time frame was 0.02 seconds in the original MOD file, or a "vertical blanking" (VSync) interval, because the original software used the VSync timing of the monitor running at 50 Hz (for PAL) or 60 Hz (for NTSC) for timing.

## References

* [MOD (file format) - By Wikipedia](https://en.wikipedia.org/wiki/MOD_(file_format))

