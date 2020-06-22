{
  "date" : "2019-11-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "JPEG - Image File Format",
  "linktitle" : "JPEG - Image File Format",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-11-25"
}

## What is a JPEG file? ##

A JPEG is a type of image format that is saved using the method of lossy compression. The output image, as result of compression, is a trade-off between storage size and image quality. Users can adjust the compression level to achieve the desired quality level while at the same time reduce the storage size. Image quality is negligibly affected if 10:1 compression is applied to the image.  The higher the compression value, the higher the degradation in image quality. JPEG image file format was standardized by the Joint Photographic Experts Group and, hence, the name JPEG. The format has been the choice of storing and transmitting photographic images on the web. Almost all Operating systems now have viewers that support visualization of JPEG images, which are often stored with JPG extension as well. Even the web browsers support visualization of JPEG images.

## File Format Specifications ##

Before going into the JPEG file format specifications, the overall process of steps involved in JPEG creation need to be mentioned.

### JPEG Compression Steps ###

**Transformation:** Color images are transformed from RGB into a luminance/chrominance image (Eye is sensitive to luminance, not chrominance, so that chrominance part can lose much data and thus can be highly compressed.

**Down Sampling:** The down sampling is done for colored component and not for luminance component .Down sampling is done either at a ratio 2:1 horizontally and 1:1 vertically (2h 1 V). Thus the image reduces in size since the ‘y’ component is not touched, there is no noticeable loss of image quality.

**Organizing in Groups:** The pixels of each color component are organized in groups of 8×2 pixels called “ data units” if number of rows or column is not a multiple of 8, the bottom row and rightmost columns are duplicated.

**Discrete Cosine Transformation:** Discrete Cosine Transform ( DCT) is then applied to each data unit to create 8×8 map of transformed components.DCT involves some loss of information due to the limited precision of computer arithmetic. This means that even without the map there will be some loss of image quality but it is normally small.

**Quantization:** Each of the 64 transformed components in the data unit is divided by a separate number called its ‘Quantization Coefficient (QC)’ and then rounded to an integer. This is where information is lost irretrievably, Large QC cause more loss. In general, the most JPEG implements allow use QC tables recommended by the JPEG standard.

**Encoding:** The 64 quantized transformed coefficients ( Which are now integers) of each data unit are encoded using a combination of RLE and Huffman coding.

**Adding Header:** The last step adds header and all the JPEG parameters used and output the result.

The JPEG decoder uses the steps in reverse to generate the original image from the compressed one.

### File Structure ###

A JPEG image is represented as a sequence of segments where each segment begins with a marker. Each marker starts with 0xFF byte followed by marker flag to represent the type of marker. The payload followed by marker is different as per marker type. Common JPEG marker types are as listed below:

|Short Name|Bytes|Payload|Name|Comments
---|---|---|---|---|
|SOI|0xFF, 0xD8|none|Start of Image|
|S0F0|0xFF, 0xC0|variable size|Start of Frame|
|S0F2|0xFF, 0xC2|variable size|Start fo Frame|
|DHT|0xFF, 0xC4|variable size|Define Huffman Tables|
|DQT|0xFF, 0xDB|variable size|Define Quantization Table(s)|
|DRI|0xFF, 0xDD|4 bytes|Define Restart Interval|
|SOS|0xFF, 0xDA|variable size|Start Of Scan|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|none|Restart|
|APPn|0xFF, 0xE//n//|variable size|Application specific|
|COM|0xFF, 0xFE|variable size|Comment|
|EOI|0xFF, 0xD9|none|End Of Image|

Within the entropy-coded data, after any 0xFF byte, a 0x00 byte is inserted by the encoder before the next byte, so that there does not appear to be a marker where none is intended, preventing framing errors. Decoders must skip this 0x00 byte. This technique, called [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) (see JPEG specification section F.1.2.3), is only applied to the entropy-coded data, not to marker payload data. Note however that entropy-coded data has a few markers of its own; specifically the Reset markers (0xD0 through 0xD7), which are used to isolate independent chunks of entropy-coded data to allow parallel decoding, and encoders are free to insert these Reset markers at regular intervals (although not all encoders do this).
