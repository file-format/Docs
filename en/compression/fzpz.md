{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FZPZ File Format - Fritzing Part File",
  "description":"Learn about what is a FZPZ file and APIs that can create and open FZPZ files.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2022-06-20"
}

## What is a FZPZ file?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/image/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ File Format - More Information

FZPZ files are saved to disc as compressed [ZIP](/compression/zip/) archives. You can rename the extension from .fzpz to .zip and use any standard decompression utility such as WinZIP to extract the files from the archive.

### FZPZ File Structure Information

As mentioned, an FZPZ file is an archive file that contains multiples files for representation of a part used in printed circuit board. The FZPZ contains the following files:

 * `Four SVG files` - that represent part's breadboard, schematic, PCB and icon images
 * `FZP file` - An XML file that contains information about the part's properties, connectors, and buses

 The files are usually named as follow.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## References ##

* [New parts with fzpz extension](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)
