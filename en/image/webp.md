{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "WEBP",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

WebP, introduced by Google, is a modern raster web image file format that is based on lossless and lossy compression. It provides same image quality while considerably reducing the image size. Since most of the web pages use images as effective representation of data, the use of WebP images in web pages results in faster loading of web pages. As per Google, WebP lossless images are 26% smaller in size compared to [PNGs](/image/png/), while WebP lossy images are 25-34% smaller than comparable [JPEG](/image/jpeg/) images. Images are compared based on the Structural Similarity (SSIM) index between WebP and other image file formats. WebP is a sister project of [WebM](https://en.wikipedia.org/wiki/WebM) multimedia container format.

## WebP Features Overview ##

WebP images use the compression process based on the prediction of pixels from their surrounding blocks, resulting in pixels to be used multiple times in a single file. It supports animated images and is expected to support more features in the future. Google has made available the source code [online](https://developers.google.com/speed/webp/download) for its encoder and decoder so as to be used where required.  The WebP image provides support for:

* **Lossy compression:** The lossy compression is based on [VP8](http://en.wikipedia.org/wiki/VP8) key frame encoding. VP8 is a video compression format created by On2 Technologies as a successor to the VP6 and VP7 formats.
* **Lossless compression:** The lossless compression format is developed by the WebP team.
* **Transparency:** 8-bit alpha channel is useful for graphical images. The Alpha channel can be used along with lossy RGB, a feature that's currently not available with any other format.
* **Animation:** It supports true-color animated images.
* **Metadata:** It may have EXIF and XMP metadata (used by cameras, for example).
* **Color Profile:** It may have an embedded ICC profile.

Lossy WebP compression uses predictive coding to encode an image, the same method used by the VP8 video codec to compress keyframes in videos. Predictive coding uses the values in neighboring blocks of pixels to predict the values in a block, and then encodes only the difference.

Lossless WebP compression uses already seen image fragments in order to exactly reconstruct new pixels. It can also use a local palette if no interesting match is found.

## File Format ##

The WebP file format is based on the RIFF (resource interchange file format) document format. The WebP container provides support for over and above features than only containing a single image encoded as a VP8 key frame. The basic element of a RIFF file is a chunk which consists of:


|Field|Description
---|---|
|Chunk FourCC: 32 bits|ASCII four-character code used for chunk identifcation
|Chunk Size: 32 bits (uint32)|The size of the chunk not including this field, the chunk identifier or padding
|Chunk Payload: Chunk Size bytes|The data payload. If Chunk Size is odd, a single padding byte ~-~- that should be 0 ~-~- is added
|ChunkHeader ('ABCD')|Used to describe the FourCC and Chunk Size header of individual chunks, where 'ABCD' is the FourCC for the chunk. This element's size is 8 bytes.

### WebP Header ###

A WebP file header is as follow:

* RIFF Header - 32 bits representing the ASCII characters 'R' 'I' 'F' 'F'
* File Size - 32 bits (uint32) representing the size of the file in bytes starting at offset 8. The maximum value of this field is 2^32 minus 10 bytes and thus the size of the whole file is at most 4GiB minus 2 bytes.
* 'WEBP' - 32 bits representing the ASCII characters 'W' 'E' 'B' 'P'

### Lossy File Format ###

WebP images use the lossy file format if the image is based on lossy encoding and does not require any advanced/extended features such as transparency, animate, alpha, etc. Lossy images are smaller and are supported by the older applications as well.

The WebP file, in this case, consists of:

* 12 bytes WebP file header
* VP8 Chunk

The [VP8 Data Format and Decoding Guide](https://tools.ietf.org/html/rfc6386) illustrates the VP8 bitstream format specifications.

### Lossless File Format ###

This layout is used when the image is based on loseless encoding and there is no need of the advanced features provided by the external format. Older applications may not be able to read such files though.

The WebP file, in this case, consists of:

* 12 bytes WebP file header
* VP8L Chunk

## References ##

* [WebP Developer's Reference - By Google](https://developers.google.com/speed/webp/)
* [WebP File Format - By Wikipedia](https://en.wikipedia.org/wiki/WebP)
