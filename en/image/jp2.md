{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JP2 - Image File Format",
  "linktitle" : "JP2 - Image File Format",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a JP2 file? ##

JPEG 2000 (**JP2**) is an image coding system and state-of-the-art image compression standard. Designed, using wavelet technology JPEG 2000 can code lossless content in any quality at once. Moreover, without any substantial penalty in coding efficiency, JPEG 2000  have the capability to access and decode the same content efficaciously into a variety of other resolutions and qualities. The code streams in JPEG 2000 is significantly scalable having regions of interest that provide the facility for spatial random access. Possessing Up to 16384 diverse components with the dimensions in terapixels, and precision that can be high as 38 bits/sample.

JPEG 2000 stands out to be one of the most scalable standard.  Different parts of an image can be stored using diverse qualities. A noteworthy performance escalation can be achieved by ordering the code stream in a variety of ways. Nevertheless, JP2 requires complex and computationally challenging encoders/decoders, as an outcome of this flexibility. In comparison with JPEG, JPEG 2000  only produce ringing artifacts that makes rings near the image edge and can be blurry, while JPEG uses 8×8 visual artifacts blocks which can be both ringing and blocking artifacts.

## History ##

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard. Though most web browser are not ready to give a hand to JPEG 2000 since 2017.

## Parts of JPEG 2000 image coding system ##

Following are the main parts that constitute the complete suite of standards for JPEG 2000.


|Part|Title|Description|Number
---|---|---|---|
|Part 1|Core coding system|* Define syntax of code stream * Different stages involved in decoding JPEG 2000 images* Explains basic file format JP2, metadata, and IP rights to be provided.|ISO/IEC 15444-1
|Part 2|Extensions| * defines extensions for file format code stream * Allow HDR sample demonstrations, color space specification, cropping, geometric transforms; diverse animations, metadata, and multiple code stream.|ISO/IEC 15444-2
|Part 3|Motion JPEG 2000 (MJ2 or MJP2)|* Introduce a file format for motion sequences, encoding images in an independent code stream.|ISO/IEC 15444-3
|Part 4|Conformance|* States test techniques for encoding and decoding.* Check files for both bare code streams and JP2 files.|ISO/IEC 15444-4
|Part 5|Reference software| * Comprises of two source code packages (Java, C) that implement Core coding system and available under open-source licenses.|ISO/IEC 15444-5
|Part 6|Compound image file format|* Defines the JPM file format * Allows multi-page document imaging for fax-like applications.* Supports the use of JBIG2 and JPEG.|ISO/IEC 15444-6
|Part 8|JPEG 2000 Secured (JPSEC)|* ensures the security of transaction, contents, and technologies * Allows secured JPEG 2000 bit streams.|ISO/IEC 15444-8
|Part 9|JPIP|* Defines tools in a networked environment to access to metadata and imagery. * States Interactive and  efficient protocols|ISO/IEC 15444-9
|Part 10|JP3D|* Volumetric extension of Part 1.* Introduces the Z dimension* Extends the concept of tiles, code-blocks, precincts, and 3D region-of-interest accessibility features.|ISO/IEC 15444-10
|Part 11|JPWL|* Deals with well-organized transmission over an error-prone wireless network * This extension is compatible with decoders|ISO/IEC 15444-11
|Part 13|Entry-level Encoder|* Defines an entry level encoder implementation of Core coding system.|ISO/IEC 15444-13
|Part 14|JPXML|* A representation in XML* Explains marker segments and methods for accessing the internal data of imagery.|ISO/IEC 15444-14
|Part 15|HTJ2K (Under-development)| * Specifies an alternate block coding algorithm.* Algorithm offers a ten-fold increased throughput and lossless coding/decoding.|

## JP2 File Format ##

JPEG 2000 defines file format as well as code stream in the same way as JPEG-1. Though image samples is exclusively describes by JPEG 2000, yet JPEG-1 includes other added information about the color space and resolution of essential to encode the image. If an image stored as JPEG 2000 file, the **.jp2** is used as extension. This file format further improves by JPEG 2000 part-2 extension, which defines animation mechanisms and configuration of numerous code streams into one single image. **.jpx** extension is used when images save using this extended file-format. As code-stream data is not considered to be saved in files primarily, so no standard extension is defined for this purpose. Though for testing purposes, it frequently gets the extension **.jpc** or **.j2k**. In contrary to JPEG-1, JPEG 2000 chooses a different way of encoding metadata in XML format. The standard 12234-1.4(by the ISO TC42 committee) is used as reference between the Exif tags and the XML components. JPEG 2000 can contain an ISO standard, XMP within.

### Color transformation ###

 Initially, the transformation of images from RGB color space to another color space is required. For this purpose, there are two ways: Irreversible Color Transform (ICT) and Reversible Color Transform (RCT). Former uses YC,,B,,C,,R,, color space and has to be implemented in fix/floating –point while later a modified YUV color space and reversible in nature.// //Not restricted to RGB model, JPEG 2000 language uses multiple component transformation.

### Tiling ###

When the color transformation is done, image converts into rectangular regions called tiles that can be transformed and encoded separately. Size of the all tiles will have the same or the whole image can be consider as one single tile. Decoder takes the advantage of tiling and consume less memory or can partially encode some tiles. Though this technique has a disadvantage of quality degradation of picture.

### Wavelet transform ###

Image after tiling is wavelet transformed that can be either irreversible or reversible and implemented by using the convolution or lifting scheme.

### Compression Ratio ###

Depending upon the physical characteristics of an image, a compression gain of 20% is obtained Spatial-redundancy prediction of JPEG 2000 plays a vital role in compression process and   high resolution images tend to gain the most advantage.

## Applications served by the standard ##

* Recording, editing and storage of frame-based HD videos
* Medical imagery & biometrics
* satellite images, remote sensing  and motion detection
* Client/server communication, network distribution and storage.
* Digital cinema ,Live HDTV feed contribution, Digitized Audio-visual stuff

## References ##

* [Overview of JPEG 2000](https://jpeg.org/jpeg2000)
* [JPEG 2000 image coding system](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)
