{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RML - Elixir Report Template File",
  "description":"Learn about RML file and APIs that can create and open RML files.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml",
      "parent" : "misc"
    }
  },
  "lastmod" : "2022-01-12"
}

## What is an RML file?

An RML file is a reporting template file with the [Elixir Repertoire](https://elixirtech.com/repertoire-2/) reporting engine. The template file is used to generate reports with the data source connected to the Elixir FileSystem. Data is read and populated in the RML template file and can be exported to a number of different file formats such as [PDF](/pdf/), [RTF](/word-processing/rtf/), and spreadsheet [XLS](/spreadsheet/xls/). Elixir Repertoire reporting engine can be connected to a wide variety of JDBC data sources.

## RML File Format

The internal file structure details of RML file format are not available publicly. The files are generated and saved internally by the Elixir Repertoire application to generate reports with data populated from the connected data sources. The RML template file contains the overall layout and placeholders information of the final report to be generated from the data.

## How to RML Template File?

In order to generate RML template in Elixir Repertoire, the following steps can be followed.

1. Connect a JDBC data source to the file system.
1. Launch the Report Template Wizard
1. Use the software to locate the datasource .ds file
1. Choose tabular report as choice of export
1. Select the fields to be included in the report template
1. Finally, on clicking the Finish button, First report.rml is added to the repository and opened to show the Layout tab.

## References

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)
