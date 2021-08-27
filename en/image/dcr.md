{
  "date" : "2021-26-08",
  "keywords" : [ "dcr file", "dcr file format", "what is a dcr file", "file", "dcr example", "dcr file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "DCR - Digital Camera RAW Image File",
  "description":"Learn about DCR file format and APIs that can create and open DCR files.",
  "linktitle" : "DCR",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2021-26-08"
}

## What is a DCR file? ##
A file with dcr extension contains the content of a digital photograph saved in the Kodak Digital Camera RAW (DCR) format. The DCR is short for **Digital Camera Raw**; contains the uncompressed and lossless version of the images data captured by a Kodak digital camera. The professional photographers like to use these files, because they store images at a higher quality than low quality compressed image formats.

## DCR file format
The DCR is a proprietary format developed by Eastman Kodak Company; referred to simply as Kodak. A Digital Camera Raw (DCR) image file contains minimally processed data from the image sensor a digital camera. These files are not yet processed and therefore are not ready to be printed or edited with a bitmap graphics editor. 
Usually, a raw converter processes the image in a wide-gamut internal color space where accuracy and refinement can be made before conversion to a raster file format such as TIFF or JPEG for storage, printing, or further manipulation.
### File contents
The structure of raw files often follows a generic pattern:
- A short file header which contains an indicator of the byte-ordering of the file.
- Camera sensor metadata which is required to interpret the sensor image data, including the attributes of the CFA, the size of the sensor and its color profile.
- Image metadata which can be useful for inclusion in any CMS environment or database. Some raw files contain a standardized metadata section with data in Exif format.
- An image thumbnail.
- A full size JPEG conversion of the image, which is used to preview the file on the camera's LCD panel.
- In the case of motion picture film scans, either the timecode, keycode or frame number in the file sequence which represents the frame sequence in a scanned reel.
- The sensor image data
### Sensor image data
The raw file plays the role in the digital photography similar as photographic film plays in film photography. Raw files, thus contain the full resolution data as read out from each of the camera's image sensor pixels. The camera's sensor is almost constantly overlaid with a CFA (Color Filter Array. it can be used in high dynamic range imaging conversion when raw format data is available; as a simpler alternative to the multi-exposure HDI approach of capturing three separate images.


## References ##

* [Raw image format - By Wikipedia](https://en.wikipedia.org/wiki/Raw_image_format)
* [What Is a DCR File](https://expertphotography.com/dcr-file/)
