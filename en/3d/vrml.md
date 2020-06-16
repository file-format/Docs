{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "VRML",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

The Virtual Reality Modeling Language (VRML) is a file format for representation of interactive [3D](/3d/) world objects over the World Wide Web (www). It finds its usage in creating three-dimensional representations of complex scenes such as illustrations, definition and virtual reality presentations. The format has been superseded by [X3D](/3d/x3d/). Many 3D modelling applications can  save objects and scenes in VRML format. 

# VRML File Format #

VRML is a text file format that specifies information such as vertices and edges of a 3D polygon along with information such as surface colour, UV mapped textures, shininess, transparency and so on. It has the capability of representing static and animated objects in addition to having hyperlinks to other media such as sound, movies, and images. This allows opening hyperlinked elements when user clicks on these objects. TVRML files in common terminology are called "worlds" and have the .wrl extension. The textual nature of these files makes it possible to reduce the file size using compression formats such as gzip, making them more favourable for transfer over the internet quickly. The file format specifications for [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) acts as developer's reference for creating applications compatible for reading/writing these files.

## Design Criterion ##

The aim and design of VRML revolves around the following requirements.

* **Authorability - **Makes it possible to develop application generators and editors, and import data from other industrial formats
* **Completeness** - Provides all information necessary for implementation and address a complete feature set for wide industry acceptance
* **Composability** - The ability to use elements of VRML in combination and thus allow re-usability.
* **Extensibility - **The ability to add new elements.
* **Implementability - **Capable of implementation on a wide range of systems.
* **Multi-user potential** - Should not preclude the implementation of multi-user environments.
* **Orthogonality - **The elements of VRML should be independent of each other, or any dependencies should be structured and well defined.
* **Performance** - The elements should be designed with the emphasis on interactive performance on a variety of computing platforms.
* **Scalability - **The elements of VRML should be designed for infinitely large compositions.
* **Standard practice - **Only those elements that reflect existing practice, that are necessary to support existing practice, or that are necessary to support proposed standards should be standardized.
* **Well-structured - **An element should have a well-defined interface and a simply stated unconditional purpose. Multipurpose elements and side effects should be avoided.

## References ##

* [VRML - By Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [VRML v 2.0 File Format Specificaitons](http://gun.teipir.gr/VRML-amgem/spec/index.html)