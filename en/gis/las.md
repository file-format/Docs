{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "LAS - Lidar LASer File Format",
  "description": "Learn about LAS file format and APIs that can create and open LAS files.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-las"
    }
  },
  "lastmod": "2023-07-18"
}

## What is a LAS File?

The LAS (Lidar LASer) file format is a binary file format specifically designed for storing lidar point cloud data. It was developed and is maintained by the American Society for Photogrammetry and Remote Sensing (ASPRS) as a standardized format for lidar data exchange and interoperability.

LAS files store detailed information about individual lidar points, including their 3D coordinates (x, y, and z), intensity values, classification codes, and additional attributes. The format supports both discrete return and full waveform lidar data, allowing for the storage of multiple returns per laser pulse.

## LAS File Format

The structure of a LAS file consists of three main sections: the file header, the variable length records (VLRs), and the point data records. 

1. File Header: The file header contains essential information about the LAS file, such as the data format version, point data format, number of points, bounding box coordinates, coordinate reference system (CRS), and other metadata. It provides a summary of the lidar data contained within the file.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Point Data Records: The point data records store the actual lidar measurements. Each point data record represents a single lidar point and contains attributes such as x, y, and z coordinates, intensity values, classification codes (e.g., ground, vegetation, buildings), and other user-defined attributes. The point records can also store time stamps, return counts, and scan angles.

LAS files support different data formats (0 to 10) to accommodate various types of lidar data and the level of information needed. For example, format 0 represents a simple point format with basic information, while formats 1 to 3 provide more comprehensive data including waveform information for each return.

LAS files are widely supported by lidar software and processing tools, making them a standard format for lidar data exchange and analysis. In addition, LAS files can be compressed using lossless compression techniques to reduce file size while preserving the original data fidelity. The compressed version of LAS files is often referred to as LAZ, which offers efficient storage and data transfer capabilities.

## References

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm