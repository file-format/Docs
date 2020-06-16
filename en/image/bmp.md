{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "BMP - Image File Format",
  "linktitle" : "BMP - Image File Format",
  "menu" : {
    "docs" : {
      "parent" : "image"
    }
  },
  "lastmod" : "2019-09-10"
}

# What is a BMP file? #

Files having extension .BMP represent Bitmap Image files that are used to store bitmap digital images. These images are independent of graphics adapter and are also called device independent bitmap (DIB) file format. This independency serves the purpose of opening the file on multiple platforms such as Microsoft Windows and Mac. The BMP file format can store data as two-dimensional digital images  in both monochrome as well as color format with various colour depths. 

## BMP File Format Specifications ##

Device Independent Bitmaps act as an aid to exchanging bitmaps between devices and applications. Due to the continuous evolution of this file format, the information contained in the headers can be different as per the version of Bitmap. A single bitmap file consists of fixed as well as variable-size structures in a specific sequence.

Structures in a Bitmap file are arranged in the following order:


|#Structure|#Optional|#Size|#Purpose
|File Header|No|14|To store general information about the bitmap image file
|DIB Header|No|Fixed-Size|To store detailed information about the bitmap image and define the pixel format
|Extra Bit Masks|Yes|12 or 16 bytes|To define the pixel format
|Colour Palette|Semi-optional|Variable-size|To define colours used by the bitmap image data
|Gap1|Yes|Variable-size|Structure alignment
|Pixel Array|No|Variable-size|Pixel format is defined by the DIB header or Extra bit masks.
|Gap2|Yes|Variable-size|Structure alignment
|ICC Color profile|Yes|Variable-size|To define the colour profile for colour management

When a bitmap image is loaded into memory, it becomes a DIB structure, used by Windows via its GDI API. The File header is not part of this data structure. The color can also consist of 16-bit entries that constitute indexes to the curently referenced palette instead of explicit RGB color definitions. Lets have a look at some of these in detail, especially the headers.

### Bitmap File Header ###

A Bitmap File Header is similar to other file headers used to identify the file. Since there are different variants to BMP file format, the first 2 bytes of the BMP file format are character "B" and then character "M" in ASCII encoding. All integer values are stored in little-endian format. 

|#Offset hex|#Offset dec|#Size|#Purpose
|00|0|2 bytes|The header field used to identify the BMP and DIB file is 0x42 0x4D in hexadecimal, same as BM in ASCII. It can following possible values.(((
* **BM** – Windows 3.1x, 95, NT, ... etc.
* **BA** – OS/2 struct bitmap array
* **CI** – OS/2 struct color icon
* **CP** – OS/2 const color pointer
* **IC** – OS/2 struct icon
* **PT** – OS/2 pointer
)))
|02|2|4 bytes|The size of the BMP file in bytes
|06|6|2 bytes|Reserved; actual value depends on the application that creates the image
|08|8|2 bytes|Reserved; actual value depends on the application that creates the image
|0A|10|4 bytes|The offset, i.e. starting address, of the byte where the bitmap image data (pixel array) can be found.

#### DIB header (bitmap information header) ####

The detailed information about the image is represented by this header. Based on this information, application will be determined that will be used to display the image on the screen. All such headers contain a DWORD (32-bit) field, specifying their size, so that an application can easily determine the header used int he image. This is basically due to the fact that the DIB format underwent several extensions. Following is the DIB Header with listed fields.

#### Color Palette ####

A BMP color palette is an array of structures that specify the RGB intensity values of each colour in a display device's colour palette. Each pixel in the bitmap data stores a single value used as an index into the colour palette. The colour information stored in the element at that index specifies the colour of that pixel. Availability of colour in a bitmap file varies as follow:

* One, 4 and 8-bit - expected to always contain a colour palette
* Sixteen, 24 and 32-bit - never contain colour palettes
* Sixteen and 32-bit BMP files - contain bitfields mask values in place of the colour palette

#### Pixel Storage ####

Bitmap pixels are stored as bits packed in rows where  the size of each row is rounded up to a multiple of 4 bytes (a 32-bit DWORD) by padding. The total amount of bytes required to store the pixels of an image can not be directly calculated by just counting the bits. Since there is padding involved, the effect of round up the size of each row to a multiple of 4 bytes is required. Padding bytes (not necessarily 0) are to be appended to the end of the rows in order to bring up the length of the rows to a multiple of four bytes. When the pixel array is loaded into memory, each row must begin at a memory address that is a multiple of 4.

The image is actually described by the 32-bit DWORDs representation of the pixel array. Usually pixels are stored "bottom-up", starting in the lower left corner, going from left to right, and then row by row from the bottom to the top of the image. Pixel formats and their implications are as listed below:

* The 1-bit per pixel (1bpp) format supports 2 distinct colours, (for example: black and white). 
* The 2-bit per pixel (2bpp) format supports 4 distinct colours and stores 4 pixels per 1 byte, the left-most pixel being in the two most significant bits. Each pixel value is a 2-bit index into a table of up to 4 colours.
* The 4-bit per pixel (4bpp) format supports 16 distinct colours and stores 2 pixels per 1 byte, the left-most pixel being in the more significant nibble. Each pixel value is a 4-bit index into a table of up to 16 colours.
* The 8-bit per pixel (8bpp) format supports 256 distinct colours and stores 1 pixel per 1 byte. Each byte is an index into a table of up to 256 colours.
* The 16-bit per pixel (16bpp) format supports 65536 distinct colours and stores 1 pixel per 2-byte WORD. Each WORD can define the alpha, red, green and blue samples of the pixel.
* The 24-bit pixel (24bpp) format supports 16,777,216 distinct colours and stores 1 pixel value per 3 bytes. Each pixel value defines the red, green and blue samples of the pixel (8.8.8.0.0 in RGBAX notation). Specifically, in the order: blue, green and red (8 bits per each sample).
* The 32-bit per pixel (32bpp) format supports 4,294,967,296 distinct colours and stores 1 pixel per 4-byte DWORD. Each DWORD can define the alpha, red, green and blue samples of the pixel.

## References ##

* [Windows MetaFile Format](http://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [BMP File Format](https://en.wikipedia.org/wiki/BMP_file_format)