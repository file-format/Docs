{
  "date": "2021-06-29",
  "keywords": [
    "CUR",
    "extension",
    "file",
    "format",
    "image",
    "Device-Independent Bitmap",
    "Cursor File Format",
    "Cursor",
    "Windows",
    "application"
  ],
  "author": {
    "display_name": "Sami Cheema"
  },
  "draft": "false",
  "toc": true,
  "title": "CUR - Cursor File Format",
  "description": "Learn about CUR file format and APIs that can create and open CUR files.",
  "linktitle": "CUR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-cur"
    }
  },
  "lastmod": "2021-06-29"
}

## What is a CUR file? ##

A CUR file is a static Microsoft Windows cursor file format. Basically, they are stationary images identical to ICO (icon) files in every way except the extension. Both CUR and [ICO](/image/ico/) are established on the basis of the Device-Independent Bitmap [DIB](/image/dib/) (Device-Independent Bitmap) specification. Default, as well as custom cursor such as Windows mouse pointer for Windows operating system, are stored in CUR files. It can be an arrow for normal use, a spinning hourglass to demonstrate waiting periods, or an I-bar for text editing. CUR files come along with the installation pack of the custom desktop themes to ensure that the Windows cursor matches the custom desktop theme.

## Technical Specification ##

CUR files are binary system files that can be found on devices functioning on Microsoft Windows operating system. CUR pointer images come in different standard sizes like 16×16, 32×32, etc. CUR files are very similar to the ICO files; both of them consist of small stationary images. Only the extension of CUR and ICO files are different. Furthermore, the explanation of a hotspot in the header of the CUR file is distinct from the ICO file. The hotspot interprets the pixel offset from the top left corner to the place where you are pointing the mouse. Windows systems are still using the CUR files, but now the animated cursors usually have the file extension ANI instead of CUR.

## Brief History ##

The CUR file is made from the ICO file. The first CUR file format was incorporated into Microsoft's Windows 1.0 operating system in 1981 to smoothen commercial usage. Soon more interactive cursors were introduced allowing users to amend their cursor preferences from the pre-installed options available. However, it is easy to edit a CUR file on your own even if you have insufficient technical knowledge. 


## CUR Example ##

The CUR files can be found at *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="CUR File Format" >}}
