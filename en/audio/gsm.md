{
  "date" : "2021-08-05",
  "keywords" : [ "gsm", "file", "extension", "format", "Audio", "Global System for Mobile Audio", "gsm extension", "gsm files"],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about GSM file format and APIs that can create and open GSM files.",
  "title" : "GSM - Global System for Mobile Audio File Format",
  "linktitle" : "GSM",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-08-05"
}

## What is a GSM file? ##

GSM is a file extension that is associated with Global System for Mobile Audio Format Files. Files containing GSM extensions can be opened on Linux, Windows, and Mac OS platforms. The GSM file format belongs to the audio files category.

A GSM file is encoded with a lossy CBR (Constant bitrate) sound compression codec. The sample rate in a GSM audio file is 8000 samples/second whereas the data rate is around 13 kbps. The bitrate within the GSM files ensures quality during voice recording. Moreover, the GSM file format is also known as the global standard format to be used in mobile phones and WAV files can also be easily encoded using a GSM file format. Any issues with a GSM file can be easily resolved by the user himself without going to an expert. Users can also convert GSM files into [MP3](/audio/mp3/) and [MP4](/audio/mp4/) formats.

## Brief History ##

GSM is an audio file format that was created for internet telephony in Europe. It was developed by European Telecommunications Standard Institute (ETSI) to be used as a 2G digital cellular used in mobile phones and tablets. Today it is used to store recordings of telephone conversations and voice messages.

## GSM File Format Specifications ##

GSM work on a structured network which consists of the following sections:

**Modulation**: It is a process of transforming input data into a format that can easily be transmitted. The transmitted data is demodulated at the receiving end
**Transmission rate**: GSM is a digital system that has an over the bit rate of 270 kbps
**Uplink Frequency Range**: 933-960 MHz
**Downlink Frequency Range**: 890 – 915 MHz
**Channel Spacing**: It means the spacing between adjacent barriers which should be about 200 kHz
**Duplex Distance**: It is the space between uplink and downlink frequencies which should be 80 MHz 
**Speech Coding**: GSM uses Linear Predictive Coding (LPC). LPC compresses the bit rate. When the audio signal passes through a filter and mimics the vocal tract. GSM encode speech at 13kbps

| Audio compression format | Algorithm | Sample rate | Bit rate transform | Latency  | CBR | VBR | Stereo | Multichannel |
| ------------------------ | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
|  |
| GSM-HR  				   | VSELP     | 8 kHz       | 5.6 kbit/s         | 25 ms    | Yes | No  | No     | No           |
| GSM-FR                   | RPE-LTP   | 8 kHz       | 13 kbit/s          | 20–30 ms | Yes | No  | No     | No           |
| GSM-EFR 				   | ACELP     | 8 kHz       | 12.2 kbit/s        | 20–30 ms | Yes | No  | No     | No           |


## References ##

* [GSM - By Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)
