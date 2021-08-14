{
  "date" : "2021-08-09",
  "keywords" : [ "mmf", "file", "extension", "format", "audio", "smaf", "mmf extension", "mmf files", "mobile music file", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about MMF file format and APIs that can create and open MMF files.",
  "title" : "MMF - Mobile Music File Format",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
    }
  },
  "lastmod" : "2021-08-09"
}

## What is an MMF file? ##

MMF is a file extension associated with a SMAF file. The MMF stands for Mobile Music File whereas the SMAF stands for synthetic-music Mobile Application Format. The MMF files within a smartphone contain system ringtones, sound and can also contain graphics and text display. The MMF further contains three types of instrument parameters including FM, PCM, and Stream PCM. These file formats are compatible with the Windows system platform. The MMF files are categorized as data files. Usually, Microsoft Mail supports MMF files. The file having MMF suffix can be copied to any mobile device or system platform. 
Moreover, these files are much smaller in size compared to standard MIDI format files. [WAV](/audio/wav/) and [MID](/audio/mid/) files can be converted to MMF format which can be then shared and distributed as audio content. These files can be received via email directly to phones and PC.


## Brief History ##

Yamaha developed SMAF tools as sound files so that smartphones can store a greater number of unique ringtones. Yamaha introduced SMAF with the production of their MA-1, MA-2, MA-3, MA-5, and MA-7 LSI sound chips. All these formats become quite familiar among mobile phones in the East Asian Market during early 2000.

On the international level, the MMF format was authorized by Samsung. With the help of MMF format, Samsung was able to design a wide range of polyphonic ringtones to be used in Samsung smartphones.

Yamaha wanted to make the format even more popular and so on the official Yamaha SMAF files, it published more tools compatible with this format. With this users can now easily play MMF files on their computers.


## MMF File Format Specifications ##

MMF files are categorized into data sections. A prefixed structure around an 8-byte is used to describe each segment.
The 4-byte label includes CNTI, OPDA, MSTR, MTR, and ATR. Data size plus 8 bytes is the chunk size; the whole file size is calculated by summing all chunk sizes. If a file has not been damaged, the summed file size should be the same as a primary header size.

### Header ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Here is an example of MMF file:

![](../mmf.png)

## References ##

* [MMF - By Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)
