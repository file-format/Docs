{
  "date" : "2019-10-11",
  "keywords" : [ "MPX", "File", "Extension", "File Format", "Project", "Management", "Microsoft Project Exchange"],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MPX - Microsoft Project Exchange File Format",
  "description":"Learn about MPX file format and APIs that can create and open MPX files.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
    }
  },
  "lastmod" : "2021-05-07"
}

## What is an MPX file? ##

A file with extension .mpx is a Microsoft Exchange File Format. An MPX file format was developed by Microsoft Project (MSP) to facilitate project information exchange between MSP and other applications supporting the MPX file format, including Primavera Project Planner, Sciforma, and Timerline Precision Estimating. Using the MPX files, you can transfer all kinds of information from a project to a different system, such as detailed resource assignment information, calendar information, or info from the Project Info dialog box.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. However, support for creating MPX files has discontinued the release of Microsoft Project 2000, and the versions till Microsoft Project 2010 support only MPX reading. MPX file format is not supported in versions later than MSP 2010.

## MPX File Format ##

An overview of the MPX file specifications is given in this section. Complete specifications can be found in this [Knowledge Base](https://support.microsoft.com/en-us/help/270139/prj-description-of-the-mpx-project-file-exchange-format) article and can be referred for details.

### Records ###

A Record of the MPX file consists of information for the project. There are different types of records where each record has its own order. Each record type is identified by its record number. For an MPX file, it is necessary to contain the File Creation record type. Other types of records are not mandatory. The following table shows all the record types, their record numbers, and the number of records each type may contain in the MPX file. Record inclusion in the MPX file must follow the table order, with comments inserted anywhere.

|Record Name|Record Number|Maximum number of Records
---|---|---|
|File Creation (required)|none|1
|Currency Settings|10|1
|Default Settings|11|1
|Date and Time Settings|12|1
|Base Calendar Definition|20|250
|Base Calendar Hours|25| 7 per Base Calendar Definition record
|Base Calendar Exception|26| 250 per Base Calendar Definition record
|Project Header|30|1
|Text Resource Table Definition|140|1- (Or you can use the Numeric Resource Table Definition record)
|Numeric Resource Table Definition|41|1
|Resource|50|9,999
|Resource Notes|51| 1 per Resource record
|Resource Calendar Definition|55| 1 per Resource record
|Resource Calendar Hours|56| 7 per Resource Calendar
|Resource Calendar Exception| 57|250 per Resource Calendar
|Text Task Table Definition|60|1 (Or you can use the Numeric Task Table Definition record)
|Numeric Task Table Definition|61|1
|Task|70|9
|Task Notes|71| 1 per Task record
|Recurring Task|72| 1 per Task record
|Resource Assignment|75| 100 per Task record
|Assignment Workgroup fields|76| 1 per Assignment record
|Project Names|80|500
|DDE and OLE Client Links|81|500
|Comments|0|unlimited

### File Structure ###

An MPX file consists of records mentioned above that are arranged in pre-set manner inside the file. Details about these record types are discussed as follow:

**File Creation Record (FCR):** This is a mandatory record whose purpose is to identify the:

* File format (MPX)
* List separator character used in the file
* Program and version number used to create the file
* Version number of the MPX file format used in the file
* Code page used to create the file

This must be the first record in the file. When exporting from Microsoft Project, the list separator character is specified in the Regional Settings item in the Windows Control Panel. An FCR Record includes the following fields:

* MPX followed immediately by the list separator character
* Program Name/Identifier
* Version Number of the file
* Code Page (850, 437, MAC, ANSI)

For example, the record can contain information **MPX, Microsoft Project, 3.0**, which specifies that a comma is used as the list separator character in this MPX file. The version of the MPX format used in the file is exported from Microsoft Project version 3.0.

**Currency Settings** This record, having record number 10, specifies settings for the currency options in the Options dialog box. If this record is not included, the current settings in the Options dialog box are used. The Thousands and Decimal separators are specified in the Regional Settings item in the Windows Control Panel.
The fields included in this record are:

* Currency Symbol
* Symbol Position (0 # after, 1 # before, 2 # after with a space, 3 # before with a space)
* Currency Digits (0,1,2)
* Thousands Separator
* Decimal Separator

**Example:** 10,$,1,2,",",.
This example specifies that currency values include a dollar sign ($) before them, that two digits are included after the decimal point, that a comma is used to separate thousands, and that a period is used as the decimal point. Because the list separator character is included in the Thousands Separator field, the field is surrounded by quotation marks.

**Default Settings:** This record, having record number 11, specifies settings for the default options in the Options dialog box. If a duration is not specified, the Default Duration Unit needs to be set for correct duration unit calculations. If this record is not included, the current settings in the Options dialog box are used. 
The fields included in this record are:

* Default Duration Units (0 # minutes, 1 # hours, 2 # days, 3 # weeks)
* Default Duration Type (0 # not fixed, 1 # fixed)
* Default Work Units (0 # minutes, 1 # hours, 2 # days, 3 # weeks)
* Default Hours/Day
* Default Hours/Week
* Default Standard Rate
* Default Overtime Rate
* Updating Task Status Updates Resource Status (0 # no, 1 # yes)
* Split In-Progress Tasks (0 # no, 1 # yes)

**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\The fields included in this record are:

* Date Order (0 # month/day/year, 1 # day/month/year, 2 # year/month/day)
* Time Format (0 # 12 hour, 1 # 24 hour)
* Default Time (number of minutes after midnight)
* Date Separator
* Time Separator
* 0:00 to 11:59 Text
* 12:00 to 23:59 Text
* Date Format (0 -14)*
* Bar Text Date Format (0 -194)*

**Base Calendar Definition:**  These records, having record number 20, define base calendars and their working and non-working days of the week. The default settings are used if there is no entry for a day. The default settings are Monday through Friday for working days and Saturday and Sunday for non-working days. In this record, the Name field is required. For each of the days, an entry of 0 indicates that the day is a non-working day, and an entry of 1 indicates that the day is a working day.
The fields included in this record are:

* Name
* Sunday
* Monday
* Tuesday
* Wednesday
* Thursday
* Friday
* Saturday

**Base Calendar Hours:** These records, having record number 25, specify the working hours for the days of the week if they differ from the default settings. The default working hours are 8:00 A.M. to 12:00 P.M. and 1:00 P.M. to 5:00 P.M. Each Base Calendar Hours record refers to the preceding Base Calendar Definition record. Up to seven of these records can follow each Base Calendar Definition record.

* Day of the Week (1 - 7, where 1 # Sunday and 7 # Saturday)
* From Time 1
* To Time 1
* From Time 2
* To Time 2
* From Time 3
* To Time 3

**Base Calendar Exception:** These records, having record number 26, define the exceptions to the days and hours specified in the previous two record types. Up to 250 of these records can follow each Base Calendar Definition record. These records must be listed in chronological order. If an exception is one day, you can leave the To Date field empty. If no times are indicated, the default times of 8:00 A.M. to 12:00 P.M. and 1:00 P.M. to 5:00 P.M. are used.
The fields included in this record are:

* From Date
* To Date
* Nonworking/Working (0 # non-working, 1 # working)
* From Time 1
* To Time 1
* From Time 2
* To Time 2
* From Time 3
* To Time 3

**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
The fields and tabs included in this record are:

* Project tab
* Company
* Manager
* Calendar (Standard used if no entry)
* Start Date (either this field or the next field is calculated for an imported file, depending on the Schedule From setting)
* Finish Date
* Schedule From (0 # start, 1 # finish)
* Current Date*
* Comments
* Cost
* Baseline Cost
* Actual Cost
* Work
* Baseline Work
* Actual Work
* Work
* Duration*
* Baseline Duration*
* Actual Duration
* Percent Complete
* Baseline Start
* Baseline Finish
* Actual Start
* Actual Finish
* Start Variance
* Finish Variance
* Subject
* Author
* Keywords

**Text Resource Table Definition**: This record lists the resource fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. For exported files, this record comes from the resource Export table. Either this record or the Numeric Resource Table Definition record must be used. When exporting from Microsoft Project, both of these records are included.

**Numeric Resource Table Definition:** Using numbers rather than names, this record lists the resource fields, in order, that are being imported or exported. This is an alternate method for identifying the resource fields included in each Resource record and is useful when defining an MPX file created by a foreign language product.

**Resource:** These records contain the information for each resource being imported or exported. Each Resource record describes one resource. When you import information, the fields that are included are defined by the Text Resource Table Definition record or the Numeric Resource Table Definition record. When you export information, the fields that are included are those listed in the resource Export table.

**Resource Notes:** These records contain notes about the immediately preceding Resource record. For a new line within the note, ASCII character 127 is used. If the note includes the list separator character, enclose the note in quotation marks.

**Resource Calendar Definition:** These records define the working days for the resource specified in the immediately preceding Resource record. For imported files, if there is no entry for the Base Calendar Name field, Standard is used. No entry for the specific day indicates that the day is set to the default (2). If there are no Resource Calendar Definition records, Standard is used as the base calendar for the resource, with default used for the days. For each of the days, an entry of 0 indicates that the day is a non-working day, 1 indicates that the day is a working day, and 2 specifies that the default is used.

**Resource Calendar Hours:** These records define the working hours for the resource that differs from the base calendar used by the resource. These records apply to the Resource Calendar Definition record immediately preceding this record. Up to seven of these records can follow each Resource Calendar Definition record.

**Resource Calendar Exception:**  These records define the exceptions to the days and hours specified in the previous two record types. Up to 250 of these records can follow each Resource Calendar Definition record. These records must be listed in chronological order. If the exception is only one day, you can leave the To Date field empty. If no times are indicated, the default times of 8:00 A.M. to 12:00 P.M. and 1:00 P.M. to 5:00 P.M. are used.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Numeric Task Table Definition:** Using numbers rather than names, this record lists the task fields, in order, that are being imported or exported. This is an alternate method for identifying the task fields included in each Task record and is useful when defining an MPX file created by a foreign language product.

**Task:** These records contain the information for each task being imported or exported. Each Task record describes one task. When you import information, the fields that are included are defined by the Text Task Table Definition record or the Numeric Task Table Definition record. When you export information, the fields that are included are those listed in the task Export table.

**Task Notes:** These records contain notes about the immediately preceding Task record. Use ASCII character 127 to indicate a new line within the note. If the note includes the list separator character, enclose the note in quotation marks.

**Resource Assignment**: These records list information about the resources assigned to the task that was defined in the preceding Task record. If you are merging files, and you want resource assignment information retained, you need to include the information in the MPX file. If you merge, all existing assignments on merged tasks will be deleted. If you are merging files based on Unique IDs, resources are assigned using the Resource Unique IDs rather than IDs.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. If you are use the Workgroup features, you need to include this record to ensure that none of the information is lost.

**Project Names:** These records list all of the DDE link names stored in the project.

**DDE and OLE Client Links:** These records list the DDE links into the project.

**Comments:** These records can be used to add comments to the file and can appear in any position in the file. Each Comments record must begin with a "0."

## Problems to Open an MPX file ##

Here is the list of some common issues which may arise and cause misfunctioning of the MPX format:

 *   Absence of supporting software
 *   Corrupt file
 *   Infected file due to virus
 *   No access right in the system to open the files
 *   Outdated drive in your system
 *   Extension of the file is renamed

## References ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/help/270139/prj-description-of-the-mpx-project-file-exchange-format)
