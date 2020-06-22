{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "PSB",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

Adobe photoshop saves files in two formats. Files having 30,000 by 30,000 pixels in size are saved with PSD extension and files larger than PSD upto 300,000 by 300,000 pixels are saved with PSB extension known as “Photoshop Big”. More specifically, PSB files can be as large as 4 EB (over 4.2 billion GB) with images that have a height and width of up to 300,000 pixels. PSDs, on the other hand, can be at maximum upto 2 GB and image dimensions of 30,000 pixels. PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.

Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/EPS/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## File Format Information ##

Photoshop file format is divided into five major portions with many length markers to move between sections.

|File format
---|
|File Header
|Colour Mode Data
| Image Resources
|Layer and Mask Information
|(((
Image Data
)))

### File Header ###

File header has fixed length of 26 bytes and contains the basic properties of the image.

BYTE Signature [4] – Equals to ‘8BPS’.

WORD Version [2] – Version Number, PSD # 1, PSB # 2.

BYTE Reserved [6] – Reserved and always zero.

WORD Channels [2] – Number of colour channels in the image including alpha channels. Its value ranges from 1 to 56.

LONG Rows [4] – Height of the image in pixels, PSD 1-30,000, PSB 1-300,000.

LONG Columns [4] – Width of the image in pixels, PSD 1-30,000, PSB 1-300,000.

WORD Depth [2] – Number of bits per channel. Supported values are 1,8,16 and 32.

WORD Mode [2] – Colour Mode of the file.

#### Mode Description ####


|Mode|Description
---|---|
|0|Bitmap (monochrome)
|1|Gray-scale
|2|Indexed
|3|RGB
|4|CMYK
|7|Multichannel
|8|Duotone (halftone)
|9|Lab

### Colour Mode Data ###

After the file header section the colour mode data section follows. The block starts with a LONG Number which gives the length of the block in bytes. Structure of the colour mode data is as follow:

4 bytes – The length of the following color data.

Variable – Colour Data

If the mode field value in the header section is not Indexed Colour or duotone, length of the block will be 0 and there will be no data after length field.

For Indexed Colour Images, length will be 768 bytes which will contain a 256 colour palette. For duotone, data will contain screen parameters and other related information.

### Image Resources ###

Following the colour mode data section, the third block is the image resource section. First four bytes are a LONG number specifying the length of the block followed by a series of resource blocks. Structure of the image resource block is as follow:

BYTE Type [4] – Signature ‘8BIM’

WORD ID [2] – Image Resource ID. There is a list of Resource IDs which can be seen from the reference link.

BYTE Name [Variable] – Name: Pascal String with even length.        **          **

LONG Size [4] – Actual Size of resource data that follows.

BYTE Data [Variable} – Resource data. It is padded to make the even size.

Some of the resource formats are briefly explained below:

**Grid and Guides Resource Format:** Grid and Guides information is stored in resource block. These resource blocks contain 16 byte grid and guide header followed by 5 byte blocks of guide information.

**Thumbnail Resource Format:** Thumbnail information is stored in image resource block for preview display which consists of 28 byte header and JFIF thumbnail in RGB.

**Colour samplers Resource Format:** Colour samplers information is stored in image resource block with an 8 byte header followed by a variable length block of colour samplers information.

### Layer and Mask Information ###

The forth block is layer and mask information block and contains information about the layers and masks. Layer information is stored first and then mask information.

**Layer Information:** Layer information starts with a LONG value which shows the length of the layer information. After that there is WORD value count which shows the number of layer records to follow.

[8] – length of the layers

[2] – Layer Count

[Variable] – Information about each layer.

[Variable] – Channel image data.**          **

**Mask Information:** Mask structure has the following format:


|Data Structure|Field Name| Description
---|---|---|
|WORD|    Overlay Colour Space|     (Not documented)
|BYTE[8]|    Color Components|     4x2 byte color components
|WORD|    Opacity|     0#transparent, 1#opaque
|BYTE|    Kind|  0#inverted, 1#protected, 128#use stored value
|BYTE|    padding|     set to zero

### Image Data ###

The last section contains the image pixel data. The image data is stored as a series of sequence in planes i.e. first all red data, then all the green data etc. WORD at the start of each line shows the size in bytes related to each scan line.

[2] – Compression method:

[Variable] – Image Data in planar order i.e. RRRR, GGGG, BBBB etc.

Compression Methods:

0 – Raw Image Data

1 – RLE Compressed

2 – Zip without Prediction

3 – Zip with prediction

## Reference ##

* [PSB File Format - By Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)
