{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OAM File - Adobe Edge Animate Widget File Format",
  "description" : "Learn about what is a OAM file and APIs that can create and open OAM file.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
    }
  },
  "lastmod" : "2023-01-30"
}

## What is an OAM file?

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
Users can create OAM files by publishing from an Edge Animate project (.AN file).

## OAM File Format

An OAM file is saved to disc as compressed [ZIP](/compression/zip/) archive. This implies that you can rename the file extension to .zip and extract with any compression utility such as WinZIP or WinRAR. The reduced file size makes it easier to transfer and share the animation with other users over the internet.

### OAM File Structure

The internal file structure of a .oam file is proprietary and not publicly documented by Adobe. However, it is known that .oam files contain a collection of files and resources (such as graphics, audio, and ActionScript code) packaged into a single file. The contents of a .oam file may include [XML](/web/xml/) files, SWF files, and other resource files. The exact structure of the .oam file depends on the specific version of Adobe Animate used to create it, as well as the type of animation and assets included in the file.

An OAM file contains the following information.

`Assets:` Information about the graphics, audio, and video assets used in the animation.

`Behaviors:` Descriptions of the actions and interactions that occur in the animation.

`ActionScript code:` The code used to control the animation's behavior and interactivity.

`Publish settings:` Information about the platform and format in which the animation will be published, such as HTML5 or AIR.

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## How to Open OAM File?

You can use the following applications to open OAM files.

 * Adobe Edge Animate CC (Discontinued)
 * Adobe Animate 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## References

* [OAM Publishing](https://helpx.adobe.com/animate/using/OAM-publishing.html)
