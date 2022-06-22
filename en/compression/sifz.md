{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "SIFZ File Format - Synfig Studio Compressed Project File",
  "description":"Learn about SIFZ file format and APIs that can create and open SIFZ files.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
    }
  },
  "lastmod" : "2021-04-30"
}

## What is a SIFZ file?

A SIFZ file is a gzip compressed SIF file created by the open source 2d animations creation application **Synfig Studio**. It contains multiple graphical elements that make up for the animation. The overall animation contents are built using a combination of a canvas that is filled with shapes, brush or pencil strokes, and text. All these are arranged at their own positions, radius, tangent, angle, vertex, and width handles. SIFZ files can be opened with [Synfig Studio](https://www.synfig.org/).

## SIFZ File Format

SIFZ files are compressed [ZIP](/compression/zip/) files that are packaged using the gzip compression method. Synfig is used to create film-quality animations using a vector and bitmap artwork. Unlike the old frame-by-frame animation creation method, it lets you produce 2D animations of higher quality with fewer resources.

SIFZ files, being compressed, are smaller than the uncompressed SIF files. This also makes it easy for transferring over low bandwidth internet connections.

## References

 * [Synfig Open Source - Github](https://github.com/synfig/synfig/)
 * [Synfig Documentation](https://synfig.readthedocs.io/en/latest/index.html)
