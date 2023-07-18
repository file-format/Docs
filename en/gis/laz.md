{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "LAZ - Compressed LIDAR Data Exchange File",
  "description":"Learn about LAZ file format and APIs that can create and open LAZ files.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
    }
  },
  "lastmod" : "2023-07-18"
}

## What is a LAZ File?

The LAZ file format is a compressed version of the LAS (Lidar LASer) file format, which is specifically designed for storing lidar point cloud data. LAZ files retain the same data and structure as LAS files but employ lossless compression techniques to reduce file size while preserving the original data fidelity.

## LAZ File Format - Brief History

TThe LAZ file format was developed to address the growing demand for efficient storage and transmission of large lidar datasets. By compressing LAS files, LAZ files significantly reduce their size, making them easier to manage and transfer. The compression is achieved by employing a combination of different algorithms, such as entropy coding and variable-length encoding, to represent lidar point attributes in a more compact form.

## LAZ File Format

Despite the compression, LAZ files retain the ability to fully restore the original LAS data without any loss of information. This means that once a LAZ file is decompressed, it can be processed and analyzed in the same way as an uncompressed LAS file. The compression and decompression process is typically performed using specialized software or libraries that support the LAZ format.

The LAZ file format maintains compatibility with LAS files, ensuring interoperability across lidar software and processing tools. This means that applications that can read and process LAS files can typically handle LAZ files without any modifications. Additionally, LAZ files still include the file header, variable length records (VLRs), and point data records, preserving the same structure as LAS files.

## Advantages of LAZ File Format

**Reduced File Size:** LAZ compression significantly reduces the file size of lidar datasets, making them more manageable and easier to store and transfer.

**Data Integrity:** LAZ compression is lossless, meaning that the decompressed data is an exact replica of the original LAS data, ensuring no loss of information or precision.

**Interoperability:** LAZ files are compatible with LAS files, allowing seamless integration with existing lidar software and workflows.

**Efficient Processing:** Due to their reduced size, LAZ files can be loaded and processed more quickly, improving overall processing and analysis times.

The LAZ file format has become widely adopted in the lidar community as a standard for compressed lidar data storage and exchange. It offers a balance between efficient data compression and data integrity, enabling easier handling of large lidar datasets while maintaining the accuracy and quality of the original data.

## References

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm