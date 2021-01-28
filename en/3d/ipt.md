{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about IPT file format and APIs that can open and create IPT files.",
  "title" : "IPT - Autodesk Inventor Part File",
  "linktitle" : "IPT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2021-01-25"
}

## What is an IPT file?

A file with .ipt extension is native Autodesk's Inventor Part file format for parts. It is used in combination with Autodesk assembly (.iam) files. IPT files can be imported in 3DS Max as Body Objects where the geometry in the ACIS solids format remains in the same format. 3DS Max retains the object naming as assigned in Autodesk Inventor and the component models can be edited similar to other objects including applying modifiers, alter materials, add lighting and cameras, create animation, and so on. You can open IPT files with applications such as Autodesk Inventor and Autodesk Fusion.

## IPT File Format

An Autodesk IPT file comprises of sketches, features, and bodies that make the part capable of being used in assemblies. A sketch is the mostly used component and most parts start with a sketch. It is the profile of a feature and any geometry that is required to create the feature. Multiple features make up a `part model` and a multi-body part can be share features. The geometric relationships such as parallel and perpendicular are controlled by sketch constraints. The effect of modifications can be observed by adjusting the constraints or dimensional parameters for controlling the size and shape of a model.

IPT file format specifications are not available publicly.

## References

 * [IPT Files - Autodesk](https://knowledge.autodesk.com/support/inventor/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/Inventor-Help/files/GUID-94B779C0-6B2B-499A-A4F9-2E4BAB49712F-htm.html)
