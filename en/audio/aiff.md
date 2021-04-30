{
  "date" : "2021-04-26",
  "keywords" : [ "aiff", "file", "extension", "format", "audio interchange file format", "music", "aiff file format", "aiff to mp3", "aiff vs wav", "convert aiff to mp3" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about AIFF file format and APIs that can create, convert and open AIFF files.",
  "title" : "AIFF - Audio Interchange File Format",
  "linktitle" : "AIFF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-04-26"
}

## What is an AIFF file?
The AIFF (Audio Interchange File Format) is an uncompressed audio file format developed by Apple in 1998, but is based on **EA IFF 85** (Standard for Interchange Format Files developed by Electronic Arts), a wrapper format used on Amiga systems. This file format comes up with a standard for storing sampled sounds. The format is good enough in flexibility, and enables the storage of monaural or multichannel sampled sounds at various sample rates and sample widths. Since the AIFF files are uncompressed, this thing making them bigger in size than other lossy formats such as [MP3](https://docs.fileformat.com/audio/mp3/). These files consist of 2 channels of uncompressed stereo audio with 16 bits sample size, recorded at 44.1 khz. Because of high quality of audio, a 5 minute audio can take upto 50MB disk space which is similar to [WAV](https://docs.fileformat.com/audio/wav/) file format.



## AIFF vs WAV
The AIFF and WAV are the almost same in term of quality. Both of them use same PCM (pulse-code modulation) encoding, which makes them larger in size as compared to other lossy formats, such as, [MP3](https://docs.fileformat.com/audio/mp3/), [M4A](). Some of the general differences are written in the table below:

|AIFF|WAV|
---|---|
|Being used mostly for MAC|Mostly used for PCs|
|Allows for metadeta| Doesn't allow for metadeta|

## File Structure
The **EA IFF 85** sets out an overall structure for storing data in files. An **EA IFF 85** file consists of a number of chunks of data. A chunk is buliding block of AIFF file consists of some header information followed by data:
{{< figure src="../chunk.png" alt="AIFF Chunk" >}}

An AIFF file is a collection of a number of different types of chunks. There are two general types of chunks which are important to form an AIFF file chunk:
- **Common Chunk**: Contains important parameters describing the sampled sound, such as it's length and sample rate.
- **Sound Data Chunk**: Contains the actual audio samples.
 There are many other optional chunks that list instrument parameters, define markers, store applicationspecific information, etc.
 
### Local Chunk Types

The chunk types to form AIFF are given in the table below:

|Chunk Type| Description|
---|---|
|Common Chunk|The Common Chunk describes fundamental parameters of the sampled sound|
|Sound Data Chunk|The Sound Data Chunk contains the actual sample frames|
|Marker Chunk|The Marker Chunk contains markers that point to positions in the sound data|
|Instrument Chunk|The Instrument Chunk defines basic parameters that an instrument, such as a sampler, could use to play back the sound data|
|MIDI Data Chunk|The MIDI Data Chunk can be used to store MIDI data|
|Audio Recording Chunk|The Audio Recording Chunk contains information pertinent to audio recording devices|
|Application Specific Chunk|The Application Specific Chunk can be used for any purposes whatsoever by manufacturers of applications|
|Comments Chunk|The Comments Chunk is used to store comments in the FORM AIFF|
|Text Chunks - Name, Author, Copyright, Annotation| All are text chunks|







## References ##

* [Audio Interchange File Format - By Wikipedia](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)
