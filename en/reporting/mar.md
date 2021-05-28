{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MAR - Microsoft Access Reports File",
  "keywords" : [ "mar", "mar file", "mar file format", "what is access report", "access report", "microsoft access report"],
  "description":"Learn about Acess Report (MAR) file format used by Microsoft Access software to create a shortcut or link to Microsoft Access Report.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
    }
  },
  "lastmod" : "2021-28-05"
}

## What is Access Report (MAR file)? ##
A file created by Microsoft Access as a shortcut of its report is saved with .mar file extension. A **Microsoft Access report** offer a way to format, view, and summarize the information in the Microsoft Access database. These reports allows you to format your data in a precise and informative layout for viewing on screen or printing.

## Microsoft Access Report (MAR) file format

The MAR file format is used by Microsoft Access software to create a shortcut or link to Microsoft Access Report which is a database object that become useful when you need to present the information in your database for any of the following uses:

- Display a summary of data.
- Archive snapshots of the data.
- Display details about individual records.
- Create labels. 

## Parts of Access Report
The design of an Access report is divided into different sections which can be viewed in the Design view. Following table explains that how each section works and can helps you create reports.
| Section | How the section is displayed when printed | Where the section can be used |
---------|----|------|
| Report Header | At the beginning of the report. | Use the report header for information that might normally appear on a cover page, such as a logo, a title, or a date. When you place a calculated control that uses the Sum aggregate function in the report header, the sum calculated is for the entire report. The report header is printed before the page header. |
| Page Header | At the top of every page. | Use a page header to repeat the report title on every page. |
| Group Header | At the beginning of each new group of records. | Use the group header to print the group name. For example, in a report that is grouped by product, use the group header to print the product name. When you place a calculated control that uses the Sum aggregate function in the group header, the sum is for the current group. You can have multiple group header sections on a report, depending on how many grouping levels you have added. For more information about creating group headers and footers, see the section Add grouping, sorting, or totals. |
| Detail | Appears once for every row in the record source. | This is where you place the controls that make up the main body of the report. |
| Group Footer | At the end of each group of records. | Use a group footer to print summary information for a group. You can have multiple group footer sections on a report, depending on how many grouping levels you have added. |
| Page Footer | At the end of every page. | Use a page footer to print page numbers or per-page information. |
| Report Footer | At the end of the report. Note:  In Design view, the report footer appears below the page footer. However, in all other views (Layout view, for example, or when the report is printed or previewed), the report footer appears above the page footer, just after the last group footer or detail line on the final page. | Use the report footer to print report totals or other summary information for the entire report. |






## References ##

- [Introduction to reports in Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Designing Reports in Access](https://www.uis.edu/informationtechnologyservices/wp-content/uploads/sites/106/2013/04/DesigningReportsinAccess2010.pdf)
