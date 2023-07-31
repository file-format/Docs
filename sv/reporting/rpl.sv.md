{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - rapportsidalayout",
  "keywords" :[ "rpl", "Rapportera sidlayout", "XSD", "SQL-server", "rapportering"],
  "description":"Läs mer om RPL-strömformat som är ett internt binärt format som används av Microsoft SQL Server Reporting Services vid kontakt med tittarkontroller.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Vad är en RPL fil? ##

Strömformatet RPL (Report Page Layout) är ett internt binärt format som används av MS SQL Server Reporting Services vid kontakt med visningskontroller för att minska en del av renderingsarbetet från servern till klientvisningskontrollen. Utvecklare kan skapa anpassade rapportdesigners genom att använda RPL, som genererar RPL såväl som anpassade rapportrenderare som bearbetar och visar RPL-filen för att visa rapporter.

## RPL-strukturer

En RPL-ström inkluderar strömstruktur, rapportstruktur, rapportegenskaper och uppräkningar. Varje struktur inkluderar följande:

- En definition av strukturen.

- Den Augmented Backus-Naur Form (ABNF) grammatiken för strukturen.

– Ett bitdiagram över strukturen.

- Definitioner av alla fält som finns i strukturen.

Här är de korta anteckningarna om några av RPL-strukturerna:

### Strömningsstruktur
Strömstrukturen består av en serie poster. En post innehåller noll eller fler strukturerade fält som innehåller rapportlayouten.

#### RPL Stream
RPL-strömmen måste bara ha en rapportpost och strömmen måste vara en serie binära poster som håller rapporthierarkin.

#### Spela in
Posten är en grundläggande byggsten som används för att behålla informationen om en rapport. En post består av en sekvens av bytes med varierande längd. En post består av två komponenter:
– En rekordtyp
- Den postdata som är specifik för den posttypen.
Posttypen är en byte som definierar vilken typ av information som specificeras av posten och hur strukturen på postdata som rör posten är ordnad och strukturerad. Postvärdet beror på vilken typ av data som är specifik för den posten.

#### Enkla datatypstrukturer

Följande tabell definierar datatyperna i en RPL-ström.

|Beskrivning| format|
---|---|
|Tecken|Representerar ett 16-bitars (2-byte) numeriskt (ordinalt) värde.|
|Byte|Representerar ett 8-bitars (1-byte) heltal utan tecken.|
|Int16|Representerar ett 16-bitars (2-byte) heltal med tecken.|
|Enkel|Representerar ett 32-bitars (4-byte) flyttalsvärde med enkel precision.|
|Decimal|Representerar en 128-bitars (16-byte) datatyp.|
|DateTime|Representerar en 64-bitars (8-byte) kodning av ett datum- och tidsvärde.|
|Int64|Representerar ett 64-bitars (8-byte) heltal med tecken.|
|Int32|Representerar ett 32-bitars (4-byte) heltal med tecken.|
|Float|Representerar ett 32-bitars (4-byte) flyttalsvärde med enkel precision.|
|Boolean|Representerar ett 8-bitars (1-byte) logiskt booleskt värde. De giltiga värdena är sant (1) och falskt (0).|
|Lång|Representerar ett 64-bitars (8-byte) signerat heltal.|
|String|Alla strängvärden inom protokollet MÅSTE vara UNICODE UTF-16. Som standard börjar alla strängvärden med ett heltal som definierar längden på strängen. Strängvärden representeras i protokollet som en array av byte; antalet byte MÅSTE vara lika med antalet tecken i strängen multiplicerat med två.|

### Rapportstrukturer
Rapportstrukturerna inkluderar definitioner och storlekar på deras relevanta strukturer och element.

Följande lista specificerar rapportstrukturerna:

- Rapportera
- Version
- Rapportera egenskaper
- Offset Array Element
- Sidinnehåll
- Sida
- Sidegenskaper
- Sidlayout
- Sektion
- Enkelt avsnitt
- Blandad avdelning
- Avsnittsegenskaper
- Body Area Element
- Sidhuvudelement
- Sidsidfotselement
- Body Element
- Elementegenskaper
- Delade elementegenskaper
- Använd egenskaper för delade element
- InlineSharedElementProperties
- NonSharedElementProperties
- Stil
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
- Linje
- Bild
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Diagram
- GaugePanel
- Karta
- Rektangel
- Delrapport
- RichTextBox
- ParagraphContent
- TextRun
- Paragraf
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- Kolumnbredder
- KolumnInfo
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
- Mått
- Mätning
- ReportElementEnd

### Egenskaper
Följande är listan över egenskaper som kan användas i en RPL Stream:

- ID
- ColumnCount
- Kolumnavstånd
- Unikt namn
- Namn
- Etikett
- Bokmärke
- Verktygstips
- ToggleItem
- Beskrivning
- Plats
- ConsumeContainerWhiteSpace (RPL 10.6)
- Språk
- ExecutionTime
- Författare
- Automatisk omladdning
- Rapportnamn
- Sidhöjd
- Sidbredd
- MarginTop
- Marginal Vänster
- MarginRight
- MarginBottom
- Kolumner
- Sidnamn (RPL 10.6)
- Sned
- Kan växa
- CanShrink
- Värde
- ToggleState
- KanSortera
- SortState
- Formel
- IsToggleParent
- Typkod
- Originalvärde
- Det är enkelt
- ContentOffset
- Strömnamn
- Storlek
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Bildnamn
- Bredd
- Höjd
- Horisontell upplösning
- Vertikal upplösning
- RawFormat
- Hyperlänk
- BookmarkLink
- DrillthroughId
- DrillthroughUrl
- Gräns färg
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Gränsbredd
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- Vaddering Vänster
- VadderingRätt
- PaddingTop
- PaddingBottom
- Typsnitt
- Typsnittsfamilj
- Textstorlek
- FontWeight
- Format
- Textdekoration
- TextAlign
- VerticalAlign
- Färg
- Radavstånd
- Riktning
- Skrivläge
- UnicodeBiDi
- Bakgrundsbild
- Bakgrundsfärg
- BackgroundRepeat
- NumeralLanguage
- NumeralVariant
- Kalender
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Nivå
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- ColumnIndex
- RowIndex
- GroupLabel
- RecursiveToggleLevel
- Liststil
- Listnivå
- ParagraphNumber
- HögerIndrag
- VänsterIndrag
- Hängande indrag
- SpaceBefore
- SpaceAfter
- Första linjen
- Markup
- ContentTop
- Innehåll vänster
- ContentWidth
- ContentHeight
- Stat
- CellItemState
- MemberDefState

### Uppräkningar
Följande lista visar uppräkningarna som kan användas i RPL-strömmen:

- SortOptions
- Storlekar
- ShapeType
- ImageRawFormat
- FontStyles
- FontWeights
- Textdekorationer
- Textjusteringar
- VerticalAlignments
- Vägbeskrivning
- Skrivlägen
- UnicodeBiDiTypes
- Kalendrar
- BorderStyles
- BackgroundRepeatTypes
- Liststilar
- MarkupStyles
- Typkod
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLS-storlek





## Referenser ##

- [Rapport Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

