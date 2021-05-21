{
  "date" : "2019-12-13",
  "keywords" : [ "MP3", "file", "extension", "format", "Audio", "MPEG" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MP3 file format and APIs that can open and create MP3 files.",
  "title" : "MP3 - Audio File Format",
  "linktitle" : "MP3",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2020-09-04"
}

## What is a MP3 file?

Files with .mp3 extension are digitally encoded file formats for audio files that are formally based on the MPEG-1 Audio Layer III or MPEG-2 Audio Layer III. It was developed by the Moving Picture Experts Group (MPEG) that uses Layer 3 audio compression. Compression achieved by MP3 file format is 1/10th the size of .WAV or .AIF files. The format gives advantages of streaming such audio files over the internet for listening online that was previously not possible due to the large file sizes of audio files. Sound quality of an MP3 audio file can be controlled by parameter settings such as bit rate, sample rate, joint or normal stereo.

## Brief History of MP3 ##

The MP3 format was invented and developed by a German Company, Fraunhofer-Gesellshart. The algorithm has licensed patents for compression technology it uses. Here's a handy timeline of MP3:

• **1987** - The Fraunhofer Institute in Germany began researching high-quality low bit-rate audio coding. It was called the EUREKA project EU147, Digital Audio Broadcasting.

• **January 1988** - The Moving Picture Experts Group, or MPEG, was established.

• **April 1989** - Fraunhofer received a patent in Germany for MP3.

• **1992** - Dieter Seitzer, who helped with the Fraunhofer with its research, integrated his audio coding with MPEG-1.

• **1993** - The MPEG-1 standard was published.

• **1994** - The MPEG-2 standard was developed and then published a year later.

• **Nov. 26, 1996** - The U.S. patent for MP3 was issued.

• **September 1998** - Fraunhofer began enforcing patent rights. Whoever used the MP3 audio coding paid a licensing fee to Fraunhofer.

• **February 1999** - SubPop, a recording company, distributed music under the MP3 format, the first such company to do so.

• **1999** - The first portable MP3 players appear.

## MP3 File Format ##

An MP3 file consists of MP3 frames where each frame consists of a header and a data block. The frames are not independent and cannot usually be extracted at arbitrary frame boundaries. The data blocks of file contains information about the audio in terms of frequencies and amplitudes. The sync word in the header identifies the beginning of a valid frame. This is followed by 3 bits where the frist bit shows that it is an MPEG standard and remaining 2 bits show that layer 3 is used; hence MPEG-1 Audio Layer 3 or MP3. After this, the values will differ, depending on the MP3 file.[ISO](https://en.wikipedia.org/wiki/International_Organization_for_Standardization)/[IEC](https://en.wikipedia.org/wiki/International_Electrotechnical_Commission) 11172-3 defines the range of values for each section of the header along with the specification of the header. Most MP3 files today contain [ID3](https://en.wikipedia.org/wiki/ID3) [metadata](https://en.wikipedia.org/wiki/Metadata), which precedes or follows the MP3 frames, as noted in the diagram. The data stream can contain an optional checksum.

## References ##

* [MP3 - By Wikipedia](https://en.wikipedia.org/wiki/MP3)
