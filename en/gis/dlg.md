{
  "date": "2021-07-30",
  "keywords": [
    "dlg file",
    "dlg file format",
    "what is a dlg file",
    "file",
    "dlg example",
    "dlg file extension",
    "extension",
    "format"
  ],
  "author": {
    "display_name": "Muhammad Umar"
  },
  "draft": "false",
  "toc": true,
  "title": "DLG - Shapefile Shape Index Format",
  "description": "Learn about DLG file format and APIs that can create and open DLG files.",
  "linktitle": "DLG",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-dlg"
    }
  },
  "lastmod": "2021-07-30"
}

## What is a DLG file?
A file with .dlg extension contains the Digital Line Graph which is a cartographic map feature showed in digital vector form that is administered by the U.S. Geological Survey (USGS). The DLG files are available in two different formats: 
1. **Optional format**: A simple-to-use format that incorporates an 80-byte logical record length, the UTM ground coordinate system, and topology linkages contained in line, node and area elements.
2. **Spatial Data Transfer Standard (SDTS) format**: a format that facilitates transferring of spatial data between different computer systems.

## DLG File Format
DLG file format is designed for USGS maps and are transmitted in large, intermediate and small scale with up to nine different categories of features. The DLG files come in optional and Spatial Data Transfer Standard (SDTS) formats having topologically structured for use in mapping and GIS applications.
### Specifications of DLG File Format
The DLG files are distributed at three different scales: 

1. **Large scale** - normally correspond to:
	- The USGS 7.5- by 7.5-minute
	- 1:24,000 and 1:25,000-scale topographic quadrangle map series
	- 1:63,360-scale for Alaska  
	- 1:30,000-scale for Puerto Rico
 
2. **Intermediate scale** - derived from the USGS: 
	- 30- by 60-minute 
	- 1:100,000-scale map series
3. **Small scale** -  derived from the USGS 1:2,000,000-scale sectional maps of the National Atlas of the United States
### Data Categories
Nine different categories of layers, or features, are available in DLG files:
1. Public Land Survey System (PLSS)
2. Boundaries (BD)
3. Transportation (TR)
4. Hydrography (HY)
5. Hypsography (HP)
6. Non-vegetative features (NV)
7. Survey control and markers (SM) 
8. Man-made features (MS) 
9. Vegetative surface cover (SC)

Large scale DLG files offer all nine layers, while intermediate-scale offer the five layers of PLSS, BD, TR, HY and HP. Small scale DLGs offer the five layers of PLSS, BD, TR, HY and MS.

## References

* [Digital line graph - by Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)

