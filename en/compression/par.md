{
   "date":"2023-07-18",
   "keywords":[
      "PAR",
      "PAR File",
      "how to open a par file",
      "file",
      "PAR file extension",
      "extension",
      "file"
   ],
   "author":{
      "display_name":"Shakeel Faiz"
   },
   "draft":"false",
   "toc":true,
   "title":"PAR File Format - Parchive Index File",
   "description":"Learn about PAR format and APIs that can create and open PAR files.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par",
         "parent":"compression"
      }
   },
   "lastmod":"2023-07-18"
}

## What is a PAR file?

Within Parchive (PAR) archives, a .par file refers to an index file that contains a group of parity volumes or parity blocks. This index file is used for error detection and recovery purposes when one or more files in the archive are lost or damaged.

A Parchive archive typically consists of both the original data files and the corresponding parity volumes. Parity volumes are created using Reed-Solomon error correction algorithms. These parity volumes contain redundant information that can be used to recover the original data files.

The .par file, also known as a parity volume set, contains information about the structure and location of the parity volumes within the archive. It serves as an index or map for the recovery process. By using the .par file, specialized PAR software can determine which parity volumes are needed and how they should be used to reconstruct the missing or damaged files.

When one or more files within the Parchive archive become inaccessible or corrupt, the .par file can be utilized in conjunction with the available parity volumes to recover the lost data. The PAR software reads the .par file, identifies the missing or damaged files, and uses the parity volumes to reconstruct them.

## How to open a PAR file?

To open and use .par files, you will need specialized PAR software. Here are a few popular software options that can handle .par files:

- **QuickPar:** QuickPar is a widely used PAR software for Windows. It allows you to create, verify, and repair PAR files. You can open a .par file in QuickPar to verify its integrity or use it to repair damaged or missing files in a Parchive archive.

- **MultiPar:** MultiPar is another popular PAR software available for Windows. It supports both PAR and PAR2 file formats and provides advanced features for creating, verifying, and repairing archives. MultiPar can open .par files and perform error detection and recovery operations based on the provided parity volumes.

- **MacPAR deLuxe:** MacPAR deLuxe is a PAR software designed specifically for macOS. It supports PAR and PAR2 file formats and provides similar functionality as QuickPar and MultiPar. MacPAR deLuxe can open .par files and assist in verifying archives and recovering damaged or missing files.

## PAR File Format - More Information

The PAR file format, commonly referred to as Parchive, is a specific file format used for creating parity data and performing error detection and recovery in file archives. The PAR file format typically consists of three types: PAR, PAR2, and PAR3.

- **PAR:** The original PAR file format, also known as PAR1, was developed by the Parchive project. It includes parity data generated from the original data files. PAR files provide a basic level of error detection and recovery but have limitations in terms of error correction capabilities.

- **PAR2:** PAR2 is an improved version of the PAR file format. It offers more advanced error correction capabilities and enhanced recovery features. PAR2 files are typically used for creating parity data that can recover lost or damaged files within an archive. PAR2 files provide better protection against data corruption and are widely used for file archiving purposes.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. PAR3 files are designed to provide more robust protection and recovery options for data stored in archives.

Both PAR2 and PAR3 file formats are widely supported by PAR software and offer the ability to verify the integrity of files within an archive and recover lost or damaged data. PAR and PAR2 files are still commonly used, while PAR3 files are gradually gaining adoption due to their enhanced error correction capabilities.

## References
* [Parchive](https://en.wikipedia.org/wiki/Parchive)
