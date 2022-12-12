{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Rozvržení stránky sestavy",
  "keywords" :[ "rpl", "Rozvržení stránky sestavy", "XSD", "SQL Server", "reporting"],
  "description":"Další informace o formátu streamu RPL, což je interní binární formát používaný službou Microsoft SQL Server Reporting Services při kontaktu s ovládacími prvky prohlížeče.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Co je soubor RPL? ##

Formát datového proudu RPL (Report Page Layout) je interní binární formát používaný službou MS SQL Server Reporting Services při kontaktu s ovládacími prvky prohlížeče, aby se snížila část vykreslovací práce ze serveru na ovládací prvek prohlížeče klienta. Vývojáři mohou vytvářet vlastní návrháře sestav pomocí RPL, které budou generovat RPL, stejně jako vlastní vykreslovače sestav, které zpracují a zobrazí soubor RPL pro zobrazení sestav.

## RPL struktury

Datový proud RPL zahrnuje strukturu toku, strukturu sestavy, vlastnosti sestavy a výčty. Každá struktura obsahuje následující:

- Definice struktury.

- Gramatika rozšířeného Backus-Naur Form (ABNF) struktury.

- Bitové schéma struktury.

- Definice všech polí obsažených ve struktuře.

Zde jsou krátké poznámky o některých strukturách RPL:

### Struktura streamu
Struktura proudu se skládá z řady záznamů. Záznam obsahuje nula nebo více strukturovaných polí, která obsahují rozvržení sestavy.

#### Stream RPL
Datový proud RPL musí mít pouze jeden záznam sestavy a datový proud musí být řadou binárních záznamů, které udržují hierarchii sestav.

#### Záznam
Záznam je základním stavebním kamenem používaným k uchování informací o zprávě. Záznam se skládá z různě dlouhé sekvence bajtů. Záznam se skládá ze dvou částí:
- Typ záznamu
- Data záznamu, která jsou specifická pro daný typ záznamu.
Typ záznamu je jeden bajt, který definuje, jaký typ informací je specifikován záznamem a jak je uspořádána a strukturována struktura dat záznamu týkajících se záznamu. Hodnota záznamu závisí na typu dat, která jsou pro daný záznam konkrétní.

#### Jednoduché struktury datových typů

Následující tabulka definuje datové typy v proudu RPL.

|Popis| formát|
---|---|
|Char|Představuje 16bitovou (2bajtovou) číselnou (ordinální) hodnotu.|
|Byte|Představuje 8bitové (1bajtové) celé číslo bez znaménka.|
|Int16|Představuje 16bitové (2bajtové) celé číslo se znaménkem.|
|Single|Představuje 32bitovou (4bajtovou) hodnotu s plovoucí desetinnou čárkou s jednoduchou přesností.|
|Decimal|Představuje 128bitový (16bajtový) datový typ.|
|DateTime|Představuje 64bitové (8bajtové) kódování hodnoty data a času.|
|Int64|Představuje 64bitové (8bajtové) celé číslo se znaménkem.|
|Int32|Představuje 32bitové (4bajtové) celé číslo se znaménkem.|
|Float|Představuje 32bitovou (4bajtovou) hodnotu s plovoucí desetinnou čárkou s jednoduchou přesností.|
|Boolean|Představuje 8bitovou (1bajtovou) logickou hodnotu typu Boolean. Platné hodnoty jsou true (1) a false (0).|
|Long|Představuje 64bitové (8bajtové) celé číslo se znaménkem.|
|String|Všechny hodnoty řetězce v rámci protokolu MUSÍ být UNICODE UTF-16. Ve výchozím nastavení začínají všechny hodnoty řetězce celým číslem, které definuje délku řetězce. Hodnoty řetězce jsou v protokolu reprezentovány jako pole bajtů; počet bajtů MUSÍ být roven počtu znaků v řetězci vynásobeném dvěma.|

### Struktury přehledů
Struktury zpráv zahrnují definice a velikosti příslušných struktur a prvků.

Následující seznam specifikuje struktury sestav:

- Zpráva
- Verze
- Vlastnosti sestavy
- Offset Array Element
- Obsah stránky
- Stránka
- Vlastnosti stránky
- Rozvržení stránky
- Sekce
- Jednoduchá sekce
- Smíšená sekce
- Vlastnosti sekce
- Prvek oblasti těla
- Prvek záhlaví stránky
- Prvek zápatí stránky
- Element těla
- Vlastnosti prvku
- Vlastnosti sdílených prvků
- Použijte sdílené vlastnosti prvku
- InlineSharedElementProperties
- NonSharedElementProperties
- Styl
- SharedStyleProperties
- NonSharedStyleProperties
- Informace o akci
- ActionInfoContent
- Akce
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Linka
- Obraz
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Graf
- Měřicí panel
- Mapa
- Obdélník
- Dílčí zpráva
- RichTextBox
- Obsah odstavce
- TextRun
- Odstavec
- RichTextBoxStructure
- Tablix
- Obsah Tablix
- TablixStructure
- TablixMeasurements
- ColumnsWidths
- Informace o sloupcích
- RowHeights
- Informace o řádcích
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
- Měření
- Měření
- ReportElementEnd

### Vlastnosti
Níže je uveden seznam vlastností, které lze použít v RPL streamu:

- ID
- ColumnCount
- ColumnSpacing
- Jedinečné jméno
- Název
- Štítek
- Záložka do knihy
- ToolTip
- ToggleItem
- Popis
- Umístění
– ConsumeContainerWhiteSpace (RPL 10.6)
- Jazyk
- Doba provedení
- Autor
- Automatické obnovení
- Název sestavy
- Výška stránky
- Šířka stránky
- Horní okraj
- Okraj vlevo
- Okraj vpravo
- MarginBottom
- Sloupce
– Název stránky (RPL 10.6)
- Šikmý
- CanGrow
- CanShrink
- Hodnota
- ToggleState
- CanSort
- SortState
- Vzorec
- IsToggleParent
- TypeCode
- Původní hodnota
- Je to jednoduché
- ContentOffset
- Název proudu
- Velikost
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMETtype
- Název obrázku
- Šířka
- Výška
- Horizontální rozlišení
- Vertikální rozlišení
- RawFormat
- Hypertextový odkaz
- Odkaz na záložku
- DrillthroughId
- DrillthroughUrl
- Barva ohraničení
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Šířka okraje
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingRight
- Polstrování
- PaddingBottom
- Styl fontu
- FontFamily
- Velikost písma
- Hmotnost písma
- Formát
- TextDecoration
- Zarovnání textu
- VerticalAlign
- Barva
- Výška čáry
- Směr
- Režim psaní
- UnicodeBiDi
- Obrázek na pozadí
- Barva pozadí
- Opakování pozadí
- Číselný jazyk
- NumeralVariant
- Kalendář
- ColumnHeaderRows
-RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- Definice Cesta
- Úroveň
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
- Číslo odstavce
- RightIndent
- LeftIndent
- HangingIndent
- SpaceBefore
- SpaceAfter
- První řada
- Označení
- ContentTop
- ContentLeft
- ContentWidth
- ContentHeight
- Stát
- CellItemState
- MemberDefState

### Výčty
Následující seznam ukazuje výčty, které lze použít v proudu RPL:

- Možnosti řazení
- Rozměry
- Typ tvaru
- ImageRawFormat
- Styly písma
- Hmotnosti písem
- Textové dekorace
- Zarovnání textu
- Vertikální zarovnání
- Pokyny
- Režimy psaní
- UnicodeBiDiTypes
- Kalendáře
- Styly okrajů
- BackgroundRepeatTypes
- Seznam stylů
- Styly značek
- TypeCode
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- Velikost RPLS





## Reference ##

- [Formát binárního streamu sestavy rozvržení stránky (RPL)](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

