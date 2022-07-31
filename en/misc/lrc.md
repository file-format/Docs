{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LRC File Format - What is an LRC file?",
  "description":"Learn about the LRC Lyric file and APIs that can create and open LRC files.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
    }
  },
  "lastmod" : "2022-01-26"
}

## What is an LRC file?

An LRC file is a text based lyrics file that contains the lyrics of an audio song. When the audio song is played with a music player or audio player software on a computer, the LRC file is read in parallel and displayed with time. LRC files contain cue points for displaying of lyrics when the song is playing. In general, the LRC files have the same name as the corresponding audio file such as audio.mp3 and audio.lrc. LRC fles are similar to subtitle files such as [SRT](/video/srt/).

## LRC File Format - More Information

LRC lyric format files are saved as plain text files and can be opened and edited in a text file. The contents of an LRC file contains color information for display of lyrics text.

## LRC Formats

There are multiple formats of LRC files that have been developed over time. These

### Simple LRC Format

The Line Time Tags are in the format [mm:ss.xx] where mm is minutes, ss is seconds and xx is hundredths of a second.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
[mm:ss.xx]last lyrics line
```

### Simple Format Extended

It includes The ability to change and specify the gender of the lyrics by using M: Male, F: Female, D: Duet.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Enhanced LRC format

The enhanced LRC format is an extended version of the Simple LRC format. It adds a Word Time Tag in the format <mm:ss.xx> at the end of the previous word.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## References

* [LRC Lyrics File Format - Wikipedia](https://en.wikipedia.org/wiki/LRC_(file_format))
