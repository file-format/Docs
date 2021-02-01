{
  "date" : "2019-12-13",
  "keywords" : [ "WAV", "file", "extension", "format", "audio interchange file format", "music" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about WAV file format and APIs that can create and open WAV files.",
  "title" : "WAV - Waveform Audio File Format",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2019-12-13"
}

## What is a WAV file?

WAV, known for WAVE (Waveform Audio File Format), is a subset of Microsoft's Resource Interchange File Format (RIFF) specification for storing digital audio files. The format doesn't apply any compression to the bitstream and stores the audio recordings with different sampling rates and bitrates. It has been and is one of the standard format for audio CDs. Wave files are larger in size as compared to new audio file formats such as [MP3](/audio/mp3/) which uses lossy compression to reduce the file size while maintaining the same audio quality. However, WAV files can be compressed using Audio Compression Manager (ACM) codecs. There are several APIs and applications available that can convert WAV files to other popular audio file formats.

## WAV File Format ##

The WAVE file format, being a subset of Microsoft's RIFF specification, starts with a file header followed by a sequence of data chunks. A WAVE file has a single "WAVE" chunk which consists of two sub-chunks:

* a "fmt" chunk - specifies the data format
* a "data" chunk - contains the actual sample data

### WAV File Header ###

The header of a WAV (RIFF) file is 44 bytes long and has the following format:


|Positions|Sample Value|Description
---|---|---|
|1 - 4|"RIFF"|Marks the file as a riff file. Characters are each 1 byte long.
|5 - 8|File size (integer)|Size of the overall file - 8 bytes, in bytes (32-bit integer). Typically, you'd fill this in after creation.
|9 -12|"WAVE"|File Type Header. For our purposes, it always equals "WAVE".
|13-16|"fmt "|Format chunk marker. Includes trailing null
|17-20|16|Length of format data as listed above
|21-22|1|Type of format (1 is PCM) - 2 byte integer
|23-24|2|Number of Channels - 2 byte integer
|25-28|44100|Sample Rate - 32 byte integer. Common values are 44100 (CD), 48000 (DAT). Sample Rate = Number of Samples per second, or Hertz.
|29-32|176400|(Sample Rate * BitsPerSample * Channels) / 8.
|33-34|4|(BitsPerSample * Channels) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Bits per sample
|37-40|"data"|"data" chunk header. Marks the beginning of the data section.
|41-44|File size (data)|Size of the data section.
|Sample values are given above for a 16-bit stereo source.

## References ##

* [WAV - By Wikipedia](https://en.wikipedia.org/wiki/WAV)
