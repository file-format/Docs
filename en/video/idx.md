{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "IDX - High Efficiency Video Codec",
  "description":"Learn about IDX file format and APIs that can create and open IDX files.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2022-07-12"
}

## What is an IDX file?

An IDX file is a subtitles index file that points to the list of metadata information for subtitles inside a .sub (VobSub Subtitles) file. It is created and used by the VobSub software application that lets users extract subtitles from DVDs and dump in a SUB file. IDX files contain timestamps and byte offsets used to point to every single subtitle. VobSub always creates an IDX file along with the corresponding SUB file.

## IDX File Format - More Information

IDX files are generated and saved as plain text files that can be opened in any text editor. An IDX file contains information that is read by the media players to read parameters such as the color of the subtitle text to display on screen, position of subtitle text on screen.

### IDX Subtitle Settings

A typical IDX file stores this metadata information at the start of the file. Subtitle settings begin with a **#**. Timestamps and image references are added after all these subtitle settings and start with **timestamp:**.

## IDX File Format Example

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## How to use IDX file?

If you have got the Sub and IDX files for a movie, you can play back these subtitles along with the movie for which these are created. Many applications such as VLC, GOM Player, PotPlayer, or PowerDVD have the capability to load these SUB and IDX files, and play these alongside the movie. Software applications can also embed SUB and IDX subtitle files in [.mkv](/video/mkv/) files.

## References

 * [VobSub](https://www.videohelp.com/software/VobSub)
 * [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)
