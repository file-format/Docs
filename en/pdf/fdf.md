{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "FDF File Format -  What is an FDF file?",
  "description":"Learn about FDF file format and APIs that can create and open FDF files.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an FDF file?

An FDF (**Forms Data Format**) file is a text document that is generated by exporting data from the form fields of a [PDF](/pdf/) file. It includes only text fields data that is extracted from the form fields available in a PDF file. This results in comparatively small data file as the exported data doesn't contain the form itself. Adobe Acrobat provides the feature of exporting form fields data by using the option of `Export Forms Data` from application menu.

## FDF File Format - More Information

FDF is plain text format and is included as part of the [ISO 32000 standard](https://www.iso.org/standard/51502.html) for Portable Document Format. It was developed by Adobe to allow import and export of data from Acrobat Forms, or AcroForms.

There are two types of FDF files:

• `Classic FDF` – It provides data to fill out an existing static form.

• `Template FDF` – Constructs a new PDF based on templates from inside specified PDF files. Forms inside the new document are filled by supplying data.

## Creating FDF using Adobe Acrobat

The [FDF toolkit](https://opensource.adobe.com/dc-acrobat-sdk-docs/) from Adobe lets you create FDF files from text data.

## References ##

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)