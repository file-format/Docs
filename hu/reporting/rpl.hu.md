{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL – Jelentés oldalelrendezése",
  "keywords" :[ "rpl", "Report Page Layout", "XSD", "SQL Server", "reporting"],
  "description":"További információ az RPL adatfolyam-formátumról, amely egy belső bináris formátum, amelyet a Microsoft SQL Server Reporting Services használ a megjelenítői vezérlőkkel való kapcsolatfelvételkor.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Mi az RPL fájl? ##

Az RPL (Report Page Layout) adatfolyam-formátum egy belső bináris formátum, amelyet az MS SQL Server Reporting Services használ, amikor kapcsolatba lép a megjelenítői vezérlőkkel, hogy csökkentse a kiszolgálóról az ügyfélmegjelenítő vezérlőjére irányuló megjelenítési munkát. A fejlesztők az RPL használatával egyéni jelentéstervezőket hozhatnak létre, amelyek RPL-t, valamint egyéni jelentéskészítőket generálnak, amelyek feldolgozzák és megjelenítik az RPL fájlt a jelentések megjelenítéséhez.

## RPL struktúrák

Az RPL adatfolyam folyamstruktúrát, jelentésstruktúrát, jelentéstulajdonságokat és felsorolásokat tartalmaz. Minden szerkezet a következőket tartalmazza:

- A szerkezet meghatározása.

- Az kiterjesztett Backus-Naur Form (ABNF) nyelvtan a szerkezethez.

- Egy kis diagram a szerkezetről.

- A szerkezetben található összes mező meghatározása.

Íme a rövid megjegyzések néhány RPL-struktúrával kapcsolatban:

### Az adatfolyam szerkezete
Az adatfolyam szerkezete rekordok sorozatából áll. Egy rekord nulla vagy több olyan strukturált mezőt tartalmaz, amely tartalmazza a jelentés elrendezését.

#### RPL Stream
Az RPL adatfolyamnak csak egy jelentésrekordnak kell lennie, és az adatfolyamnak bináris rekordok sorozatának kell lennie, amelyek megtartják a jelentéshierarchiát.

#### Felvétel
A rekord egy alapvető építőelem, amely a jelentéssel kapcsolatos információk tárolására szolgál. A rekord változó hosszúságú bájtsorozatból áll. Egy rekord két összetevőből áll:
- Egy rekord típus
- Az adott rekordtípusra jellemző rekordadatok.
A rekordtípus egy bájt, amely meghatározza, hogy a rekord milyen típusú információkat ad meg, és hogyan rendeződik és strukturálja a rekordra vonatkozó rekordadatok szerkezetét. A rekord értéke az adott rekordra jellemző adattípustól függ.

#### Egyszerű adattípus-struktúrák

Az alábbi táblázat az RPL adatfolyam adattípusait határozza meg.

|Leírás| formátum|
---|---|
|Char|16 bites (2 bájtos) numerikus (sorrendi) értéket jelent.|
|Bájt|Egy 8 bites (1 bájtos) előjel nélküli egész számot jelent.|
|Int16|16 bites (2 bájtos) előjeles egész számot jelent.|
|Single|Egy 32 bites (4 bájtos) egypontos lebegőpontos értéket jelent.|
|Tizedes|128 bites (16 bájtos) adattípust jelent.|
|DateTime|A dátum és időérték 64 bites (8 bájtos) kódolása.|
|Int64|Egy 64 bites (8 bájtos) előjeles egész számot jelent.|
|Int32|Egy 32 bites (4 bájtos) előjeles egész számot jelent.|
|Float|Egy 32 bites (4 bájtos) egypontos lebegőpontos értéket jelent.|
|Boolean|Egy 8 bites (1 bájtos) logikai logikai típusú értéket jelent. Az érvényes értékek igaz (1) és false (0).|
|Long|Egy 64 bites (8 bájtos) előjeles egész számot jelent.|
|String|A protokollon belüli összes karakterlánc-értéknek UNICODE UTF-16-nak KELL lennie. Alapértelmezés szerint minden karakterlánc érték egy egész számmal kezdődik, amely meghatározza a karakterlánc hosszát. A karakterlánc-értékek a protokollban bájtok tömbjeként jelennek meg; a bájtok számának meg KELL egyeznie a String karaktereinek számával szorozva kettővel.|

### Jelentésstruktúrák
A jelentésstruktúrák tartalmazzák a releváns struktúráik és elemeik definícióit és méretét.

A következő lista határozza meg a jelentés szerkezetét:

- Jelentés
- Verzió
- Jelentés tulajdonságai
- Offset tömb elem
- Oldal tartalma
- Oldal
- Oldal tulajdonságai
- Oldal elrendezés
- Szakasz
- Egyszerű szakasz
- Vegyes szekció
- Szakasz tulajdonságai
- Testfelület elem
- Oldalfejléc elem
- Oldallábléc elem
- Test elem
- Elem tulajdonságai
- Megosztott elem tulajdonságai
- Használja a Megosztott elem tulajdonságait
- InlineSharedElementProperties
- NonSharedElementProperties
- Stílus
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- Akció
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- Jelentéstétel
- Vonal
- Kép
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Diagram
- GaugePanel
- Térkép
- Téglalap
- Aljelentés
- RichTextBox
- BekezdésTartalom
- TextRun
- Bekezdés
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
- Mérések
- Mérés
- ReportElementEnd

### Tulajdonságok
Az alábbiakban az RPL adatfolyamban használható tulajdonságok listája található:

- Azonosító
- Oszlopszám
- Oszlopköz
- Egyedi név
- Név
- Címke
- Könyvjelző
- Eszköztipp
- ToggleItem
- Leírás
- Helyszín
- ConsumeContainerWhiteSpace (RPL 10.6)
- Nyelv
- Végrehajtási idő
- Szerző
- Automatikus frissítés
- ReportName
- Oldalmagasság
- Oldalszélesség
- MarginTop
- MarginLeft
- MarginRight
- MarginBottom
- Oszlopok
- Oldalnév (RPL 10.6)
- Ferde
- CanGrow
- CanShrink
- Érték
- ToggleState
- CanSort
- SortState
- Képlet
- IsToggleParent
- TypeCode
- Original Value
- Egyszerű
- Tartalomeltolás
- StreamName
- Méretezés
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Képnév
- Szélesség
- Magasság
- Vízszintes felbontás
- Függőleges felbontás
- RawFormat
- Hiperhivatkozás
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
- Betű stílus
- Betűtípus család
- Betűméret
- FontWeight
- Formátum
- TextDecoration
- Szöveg igazítás
- VerticalAlign
- Színes
- Vonalmagasság
- Irány
- Írásmód
- UnicodeBiDi
- Háttérkép
- Háttérszín
- Háttérismétlés
- NumeralLanguage
- NumeralVariant
- Naptár
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Szint
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
- Paragrafusszám
- RightIndent
- LeftIndent
- Függőleges behúzás
- SpaceBefore
- SpaceAfter
- Első sor
- Jelölés
- ContentTop
- Tartalom Bal
- ContentWidth
- Tartalom Magasság
- Állapot
- CellItemState
- MemberDefState

### Felsorolások
Az alábbi lista az RPL adatfolyamban használható felsorolásokat mutatja be:

- Rendezési beállítások
- Méretek
- ShapeType
- ImageRawFormat
- Betűstílusok
- FontWeights
- TextDecorations
- TextAlignments
- VerticalAlignments
- Útvonal
- Írási módok
- UnicodeBiDiTypes
- Naptárak
- BorderStyles
- BackgroundRepeatTypes
- ListStyles
- MarkupStyles
- TypeCode
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLS méret





## Referenciák ##

- [Report Page Layout (RPL) bináris adatfolyam-formátum](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

