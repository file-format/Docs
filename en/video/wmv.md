{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "WMV File Format",
  "description":"Learn about WMV file format and APIs that can create and open WMV files.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2019-09-16"
}

## What is a WMV file?

The Advanced Systems Format (ASF) is a digital multimedia container designed primarily for storing and transmitting media streams. Microsoft Windows Media Video (WMV) is the compressed video format and Microsoft Windows Media Audio (WMA) is the compressed audio format along with additional metadata in the ASF container developed by Microsoft. Once the wmv or wma files are encoded with Windows Media Video and Windows Media Audio codecs then they are represented with .ASF extension. WMV compresses large files for better transmission rate over a network while maintaining the quality of the video. WMV is specifically designed to run on all Windows devices. After the standardization by Society of Motion Picture and Television Engineer (SMPTE), WMV is now considered to be an open standard format.

## History ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Improvements were added in further two versions i.e. WMV8 and 9. Microsoft submitted 9^^th^^ version of WMV to SMPTE for standardization in 2003 which was eventually standardized in 2006 as SMPTE 421M also known as VC-1. The idea behind the WMV was to develop a media format which could be supported by all the Microsoft supported hardware and software. Furthermore, another major purpose was to transmit video streams over the internet in an optimal scenario. After the standardization from SMPTE, WMV also became a video format for Blu-ray discs.

## File Format Specifications

### Container

Generally WMV is packed into ASF container but in addition Matroska or AVI container can also support it with extensions of .mkv and .avi respectively.

### Windows Media Video 9

Though there are various audio and video codecs available in Windows Media Video 9 series for authoring and playback of digital media, but WMV-9 codec is the latest and best video codec as it can achieve the optimum compression from very low bit rates i.e. 160 x 120 at 10 Kbps to 1920 x 1080 at 4-8 Mbps for a variety of HD videos.

### Structure of Codec

WMV-9 has 8 bit 4:2:0 internal color format. Like all other popular video compression standards MPEG-1 and H.261, WMV-9 uses a block-based motion compensation and spatial transform scheme. In general, we can say that these standards perform block by block motion compensation from the previous reconstructed frame with the help of a 2-D quantity called the motion vector (MV) to signal spatial displacement. The current block is formed with the help of predicting the values from the same size previous reconstructed frame which is displaced from the current position by the motion vector. Eventually, the residual error is calculated as the difference between the motion-compensated predicted block and the actual block. This residual error is transformed using a linear energy-compacting transform then quantized and entropy coded.

Quantized transform coefficients are entropy decoded, dequantized and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Rest of the section will discuss the new improvements in WMV-9 which differentiate it from the rest of the video coding solutions like MPEG standards. WMV-9 has intra (I), predicted (P) and bi-directionally predicted (B) frames. Intra frames are those which are coded independently and have no dependence on other frames. Predicted frames are frames that depend on one frame in the past. Decoding of a predicted frame can occur only after all reference frames prior to the current frame starting from the most-recent (I) frame have been decoded. B frames are frames that have two references—one in the temporal past and one in the temporal future. B frames are transmitted subsequent to their references, which mean that B frames are sent out of order to ensure that their references are available at the time of decoding. B frames in WMV-9 are not used as a reference for subsequent frames. This places B frames outside of the decoding loop, allowing shortcuts to be taken during the decoding of B frames without drift or long-term visual artifacts. The above definition of I, P and B frames holds for both progressive and interlaced sequences.

The performance of video codecs is compared to their rate-distortion (R-D) plot. It’s a 2-D curve which shows the distortion produced by the compression at a certain bitrate.

WMV-9 has addressed this problem with the introduction of a variety of techniques listed below:

1. Adaptive block size transform

2. Limited precision transform-set

3. Motion compensation

4. Quantization and dequantization

5. Advanced entropy coding

6. Loop filtering

7. Advanced B frame coding

8. Interlace coding

9. Overlap smoothing

10. Low-rate tools

11. Fading compensation

## References ##

* [https://bytescout.com/blog/2014/10/windows-media-video-format.html](https://bytescout.com/blog/2014/10/windows-media-video-format.html)
* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)
* [http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf](http://citeseerx.ist.psu.edu/viewdoc/download?doi#10.1.1.101.488&rep#rep1&type#pdf)
