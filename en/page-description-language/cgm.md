{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CGM File Format",
  "description":"Learn about CGM file format and APIs that can create and open CGM files.",
  "linktitle" : "CGM",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a CGM file? ##

Computer Graphics Metafile (CGM) is free, platform-independent, international standard metafile format for storing and exchanging of vector graphics (2D), raster graphics, and text. CGM uses object-oriented approach and many function provisions for image production. CGM uses these object-oriented characteristics for remolding graphical elements to render an image. A metafile contains necessary information that defines other files. In CGM, a text based source file contains all graphical elements that can be later compiled into a binary file. Basically CGM is a way to facilitate 2D graphical data interchange, independent from any particular platform, or device.

CGM format provides different elements to perform functions, and signify objects to adjust geometric primitives and graphical information. Although CGM has been superseded by other formats to display graphic arts on webpages as it is not well supported by web pages, still very popular among industrial, aeronautical, and other technical applications. Though World Wide Web Consortium has developed WebCGM, an alternative approach for the use of CGM on the Web. The primary CGM implementation was an illustration of sequence of basic operations of Graphical Kernel System (GKS). It has not been much adopted in professional designs but has largely supplanted by other formats such as DXF and SVG.

## History ##

CGM turned out to be an international standard in 1987 (ISO 8632-1987) and was also adopted as a national standard in UK by BSI and the USA by ANSI. After a number of amendments in 1991 a revised standard of CGM was released in 1992 (ISO 8632:1992). In 2001, World Wide Web Consortium developed WebCGM with enhanced capability to be used with the webpages. In 2007 a second version of WebCGM was released and third version was released in 2010 with enhanced capabilities.

## CGM File Format ##

Computer graphics metafiles are basically database for graphical information and provide the means for the capture, storage and transmission of graphical data.  Consequently, there must be a graphical system component for creating the database simultaneously along with the execution of an application in a metafile format. In most cases this component is the Metafile generator. Alongside, there is a need for another component that can fetch, interpret and render graphical data in a metafile. This need is fulfilled by the presence of metafile interpreter. Following figure represents the graphical metafile working environment.

The relationship of CGM with other components of a typical graphics system is illustrated in above figure. It is also evident from the figure that the functionality of metafile is not dependent on the final device output.

Generally, there are two categories of metafile: **section capture** and **picture capture**. Primary functionality of picture capture metafile is the capturing of device independent, multiple picture definitions. While session capture metafiles use the system interface to capture the output dialogue in a graphical system. CGM belongs to the category of static picture capture metafiles. CGM provides a well-organized arrangement of components with a two level structure.

1. Metafile descriptor
1. A pool of logically independent images

Each picture is a collection of picture descriptor and a picture body including a picture definition. metafile descriptor defines descriptive information that equally applies to all pictures of that metafile. This information helps the interpreter to correctly parse a metafile and recognize the resources that are required for correct rendering of a picture. Though the picture descriptor also encloses the descriptive information yet it can only recognize the picture in which descriptor resides. In this file format each picture definition is self-contained and logically sovereign. They are independent of all other picture definition in a file. Right after the interpretation of meta descriptor, pictures can be accessed and interpreted randomly. Change in the state of previous pictures have no effect on their successors. This picture independence is another prominent feature of CGM.CGM consists of coordinates space which are 2D Cartesian coordinates called virtual device coordinates and can be represent through number or precision representing the range and granularity. CGM specifies both direct selection of colors and index based selection. In former, color specifier consists of an RGB triple while in later, color specifier indicates an index in to a color table.

CGM matches the needs of both communication dependent as  well as performance dependent applications. Centralized and distributed graphics system can use CGM in unlimited number of ways.  It can be tailored to access graphics devices using a spooling system.
