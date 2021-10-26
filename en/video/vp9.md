{
  "date" : "2021-03-12",
  "keywords" : [ "VP9", "File", "Extension", "File Format", "Video Format", "TrueMotion Video", "VPX", "On2 Technologies"],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VP9 - TrueMotion Video File",
  "description":"Learn about VP9 file format and APIs that can create and open VP9 files.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-03-27"
}

## What is a VP9 file?

Google has developed the VP9 codec as a royalty-free, open-source video coding standard as the successor to VP8. It was originally designed to compress the ultra HD content on YouTube because it expands and enhances the coding efficiency of its predecessor. If we talk about the original VPX codecs, they came from On2 Technologies, which was assimilated by Google in 2010. Google later open-sourced the codec. VP8 and VP9 both formats are available under a free BSD license that permits operators to organize encode or decode proficiencies in both exclusive software and open-source software without revealing their source code.

## Technical Features of VP9

 *	VP9 provisions a maximum resolution of 8192x4352 at up to 120 fps and multiple color spaces, with Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240, and sRGB
 *	The full range of web and mobile use cases from low bitrate compression to high-quality ultra-HD, with additional support for 10/12-bit encoding and HDR are fully supported by this format
 *	It can decrease video bit rates by as much as 50% in comparison with others
 *	It is braced for adaptive streaming and is used by YouTube and other well-known web video providers
 *	Chrome, Opera, Edge, Firefox, and Android devices, as well as millions of smart TVs, support the decoding of this codec
 *	The video resolutions greater than 1080p are modified through VP9 and allows lossless compression
 *	Different color spaces like Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240, and sRGB are supported by VP9
 *	HDR video using Hybrid Log-Gamma and Perceptual Quantizer can also be supported by VP9


## Brief History

 *  VP9 video codec development has started in 2011, and its decoder was added to the Chromium web browser in December 2012
 *  Its first Google Chrome web browser version was released in February 2013 and released decoding at that time
 *  Google released Chrome 29.0.1547 with VP9 final support in August 2013
 *  In October of 2013, an instinctive VP9 decoder was added to FFmpeg
 *  Mozilla has added VP9 sustenance to Firefox in December of 2013 in version 2 that was then released on March 18, 2014
 
## Working of VP9

Usually, the 4K video upsurges picture quality by making specific pixels smaller, the VP9 codec and HEVC make them bigger to scale back the bitrate and file size. While this might seem contradictory, the encoding engine takes the larger pixels and changes them into better resolution productivity. Source video, entailing of video frames, is encoded or compressed to make a compressed video bitstream. Each separate frame is first divided into blocks of pixels. The blocks are then scrutinized for three-dimensional dismissals and sequential connections between frames are evaluated to take advantage of areas that can’t be changed. These are encoded via motion vectors that ensure the qualities of the given block on the next frame. The residual information is encoded using an effectual binary compression.

## References

 * [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google's%20video%20platform%20YouTube)
 * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
 * [Coconut](https://www.coconut.co/)
