{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "HDR File Format - What is an HDR image file?",
  "description":"Learn about HDR file format and APIs that can create and open HDR files.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2022-07-21"
}

## What is an HDR file?

An HDR file is a High Dynamic Range (HDR) raster image file format for storing digital camera photos. It allows photo editors to enhance the color and brightness of digital images that have limited dynamic range. This modification can improve the brightness around the corners, resulting in a close-to-natural image. HDR files are usually saved as 32-bit raster images. Adobe Photoshop can create and open HDR files.

HDR files are also known as HDRI.

## HDR File Format - More Information

HDR file format is based on the original Radiance Picture (.pic) file format. The pixel data of an HDR file is usually stored uncompressed, but in some cases it is compressed using a straightforward run length encoding system.

### HDR File Structure

An HDR image file consists of the following three sections:

 * **Header:** An HDR file is identified by the first bytes in the image file i.e. "#?RADIANCE".
 * **Resolution String:** The Header is followed by a single resolution line that consists of 4 values; an X and Y label each followed by a numerical integer value. The order of the X and Y indicate rotation. The combination of X and Y with positive and negative values cover all the possible iamge orientation and rotations.
 * **Pixel Data:** The pixel data of an HDR file is either uncompressed or compressed using a standard run length encoding.

## Open-Source HDR/HDRI APIs

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** - Cross platform super fast single header [C++](/programming/cpp/) library to get image size and format without loading/decoding.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Rust library to get image size and format without loading/decoding. Supports [.avif](/image/avif/), [.bmp](/image/bmp/), [.cur](/image/cur/), [.dds](/image/dds/), [.gif](/image/gif/), hdr (pic), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/png/), [psd](/image/psd/), qoi, tga, tiff (tif), and webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Java implementation of HdrHistogram.

## References

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)
