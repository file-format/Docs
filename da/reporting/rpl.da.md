{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL - Rapportsidelayout",
  "keywords": [
"rpl",
"Rapporter sidelayout",
"XSD",
"SQL Server",
"rapportering"
],
  "description": "Lær om RPL-streamformat, som er et internt binært format, der bruges af Microsoft SQL Server Reporting Services, når du kontakter seerkontroller.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-dal"
}
},
  "lastmod": "2021-03-02"
}

## Hvad er en RPL fil? ##

RPL-streamformatet (Report Page Layout) er et internt binært format, der bruges af MS SQL Server Reporting Services, når man kontakter fremviserkontroller for at reducere noget af gengivelsesarbejdet fra serveren til klientfremviserkontrollen. Udviklere kan oprette brugerdefinerede rapportdesignere ved at bruge RPL, der genererer RPL såvel som tilpassede rapportrenderere, der behandler og viser RPL-filen for at vise rapporter.

## RPL strukturer

En RPL-strøm inkluderer strømstruktur, rapportstruktur, rapportegenskaber og opregninger. Hver struktur inkluderer følgende:

- En definition af strukturen.

- Den Augmented Backus-Naur Form (ABNF) grammatik for strukturen.

- Et bitdiagram af strukturen.

- Definitioner af alle felter indeholdt i strukturen.

Her er de korte bemærkninger om nogle af RPL-strukturerne:

### Strømstruktur
Strømstrukturen består af en række poster. En post indeholder nul eller flere strukturerede felter, der indeholder rapportlayoutet.

#### RPL Stream
RPL-strømmen skal kun have én rapportpost, og strømmen skal være en række binære poster, der bevarer rapporthierarkiet.

#### Optag
Posten er en grundlæggende byggesten, der bruges til at opbevare oplysningerne om en rapport. En post består af en sekvens af bytes af varierende længde. En post består af to komponenter:
- En rekordtype
- De registreringsdata, der er specifikke for den pågældende posttype.
Posttypen er én byte, der definerer, hvilken type information der er specificeret af posten, og hvordan strukturen af postdataene vedrørende posten er ordnet og struktureret. Registreringsværdien afhænger af den type data, der er specifik for den pågældende post.

#### Simple datatypestrukturer

Følgende tabel definerer datatyperne i en RPL-strøm.

|Beskrivelse| format|
---|---|
|Char|Repræsenterer en 16-bit (2-byte) numerisk (ordinal) værdi.|
|Byte|Repræsenterer et 8-bit (1-byte) heltal uden fortegn.|
|Int16|Repræsenterer et 16-bit (2-byte) heltal med fortegn.|
|Enkelt|Repræsenterer en 32-bit (4-byte) enkeltpræcision flydende kommaværdi.|
|Decimal|Repræsenterer en 128-bit (16-byte) datatype.|
|DatoTid|Repræsenterer en 64-bit (8-byte) kodning af en dato- og tidsværdi.|
|Int64|Repræsenterer et 64-bit (8-byte) fortegnet heltal.|
|Int32|Repræsenterer et 32-bit (4-byte) fortegnet heltal.|
|Float|Repræsenterer en 32-bit (4-byte) enkeltpræcision flydende kommaværdi.|
|Boolean|Repræsenterer en 8-bit (1-byte) logisk boolesk typeværdi. De gyldige værdier er sande (1) og falske (0).|
|Lang|Repræsenterer et 64-bit (8-byte) fortegnet heltal.|
|String|All String values within the protocol MUST be UNICODE UTF-16. Som standard starter alle strengværdier med et heltal, der definerer længden af strengen. Strengværdier er repræsenteret i protokollen som et array af bytes; antallet af bytes SKAL være lig med antallet af tegn i strengen ganget med to.|

### Rapportstrukturer
Rapportstrukturerne omfatter definitioner og størrelser af deres relevante strukturer og elementer.

Følgende liste specificerer rapportstrukturerne:

- Rapport
- Version
- Rapportegenskaber
- Offset Array Element
- Sideindhold
- Side
- Sideegenskaber
- Sidelayout
- Afsnit
- Enkelt afsnit
- Blandet afsnit
- Sektionsegenskaber
- Body Area Element
- Sidehovedelement
- Sidefodelement
- Kropselement
- Elementegenskaber
- Delte elementegenskaber
- Brug egenskaber for delt element
- InlineSharedElementProperties
- NonSharedElementProperties
- Stil
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- Handling
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Linje
- Billede
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Diagram
- Målepanel
- Kort
- Rektangel
- Underrapport
- RichTextBox
- Afsnitindhold
- TextRun
- Afsnit
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- Kolonnebredder
- Kolonneinfo
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
- Mål
- Måling
- ReportElementEnd

### Ejendomme
Følgende er listen over egenskaber, der kan bruges i en RPL Stream:

- ID
- ColumnCount
- ColumnSpacing
- Unikt Navn
- Navn
- Etiket
- Bogmærke
- Værktøjstip
- ToggleItem
- Beskrivelse
- Beliggenhed
- ConsumeContainerWhiteSpace (RPL 10.6)
- Sprog
- Udførelsestid
- Forfatter
- AutoRefresh
- Rapportnavn
- Sidehøjde
- Sidebredde
- MarginTop
- Margin Venstre
- MarginHøjre
- MarginBund
- Kolonner
- Sidenavn (RPL 10.6)
- Skrå
- CanGrow
- CanShrink
- Værdi
- ToggleState
- KanSortere
- SortState
- Formel
- IsToggleParent
- Typekode
- Originalværdi
- Er Enkel
- ContentOffset
- Strømnavn
- Størrelse
- LinkToChild
- Udskriv På FørsteSide
- PrintBetweenSections (RPL 10.4)
- Formateret værdiudtryksbaseret
- ProcessedWithError
- ImageMIMEType
- Billednavn
- Bredde
- Højde
- Horisontal opløsning
- Vertikal opløsning
- RawFormat
- Hyperlink
- BogmærkeLink
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
- Polstring til venstre
- Polstring Højre
- Polstring Top
- PaddingBund
- Skrifttype
- FontFamily
- Skriftstørrelse
- Skrifttypevægt
- Format
- Tekstdekoration
- Tekstjustering
- VerticalAlign
- Farve
- Linjehøjde
- Retning
- Skrivetilstand
- UnicodeBiDi
- Baggrundsbillede
- Baggrundsfarve
- Gentag baggrund
- NumeralLanguage
- NumeralVariant
- Kalender
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- Layoutretning
- DefinitionPath
- Niveau
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- ColumnIndex
- Rækkeindeks
- GroupLabel
- RecursiveToggleLevel
- Listestil
- Listeniveau
- Afsnitnummer
- Højre indrykning
- Venstreindrykning
- Hængende Indryk
- SpaceBefore
- SpaceAfter
- Første linje
- Markup
- ContentTop
- Indhold til venstre
- Indholdsbredde
- Indholdshøjde
- Stat
- CellItemState
- Medlemsstat

### Optællinger
Følgende liste viser de opregninger, der kan bruges i RPL-strømmen:

- SortOptions
- Størrelser
- ShapeType
- ImageRawFormat
- FontStyles
- Fontvægte
- Tekstdekorationer
- Tekstjusteringer
- Vertical Alignments
- Vejbeskrivelse
- Skrivetilstande
- UnicodeBiDiTypes
- Kalendere
- BorderStyles
- BackgroundRepeatTypes
- Listestile
- MarkupStyles
- Typekode
- Statsværdier
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLS størrelse





## Referencer ##

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

