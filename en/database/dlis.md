{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about DLIS file format and APIs that can create and open DLIS files.",
  "title" : "DLIS File Format - Well Log Data File",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis",
      "parent" : "database"
    }
  },
  "lastmod" : "2020-01-16"
}

## What is a DLIS file?

The .dlis file format is a standard file format for the storage and exchange of well log data in the oil and gas industry. The format was developed by the Logging Industry Data Standard (LIDS) committee and it stands for "Digital Log Information Standard." The format is designed to store well log data in a way that is easy to read, write and exchange between different systems.

DLIS files contain a set of logical records that describe the well log data and its characteristics, such as the type of log data (e.g. resistivity, gamma ray), the measurement units, and the location of the data in the well. The actual log data is stored in separate binary files and is referenced by the logical records in the DLIS file.

## Brief Information about Well Log Data

Well log data is a record of measurements taken at different depths in a well, typically during the drilling process or after the well has been drilled. These measurements can include various physical, chemical and/or geophysical properties of the rock and fluids in the well. Some examples of well log data include:

- Electrical resistivity: a measure of the ability of rock to resist the flow of an electrical current
- Gamma ray: a measure of the natural radioactivity of the rock
- Porosity: a measure of the amount of open spaces or pores in the rock
- Sonic: a measure of the time it takes for a sound wave to travel through the rock
- Density: a measure of the mass of a rock per unit volume
- Lithology: a measure of the rock type or formation

Well log data is used for various purposes in the oil and gas industry such as:

- Identifying the location and quality of hydrocarbon-bearing formations
- Evaluating the production potential of a well
- Planning and monitoring the completion and stimulation of a well
- Monitoring the well behavior over time

## Relation with PPDM

PPDM (Professional Petroleum Data Management) is an oil and gas industry data management standard that provides a common data model for managing well and production data. The PPDM data model defines a set of standard data objects and relationships that can be used to organize and manage well log data, including DLIS data.

The PPDM data model includes data objects for well and production data, such as wells, well headers, well logs, and production data. It also includes relationships between these data objects, such as the relationship between a well and the well logs that are associated with it.

The PPDM data model provides a consistent, industry-standard way to organize and manage well log data, including DLIS data. It allows different organizations to share and exchange data using a common data model, improving data interoperability and reducing data integration costs.

Using PPDM data model and DLIS data together makes it possible to store and manage well log data in a way that is consistent with industry standards and easily accessible to other systems and applications.

## References
* [Format for Digital Well Log Data](http://w3.energistics.org/rp66/V1/Toc/main.html)
* [DLIS - Data Organization](http://w3.energistics.org/rp66/V1/Toc/main.html)
