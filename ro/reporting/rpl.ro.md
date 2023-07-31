{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Aspect pagină raport",
  "keywords" :[ "rpl", "Aspect pagină raport", "XSD", "SQL Server", "raportare"],
  "description":"Aflați despre formatul de flux RPL, care este un format binar intern utilizat de Microsoft SQL Server Reporting Services atunci când contactați controalele vizualizatorului.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Ce este un fișier RPL? ##

Formatul de flux RPL (Report Page Layout) este un format binar intern utilizat de MS SQL Server Reporting Services atunci când contactează controalele vizualizatorului pentru a reduce o parte din munca de redare de la server la controlul vizualizatorului client. Dezvoltatorii pot crea designeri de rapoarte personalizați utilizând RPL, care va genera RPL, precum și redare de rapoarte personalizate care procesează și afișează fișierul RPL pentru a afișa rapoarte.

## Structuri RPL

Un flux RPL include structura fluxului, structura raportului, proprietățile raportului și enumerări. Fiecare structură include următoarele:

- O definiție a structurii.

- Gramatica Augmented Backus-Naur Form (ABNF) pentru structura.

- O diagramă de biți a structurii.

- Definițiile tuturor câmpurilor conținute în structura.

Iată scurtele note despre unele dintre structurile RPL:

### Structura fluxului
Structura fluxului constă dintr-o serie de înregistrări. O înregistrare conține zero sau mai multe câmpuri structurate care conțin aspectul raportului.

#### Flux RPL
Fluxul RPL trebuie să aibă o singură înregistrare Raport, iar fluxul trebuie să fie o serie de înregistrări binare care păstrează ierarhia raportului.

#### Record
Înregistrarea este un element de bază folosit pentru a păstra informațiile despre un raport. O înregistrare constă dintr-o secvență de octeți de lungime variabilă. O înregistrare constă din două componente:
- Un tip de înregistrare
- Datele de înregistrare care sunt specifice acelui tip de înregistrare.
Tipul de înregistrare este un octet care definește ce tip de informații este specificat de înregistrare și modul în care este ordonată și structurată structura datelor de înregistrare referitoare la înregistrare. Valoarea înregistrării depinde de tipul de date care sunt specifice acelei înregistrări.

#### Structuri simple de tip de date

Următorul tabel definește tipurile de date dintr-un flux RPL.

|Descriere| format|
---|---|
|Char|Reprezintă o valoare numerică (ordinală) de 16 biți (2 octeți).|
|Oct|Reprezintă un întreg fără semn de 8 biți (1 octet).|
|Int16|Reprezintă un număr întreg cu semn de 16 biți (2 octeți).|
|Single|Reprezintă o valoare în virgulă mobilă cu precizie unică de 32 de biți (4 octeți).|
|Decimal|Reprezintă un tip de date de 128 de biți (16 octeți).|
|DateTime|Reprezintă o codificare pe 64 de biți (8 octeți) a unei valori de dată și oră.|
|Int64|Reprezintă un număr întreg cu semn de 64 de biți (8 octeți).|
|Int32|Reprezintă un număr întreg cu semn de 32 de biți (4 octeți).|
|Float|Reprezintă o valoare în virgulă mobilă cu precizie unică de 32 de biți (4 octeți).|
|Boolean|Reprezintă o valoare de tip boolean logic de 8 biți (1 octet). Valorile valide sunt adevărate (1) și false (0).|
|Long|Reprezintă un număr întreg cu semn de 64 de biți (8 octeți).|
|Șir|Toate valorile String din protocol TREBUIE să fie UNICODE UTF-16. În mod implicit, toate valorile șirului încep cu un număr întreg care definește lungimea șirului. Valorile șirurilor sunt reprezentate în protocol ca o matrice de octeți; numărul de octeți TREBUIE să fie egal cu numărul de caractere din șir înmulțit cu doi.|

### Structuri de raportare
Structurile raportului includ definițiile și dimensiunile structurilor și elementelor lor relevante.

Următoarea listă specifică structurile raportului:

- Raportează
- Versiune
- Proprietăți raport
- Element de matrice offset
- Conținutul paginii
- Pagina
- Proprietățile paginii
- Aranjament în pagină
- Secțiune
- Secțiune simplă
- Sectiunea mixta
- Proprietăți secțiuni
- Elementul zonei corpului
- Element de antet de pagină
- Element de subsol al paginii
- Elementul corpului
- Proprietățile elementului
- Proprietăți element partajat
- Utilizați proprietățile elementului partajat
- InlineSharedElementProperties
- NonSharedElementProperties
- Stil
- SharedStyleProperties
- NonSharedStyleProperties
- Informații de acțiune
- ActionInfoContent
- Acțiune
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Linie
- Imagine
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Diagrama
- GaugePanel
- Hartă
- Dreptunghi
- Subraport
- RichTextBox
- ParagraphContent
- TextRun
- Paragraf
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
- Măsurătorile
- Măsurare
- ReportElementEnd

### Proprietăți
Mai jos este lista proprietăților care pot fi utilizate într-un flux RPL:

- ID
- Număr de coloane
- ColumnSpacing
- Nume unic
- Nume
- Eticheta
- Semn de carte
- Sfat instrument
- ToggleItem
- Descriere
- Locație
- ConsumeContainerWhiteSpace (RPL 10.6)
- Limba
- Timpul de execuție
- Autorul
- Reîmprospătare automată
- Nume Raport
- Înălțimea paginii
- Lățimea paginii
- MarginTop
- MarjaStânga
- MarjaDreapta
- MarginBottom
- Coloane
- Nume pagină (RPL 10.6)
- Slant
- Poate crește
- CanShrink
- Valoare
- ToggleState
- CanSort
- SortState
- Formulă
- IsToggleParent
- TypeCode
- Valoarea originală
- Este simplu
- ContentOffset
- StreamName
- Dimensiunea
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- ImageName
- Latime
- Înălţime
- Rezoluție orizontală
- Rezoluție verticală
- Format brut
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
- BorderStyleDreapta
- BorderStyleTop
- BorderStyleBottom
- Lățimea graniței
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- PaddingStânga
- PaddingDrept
- PaddingTop
- Umplutură de fund
- Stilul fontului
- Familie de fonturi
- Marimea fontului
- Grosimea fontului
- Format
- TextDecoration
- Aliniere text
- VerticalAlign
- Culoare
- Inaltimea liniei
- Direcția
- Modul de scriere
- UnicodeBiDi
- Imagine de fundal
- Culoare de fundal
- BackgroundRepeat
- NumeralLanguage
- NumeralVariant
- Calendar
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Nivel
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
- Prima linie
- Markup
- ContentTop
- ContentLeft
- ContentWidth
- ContentHeight
- Stat
- CellItemState
- MemberDefState

### Enumerări
Următoarea listă arată enumerările care pot fi utilizate în fluxul RPL:

- SortOptions
- Dimensiuni
- ShapeType
- ImageRawFormat
- FontStiluri
- FontWeights
- TextDecorations
- TextAlignments
- Alinieri verticale
- Directii
- Moduri de scriere
- UnicodeBiDiTypes
- Calendare
- BorderStyles
- BackgroundRepeatTypes
- ListStyles
- MarkupStyles
- TypeCode
- Valori de stat
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSize





## Referințe ##

- [Format de flux binar pentru aspectul paginii de raport (RPL)](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

