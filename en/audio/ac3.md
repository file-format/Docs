{
  "date" : "2019-12-13",
  "keywords" : [ "AC3", "file", "extension", "format", "Audio Coding", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about AC3 file format and APIs that can create and open AC3 files.",
  "title" : "AC3 - Audio Codec 3 File",
  "linktitle" : "AC3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2019-12-13"
}

## What is an AC3 file?

A file with a .ac3 extension is an Audio Codec 3 file, introduced by Dolby Laboratories. It is an audio format that can contain up to six channels of audio output. The format had been originally used for audio but is now also used for other applications such as HDTV broadcast, DVDs, Blue-ray discs and game consoles. Applications that can open AC3 files include Apple QuickTime player, Microsoft Windows Media Player, Winamp, MPlayer and other similar.

## AC3 File Format

AC3 files are binary in nature and based on the Modified Discrete Cosine Transform (MDCT) which is a lossy compression algorithm. Dolby Laboratories used the MDCT algorithm along with perceptual coding principles to develop the AC-3 audio format. This led to the release of the AC-3 format as the Dolby Digital standard in 1991. The format supports the provision of five channels for normal-range speakders (20 Hz - 20,000 Hz) and one channel (20 Hz - 120 Hz) for the subwoofer driven low-frequency effects. AC3 supports sample rates up to 48 kHz.

### Technical Details

The Dolby Digital technology uses a very efficient way to compress the size of multichannel audio files without impairing the sound quality. This compression leads to smaller file size which makes it easy to distribute the sound files. Using Dolby Digital, it is possible to include a full 5.1-channel audio mix on a film print or a DVD.

#### Specifications
The Dolby Digital specifications are as follow.

|Field|Specification|
---|---|
|Channels	|1.0 to 5.1, discrete|
|DVD data rate, 5.1-channel audio| 384 or 448 kbps|
|Blu-ray Disc data rate, 5.1-channel audio|640 kbps|
|Supports Dolby metadata |Yes|
|Connections |S/PDIF, HDMI®, IEEE 1394|
|Mixing/streaming capabilities|Yes|

#### MetaData Parameters

|Metadata Paramter| Informational|Control|
---|---|---|
|Dialogue level| |Yes|
|Channel mode| | Yes|
|LFE channel| | Yes|
|Bitstream mode| Yes| Yes|
|Line mode compression| | Yes|
|RF mode compression| | Yes|
|RF overmodulation protection| | Yes|
|Center downmix level| | Yes|
|Surround downmix level| | Yes|
|Dolby Surround mode| |Yes|
|Audio production information| Yes||
|Mix level| Yes||
|Room type| Yes||
|Copyright bit| Yes||
|Original bitstream| Yes||
|Preferred stereo downmix| |Yes|
|Lt/Rt Center downmix level||Yes|
|Lt/Rt Surround downmix level||Yes|
|Lo/Ro Center downmix level||Yes|
|Lo/Ro Surround downmix level||Yes|
|Dolby Digital Surround EX™ mode||Yes|
|A/D converter type|Yes||
|DC filter||Yes|
|Lowpass filter||Yes|
|LFE lowpass filter||Yes|
|Surround 3 dB attenuation||Yes|
|Surround phase shift||Yes|

## References

* [AC3 - By Wikiepedia](https://en.wikipedia.org/wiki/Dolby_Digital)
* [Dolby Digital 5.1](https://professional.dolby.com/tv/dolby-digital)
