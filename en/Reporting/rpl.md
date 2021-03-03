{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "RPL - Report Page Layout",
  "keywords" : [ "rpl", "Report Page Layout", "XSD", "SQL Server", "reporting"],
  "description":"Learn about RPL stream format which is an internal binary format used by Microsoft SQL Server Reporting Services when contacting with viewer controls.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "Reporting"
    }
  },
  "lastmod" : "2021-03-02"
}

## What is an RPL file? ##

The RPL (Report Page Layout) stream format is an internal binary format used by MS SQL Server Reporting Services when contacting with viewer controls to reduce some of the rendering work from the server to the client viewer control. Developrers can create custom report designers by using RPL, that will generate RPL as well as custom report renderers that process and display the RPL file to display reports.

## RPL Structures

An RPL stream includes stream structure, report structure, report properties, and enumerations. Every structure include the following:

- A definition of the structure.

- The Augmented Backus-Naur Form (ABNF) grammar for the structure.

- A bit diagram of the structure.

- Definitions of all fields contained within the structure.

Here are the brief notes about some of the RPL Structures:

### Stream Structure
The stream structure consists of a series of records. A record contains zero or more structured fields that contain the report layout.

#### RPL Stream
The RPL stream must have just one Report record and the stream must be a series of binary records that keep the report hierarchy.

#### Record
The record is a basic building block used to keep the information about a report. A record consists of a varying-length sequence of bytes. A record consists of two components: 
- A record type 
- The record data that is specific to that record type.
The record type is one byte that defines what type of information is specified by the record and how the structure of the record data concerning to the record is ordered and structured. The record value is dependent on the type of data that is particular to that record.

#### Simple Data Type Structures

The following table defines the data types in an RPL stream.

|Description| format|
---|---|
|Char|Represents a 16-bit (2-byte) numeric (ordinal) value.|
|Byte|Represents a 8-bit (1-byte) unsigned integer.|
|Int16|Represents a 16-bit (2-byte) signed integer.|
|Single|Represents a 32-bit (4-byte) single-precision floating point value.|
|Decimal|Represents a 128-bit (16-byte) data type.|
|DateTime|Represents a 64-bit (8-byte) encoding of a date and time value.|
|Int64|Represents a 64-bit (8-byte) signed integer.|
|Int32|Represents a 32-bit (4-byte) signed integer.|
|Float|Represents a 32-bit (4-byte) single-precision floating point value.|
|Boolean|Represents an 8-bit (1-byte) logical Boolean type value. The valid values are true (1) and false (0).|
|Long|Represents a 64-bit (8-byte) signed integer.|
|String|All String values within the protocol MUST be UNICODE UTF-16. By default, all String values start with an integer that defines the length of the String. String values are represented in the protocol as an array of bytes; the number of bytes MUST be equal to the number of characters in the String multiplied by two.|

### Report Structures
 The report structures include the definitions and sizes of their relevant structures and elements.
 
 Following list specifies the report structures:
 
- Report
- Version
- Report Properties
- Offset Array Element
- Page Content
- Page
- Page properties
- Page Layout
- Section
- Simple Section
- Mixed Section
- Section Properties
- Body Area Element
- Page Header Element
- Page Footer Element
- Body Element
- Element Properties
- Shared Element Properties
- Use Shared Element Properties
- InlineSharedElementProperties
- NonSharedElementProperties
- Style
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- Action
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Line
- Image
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Chart
- GaugePanel
- Map
- Rectangle
- SubReport
- RichTextBox
- ParagraphContent
- TextRun
- Paragraph
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- ColumnsWidths
- ColumnInfo
- RowHeights
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Measurements
- Measurement
- ReportElementEnd

### Properties
Following is the list of properties that can be used in an RPL Stream:

- ID
- ColumnCount
- ColumnSpacing
- UniqueName
- Name
- Label
- Bookmark
- ToolTip
- ToggleItem
- Description
- Location
- ConsumeContainerWhiteSpace (RPL 10.6)
- Language
- ExecutionTime
- Author
- AutoRefresh
- ReportName
- PageHeight
- PageWidth
- MarginTop
- MarginLeft
- MarginRight
- MarginBottom
- Columns
- PageName (RPL 10.6)
- Slant
- CanGrow
- CanShrink
- Value
- ToggleState
- CanSort
- SortState
- Formula
- IsToggleParent
- TypeCode
- OriginalValue
- IsSimple
- ContentOffset
- StreamName
- Sizing
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- ImageName
- Width
- Height
- HorizontalResolution
- VerticalResolution
- RawFormat
- Hyperlink
- BookmarkLink
- DrillthroughId
- DrillthroughUrl
- BorderColor
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- BorderWidth
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingRight
- PaddingTop
- PaddingBottom
- FontStyle
- FontFamily
- FontSize
- FontWeight
- Format
- TextDecoration
- TextAlign
- VerticalAlign
- Color
- LineHeight
- Direction
- WritingMode
- UnicodeBiDi
- BackgroundImage
- BackgroundColor
- BackgroundRepeat
- NumeralLanguage
- NumeralVariant
- Calendar
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Level
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- ColumnIndex
- RowIndex
- GroupLabel
- RecursiveToggleLevel
- ListStyle
- ListLevel
- ParagraphNumber
- RightIndent
- LeftIndent
- HangingIndent
- SpaceBefore
- SpaceAfter
- FirstLine
- Markup
- ContentTop
- ContentLeft
- ContentWidth
- ContentHeight
- State
- CellItemState
- MemberDefState

### Enumerations
Following list shows the enumerations that can be used in the RPL stream:

- SortOptions
- Sizings
- ShapeType
- ImageRawFormat
- FontStyles
- FontWeights
- TextDecorations
- TextAlignments
- VerticalAlignments
- Directions
- WritingModes
- UnicodeBiDiTypes
- Calendars
- BorderStyles
- BackgroundRepeatTypes
- ListStyles
- MarkupStyles
- TypeCode
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSize
 




## References ##

- [Report Page Layout (RPL) Binary Stream Format](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

