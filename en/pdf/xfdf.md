{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "XFDF File Format -  What is an XFDF file?",
  "description":"Learn about XFDF file and APIs that can create and open XFDF files.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an XFDF file?

A file with .xfdf extension is an XML Forms Data Format that is generated with Adobe Acrobat software. Like [FDF](/pdf/fdf/), XFDF contains form elements description and their values in XML format. This can include the names and values of text fields in the PDF form. XFDF are saved in human-readable format and can be read programatically read using programming languages such as C#.

## XFDF File Format - More Information

XFDF files are saved in XML file format that is a universal format used for import and export of data. An XFDF file structure consists of a header, followed by field values, and elements data as shown below.

|Element|Attribute|Content|
---|---|---|
|\<XFDF>		||Topmost element|
|\<fields>		||All the field values for this template|
|<field (T)>	|name	|Field name|
|<value (V)>	|value	|Field value|

## References

* [FDF Format Support by Acrobat](https://helpx.adobe.com/coldfusion/developing-applications/working-with-documents-charts-and-reports/assembling-pdf-documents/fdf-format-support-for-acroforms.html)
* [Adobe Developer Resources](https://opensource.adobe.com/dc-acrobat-sdk-docs/)
