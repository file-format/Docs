{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MK3D File Format",
  "keywords" : [ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", StereoMode ],
  "description":"Learn about MK3D file format for stereoscopic 3d videos created by Matroska and APIs that can create and open MK3D files.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-23-02"
}

## What is an MK3D file? ##

The MK3D files belong to the Matroska video formats family. These files are actually **stereoscopic 3d** videos created using Matroska 3D format. The MKV file Container uses a StereoMode field's value to define the type of stereoscopic 3D video stuff. A StereoMode value is also available to display the old stereo 3D videos by separating cyan and red colours (AnaGlyph) 

## Technical Details ##
The 3D videos can be compressed in the following two ways:

- Seperate track for each eye.
- Combine each eye track into a single track.

The MKV file container support both of these.

For the single track videos which are easier with the 3D material inside it, you have to set the **StereoMode** field which decides either the planes are assembled in the mono or left right combined track. You can use one of the following StereoMode field values:

|Value	| Description |
|---|---|
|0| mono|
|1| side by side (left eye is first)|
|2| top-bottom (right eye is first)|
|3| top-bottom (left eye is first)|
|4| checkboard (right is first)|
|5| checkboard (left is first)|
|6| row interleaved (right is first)|
|7| row interleaved (left is first)|
|8| column interleaved (right is first)|
|9| column interleaved (left is first)|
|10| anaglyph (cyan/red)|
|11| side by side (right eye is first)|
|12| anaglyph (green/magenta)|
|13| both eyes laced in one Block (left eye is first) (field sequential mode)|
|14| both eyes laced in one Block (right eye is first) (field sequential mode)|

For the multiple tracks the MKV container needs to decide the functionlaity of each track separately. The **TrackOperation** with **TrackCombinePlanes** are used to do the job.


## References ##

- [Matroska Specification Notes]https://www.matroska.org/technical/notes.html)
- [MKV File Container Support for Stereo 3D Video and the MK3D Files](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

