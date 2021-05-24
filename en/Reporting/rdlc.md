{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RDLC - Report Definition Language Client-side",
  "keywords" : [ "rdlc", "report definition language", "mkv format", "XSD", "report definition language client side"],
  "description":"Learn about RDLC file format which is an XML representation of a SQL Server Reporting Services report definition.",
  "linktitle" : "RDLC",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
    }
  },
  "lastmod" : "2021-03-02"
}

## What is an RDLC file? ##

The RDLC stands for Report Definition Language Client side. Actually It is an extension of report file created by using Microsoft reporting technology. The SQL Server 2005 version of Report Designer is used to create these files. The **ReportViewer** control in client side can directly execute the RDLC reports.

## RDL VS RDLC Files
|.rdl Files |.rdlc files|
---|---|
|RDL files are created by the SQL Server 2005 version of Report Designer|RDLC files are created by the Visual Studio 2005 version of Report Designer|
|It is used in SQL Server Reporting Services|It is used in Visual Studio|
|It is a remote report|It is a local report|
|Need a Reporting Services instance to run it|No need a Reporting Services instance|

## Creating Client Report Definition (.rdlc) Files
The ReportViewer control is used to run client report definition (.rdlc) files using the built-in processing capability of the control. The client reports that you run in local processing mode can be easily created in your application project. Following are the approaches for creating the report:

- Use the **Report Wizard** to Create a new client report definition (.rdlc).

- Create a new client report definition (.rdlc) file by using Visual Studio.

- Generate a report definition programmatically.


You can only preview a report by running it in a **ReportViewer** control. Please Note that you can open and edit the report definition at any time, and then build or deploy the application to check the results.

## References ##

- [Creating Client Report Definition (.rdlc) Files](https://docs.microsoft.com/en-us/previous-versions/visualstudio/visual-studio-2010/ms252067(v=vs.100))
