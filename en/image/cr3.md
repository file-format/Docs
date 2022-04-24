{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CR3 File Format - Canon Raw 3 Image File",
  "description":"Learn about CR3 file format and APIs that can create and open CR3 files.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
    }
  },
  "lastmod" : "2022-03-26"
}

## What is a CR3 file?

A CR3 file is a Canon RAW image file format that is created by selected Canon digital cameras. It was introduced by Canon to replace the CR2 file format and is used by some of the Canon digital devices. CR3 files store the original non-processed lossless image data captured by the camera. The use of these raw images provide high quality images and allow plenty of room for editing to photographers. In addition to main image data, CR3 files also store metadata information about the image.

## CR3 File Format

CR3 files are stored to disc as binary file in the ISO Base Media File Format (ISO/IEC 14496-12) and also includes custom [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid). It also includes the [Canon 'crx' codec](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp) that is a mix of JPEG-LS (Rice-Golomb + RLE coding) and JPEG-2000 (LeGall 5/3 DWT + quantification).

## CR3 Custom Tags

CR3 files contain custom tags for different purposes. Some of these tags are as follow.

|Tag ID|	Tag Name|	Writable	|Values / Notes|
---|---|---|---|
|'CCTP'	|CanonCCTP|	-	|--> Canon CCTP Tags|
|'CMT1'	|IFD0|	-	|--> EXIF Tags|
|'CMT2'	|ExifIFD|	-	|--> EXIF Tags|
|'CMT3'	|MakerNoteCanon|	-	|--> Canon Tags|
|'CMT4'	|GPSInfo|	-	|--> GPS Tags|
|'CNCV'	|CompressorVersion|	no| |	 
|'CNOP'	|CanonCNOP|	-	|--> Canon CNOP Tags|
|'CNTH'	|CanonCNTH|	-	|--> Canon CNTH Tags|
|'THMB'	|ThumbnailImage|	no| |	 

## References

 * [CR2 File Format](http://lclevy.free.fr/cr2/)
 * [Canon tags](https://exiftool.org/TagNames/Canon.html#uuid)
