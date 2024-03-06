{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL — Pārskata lapas izkārtojums",
  "keywords": [
"rpl",
"Pārskata lapas izkārtojums",
"XSD",
"SQL serveris",
"ziņošana"
],
  "description": "Uzziniet par RPL straumes formātu, kas ir iekšējs binārais formāts, ko izmanto Microsoft SQL Server Reporting Services, sazinoties ar skatītāja vadīklām.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-lvl"
}
},
  "lastmod": "2021-03-02"
}

## Kas ir RPL fails? ##

RPL (Report Page Layout) straumes formāts ir iekšējs binārais formāts, ko izmanto MS SQL Server Reporting Services, sazinoties ar skatītāja vadīklām, lai samazinātu daļu renderēšanas darba no servera uz klienta skatītāja vadīklu. Izstrādātāji var izveidot pielāgotus atskaišu noformētājus, izmantojot RPL, kas ģenerēs RPL, kā arī pielāgotus atskaišu renderētājus, kas apstrādā un parāda RPL failu, lai parādītu atskaites.

## RPL struktūras

RPL straumē ir iekļauta straumes struktūra, atskaites struktūra, atskaites rekvizīti un uzskaitījumi. Katra struktūra ietver šādus elementus:

- Struktūras definīcija.

- Augmented Backus-Naur Form (ABNF) gramatika struktūrai.

- Maza struktūras diagramma.

- visu struktūrā ietverto lauku definīcijas.

Šeit ir īsas piezīmes par dažām RPL struktūrām:

### Straumes struktūra
Straumes struktūra sastāv no ierakstu sērijas. Ierakstā ir nulle vai vairāk strukturētu lauku, kas satur pārskata izkārtojumu.

#### RPL straume
RPL straumē ir jābūt tikai vienam pārskata ierakstam, un straumei ir jābūt bināro ierakstu sērijai, kas saglabā pārskatu hierarhiju.

#### Ieraksts
Ieraksts ir pamatelements, ko izmanto, lai saglabātu informāciju par ziņojumu. Ieraksts sastāv no dažāda garuma baitu secības. Ieraksts sastāv no diviem komponentiem:
- Ieraksta veids
- ieraksta dati, kas ir raksturīgi šim ieraksta veidam.
Ieraksta tips ir viens baits, kas nosaka, kāda veida informācija ir norādīta ierakstā un kā tiek sakārtota un strukturēta ar ierakstu saistīto ieraksta datu struktūra. Ieraksta vērtība ir atkarīga no datu veida, kas ir īpaši šim ierakstam.

#### Vienkāršas datu tipu struktūras

Šajā tabulā ir definēti datu veidi RPL straumē.

|Apraksts| formāts|
---|---|
|Char|Apzīmē 16 bitu (2 baitu) skaitlisko (kārtas) vērtību.|
|Baits|Apzīmē 8 bitu (1 baita) neparakstītu veselu skaitli.|
|Int16|Apzīmē 16 bitu (2 baitu) veselu skaitli.|
|Single|Apzīmē 32 bitu (4 baitu) vienas precizitātes peldošā komata vērtību.|
|Decimal|Apzīmē 128 bitu (16 baitu) datu tipu.|
|DateTime|Apzīmē 64 bitu (8 baitu) datuma un laika vērtības kodējumu.|
|Int64|Apzīmē 64 bitu (8 baitu) veselu skaitli.|
|Int32|Apzīmē 32 bitu (4 baitu) veselu skaitli.|
|Peldošs|Apzīmē 32 bitu (4 baitu) vienas precizitātes peldošā komata vērtību.|
|Būla|Apzīmē 8 bitu (1 baita) loģisku Būla tipa vērtību. Derīgās vērtības ir patiesa (1) un false (0).|
|Long|Apzīmē 64 bitu (8 baitu) zīmīgu veselu skaitli.|
|String|All String values within the protocol MUST be UNICODE UTF-16. Pēc noklusējuma visas virknes vērtības sākas ar veselu skaitli, kas nosaka virknes garumu. Virknes vērtības protokolā tiek attēlotas kā baitu masīvs; baitu skaitam OBLIGĀTI ir jābūt vienādam ar rakstzīmju skaitu virknē, kas reizināts ar divi.|

### Pārskatu struktūras
Pārskatu struktūrās ir iekļautas to atbilstošo struktūru un elementu definīcijas un izmēri.

Šajā sarakstā ir norādītas pārskatu struktūras:

- Ziņot
- Versija
- Pārskata rekvizīti
- nobīdes masīva elements
- Lapas saturs
- Lappuse
- Lapas rekvizīti
- Lapas izkārtojums
- Sadaļa
- Vienkārša sadaļa
- Jauktā sadaļa
- Sadaļas Rekvizīti
- Ķermeņa zonas elements
- Lapas galvenes elements
- Lapas kājenes elements
- Ķermeņa elements
- Elementu īpašības
- Koplietojamo elementu rekvizīti
- Izmantojiet koplietojamo elementu rekvizītus
- InlineSharedElementProperties
- NonSharedElementProperties
- Stils
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- Darbība
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Līnija
- Attēls
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Diagramma
- GaugePanel
- Karte
- Taisnstūris
- Apakšpārskats
- RichTextBox
- PunktsSaturs
- TextRun
- Paragrāfs
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- Kolonnas platumi
- Kolonnas informācija
- Rindas augstumi
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
- Mērījumi
- Mērīšana
- ReportElementEnd

### Rekvizīti
Tālāk ir norādīts to rekvizītu saraksts, kurus var izmantot RPL straumē.

- ID
- Kolonnu skaits
- kolonnu atstarpes
- Unikāls nosaukums
- Vārds
- Etiķete
- Grāmatzīme
- Rīka padoms
- Pārslēgt vienumu
- Apraksts
- Atrašanās vieta
- ConsumeContainerWhiteSpace (RPL 10.6)
- Valoda
- Izpildes laiks
- Autors
- Automātiskā atsvaidzināšana
- Pārskata nosaukums
- Lapas augstums
- Lapas platums
- MarginTop
- MarginLeft
- MarginRight
- MarginBottom
- Kolonnas
- Lapas nosaukums (RPL 10.6)
- Slīpi
- CanGrow
- CanShrink
- Vērtība
- ToggleState
- CanSort
- SortState
- Formula
- IsToggleParent
- TypeCode
- OriginalValue
- Ir vienkāršs
- Satura nobīde
- Straumes nosaukums
- Izmēru noteikšana
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Attēla nosaukums
- Platums
- Augstums
- Horizontālā izšķirtspēja
- Vertikālā izšķirtspēja
- RawFormat
- Hipersaite
- Grāmatzīmes saite
- DrillthroughId
- DrillthroughUrl
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
- BorderWidth Bottom
- PaddingLeft
- PaddingRight
- PaddingTop
- Polsterējums apakšā
- Fonta stils
- FontFamily
- Fonta izmērs
- FontWeight
- Formāts
- Teksta dekorēšana
- TextAlign
- VerticalAlign
- Krāsa
- Līnijas augstums
- Virziens
- rakstīšanas režīms
- UnicodeBiDi
- Fona attēls
- Fona krāsa
- Fons Atkārtot
- Ciparu valoda
- Skaitliskais variants
- Kalendārs
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Līmenis
- MemberCellIndex
- CellItemOffset
- ColSpan
- Rindas paplašināšana
- DefIndex
- ColumnIndex
- RowIndex
- GroupLabel
- RecursiveToggleLevel
- ListStyle
- ListLevel
- RindasNumurs
- RightIndent
- Kreisā atkāpe
- HangingIndent
- SpaceBefore
- Kosmoss Pēc
- Pirmā līnija
- Atzīmes
- Satura augšdaļa
- Kreisais saturs
- Satura platums
- Satura augstums
- Valsts
- CellItemState
- MemberDefState

### Uzskaitījumi
Šajā sarakstā ir parādīti uzskaitījumi, kurus var izmantot RPL straumē:

- Kārtošanas opcijas
- Izmēri
- ShapeType
- ImageRawFormat
- Fontu stili
- FontWeights
- Teksta dekorācijas
- TextAlignments
- VerticalAlignments
- Norādes
- rakstīšanas režīmi
- UnicodeBiDiTypes
- Kalendāri
- BorderStyles
- BackgroundRepeatTypes
- Sarakstu stili
- Markup Styles
- TypeCode
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLS izmērs





## Atsauces Nr.

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

