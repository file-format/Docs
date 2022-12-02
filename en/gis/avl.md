{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ArcView Legend File",
  "description":"Learn about AVL file format and APIs that can create and open AVL files.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl",
      "parent" : "gis"
    }
  },
  "lastmod" : "2022-11-30"
}

## What is an AVL file?

An AVL file is a legend file that contains a key for a map generated with ESRI ArcView GIS (Geographic Information System) software. It contains reference symbology information used in the corresponding map for access. An AVL file can contain more information such as Symbology, Display settings, such as transparency, Scale dependent display properties, joined table/related table information, Definition query, labelling properties for feature layers, and Annotation display properties for annotation layers depending on the type kind of layer.

An AVL file may be referenced from the ArcView project [.APR](/gis/apr/) file.

## AVL File Format - More Information

AVL files are saved in plain text file format. It means you can open AVL files in any text editor such as Notepad, Notepad++, and Apple TextEdit. Once opened, you can not only view the content of the file but also modify these.

### Difference between .LYR and .AVL Files

 * **File Format Difference** - .lyr is a binary file whereas .avl is a text file
 * **Content Difference** - A .lyr file contains more information than a .avl file. An AVL file only stores symbology information, while a LYR file stores all the information that is available in the layer properties dialog box in ArcMap.

## References

* [Difference between .lyr and .avl Files](https://support.esri.com/en/technical-article/000005936)
