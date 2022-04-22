{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CR2 File Format - Canon Raw 2 Image File",
  "description":"Learn about CR2 file format and APIs that can create and open CR2 files.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
    }
  },
  "lastmod" : "2022-03-26"
}

## What is a CR2 file?

A CR2 (Camera RAW 2) file is a RAW image file created by Canon digital cameras. It stores the original non-processes lossless image data captured by the camera. CR2 file format was developed by Canon for its digital cameras and can record high-qulaity images of up to 14 bits of RGB. This produces high quality images with enough room of post processing. CR2 image format has been used by Canon in their 350D, 20D and 1D camera models. CR2 files are RAW files and contain additional metadata information such as camera information, lens info, bracketing information, white balance and other settings.

## CR2 File Format

CR2 files are stored to camera memory card as binary files in Canon proprietary file format. CR2 file format replaced the initially used CRW file format and was replaced itself by the Canon RAW 3 file format later on. CR2 file format is based on the [TIFF](/image/tiff/) specifications which has 4 Image File Directories (IFDs).

|Offset	|Content	|Comment|
---|---|---|
|0x0000	|Header	|contains the byte ordering, the version and the offset to the RAW picture|
|computed	|IFD#0	|this part contains the Exif section, which contains the Makernotes section.
Information about picture#0|
|computed	|picture#0	|small version of the picture (one fourth the size of the original), compressed in Jpeg|
|computed	|IFD#1	|Information about picture#1.|
|computed	|picture#1	|small version of the picture, compressed in Jpeg|
|computed	|IFD#2	|Information about picture#2.|
|computed	|picture#2	|small version of the picture, not compressed|
|in header|	IFD#3|	Information about picture#3, the full dimension RAW image|
|computed	|picture#3	|RAW image data, lossless compressed in Jpeg (not RGB data!)|

## Advantage of CR2 File Format

Storing pictures in RAW format allows a lot of post-processing to the photograph such as adjustment to the White Balance. This is far more difficult and with a big quality loss with other image file formats such as [JPEG](/image/jpeg/).

## Is CR2 better than JPEG?

CR2 files are raw files without any loss of data and, hence, no loss of quality. JPEG on the other is lossy image file format as it loses some data to reduce the file. Thus, the CR2 files are high in quality and more suitable for retouching and enhancements.

## References

 * [CR2 File Format](http://lclevy.free.fr/cr2/)
