{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ File -  What is a EAZ file and how to open it?",
  "description":"Learn about EAZ file format and APIs that can create and open EAZ files.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-eaz"
    }
  },
  "lastmod" : "2023-12-23"
}

## What is an EAZ file?

The EAZ file is an Add-in file utilized by ArcGIS Explorer, a free application developed by ESRI for map exploration, visualization, and sharing. It contains a compressed file archive that includes an [XML file](/web/xml/), compiled code, and supporting files necessary for the add-in. These files are employed to expand the base functionality of the software by incorporating new buttons, dockable windows, and other extensions.

## EAZ File Format - More Information

EAZ files are created through the utilization of the ArcGIS Explorer SDK, a development kit designed for creating custom functionalities within ArcGIS Explorer. These files utilize [ZIP](/compression/zip/) compression to efficiently package their contents. At the core of the archive, the **Addins.xml** file resides in the root directory, serving as a vital component that outlines and details the various customizations embedded in the EAZ file.

The Addins.xml file essentially acts as a roadmap, offering insights into the specific enhancements, modifications, and extensions that the EAZ file introduces to ArcGIS Explorer. Through this comprehensive structure, developers can encapsulate and seamlessly integrate new features, buttons, and dockable windows, enhancing the overall functionality and user experience of the ArcGIS Explorer application.

## References

 * [Sharing and installing add-ins
](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)