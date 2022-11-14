{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Rapportpagina-indeling",
  "keywords" :[ "rpl", "Report Page Layout", "XSD", "SQL Server", "reporting"],
  "description":"Meer informatie over het RPL-stroomformaat, een intern binair formaat dat wordt gebruikt door Microsoft SQL Server Reporting Services bij contact met de bedieningselementen van de kijker.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## Wat is een RPL-bestand? ##

Het RPL-stroomformaat (Report Page Layout) is een intern binair formaat dat wordt gebruikt door MS SQL Server Reporting Services bij contact met viewerbesturingselementen om een deel van het weergavewerk van de server naar de clientviewerbesturing te verminderen. Ontwikkelaars kunnen aangepaste rapportontwerpers maken met behulp van RPL, dat RPL genereert, evenals aangepaste rapportrenderers die het RPL-bestand verwerken en weergeven om rapporten weer te geven.

## RPL-structuren

Een RPL-stroom omvat stroomstructuur, rapportstructuur, rapporteigenschappen en opsommingen. Elke structuur omvat het volgende:

- Een definitie van de structuur.

- De Augmented Backus-Naur Form (ABNF) grammatica voor de structuur.

- Een beetje diagram van de structuur.

- Definities van alle velden in de structuur.

Hier zijn de korte opmerkingen over enkele van de RPL-structuren:

### Streamstructuur
De stroomstructuur bestaat uit een reeks records. Een record bevat nul of meer gestructureerde velden die de rapportlay-out bevatten.

#### RPL-stream
De RPL-stream mag slechts één rapportrecord hebben en de stream moet een reeks binaire records zijn die de rapporthiërarchie behouden.

#### Dossier
Het record is een basisbouwsteen die wordt gebruikt om de informatie over een rapport te bewaren. Een record bestaat uit een reeks bytes met verschillende lengtes. Een record bestaat uit twee componenten:
- Een recordtype
- De recordgegevens die specifiek zijn voor dat recordtype.
Het recordtype is één byte dat definieert welk type informatie door het record wordt gespecificeerd en hoe de structuur van de recordgegevens met betrekking tot het record is geordend en gestructureerd. De recordwaarde is afhankelijk van het type gegevens dat specifiek is voor dat record.

#### Eenvoudige gegevenstypestructuren

De volgende tabel definieert de gegevenstypen in een RPL-stroom.

|Beschrijving| formaat|
---|---|
|Char|Vertegenwoordigt een 16-bits (2-byte) numerieke (ordinale) waarde.|
|Byte|Vertegenwoordigt een 8-bits (1-byte) geheel getal zonder teken.|
|Int16|Vertegenwoordigt een 16-bits (2-byte) geheel getal met teken.|
|Single|Vertegenwoordigt een 32-bits (4-byte) single-precision floating point-waarde.|
|Decimaal|Vertegenwoordigt een 128-bits (16-byte) gegevenstype.|
|DateTime|Vertegenwoordigt een 64-bits (8-byte) codering van een datum- en tijdwaarde.|
|Int64|Vertegenwoordigt een 64-bits (8-byte) geheel getal met teken.|
|Int32|Vertegenwoordigt een 32-bits (4-byte) geheel getal met teken.|
|Float|Vertegenwoordigt een 32-bits (4-byte) single-precision floating point-waarde.|
|Boolean|Vertegenwoordigt een 8-bits (1-byte) logische Booleaanse waarde. De geldige waarden zijn waar (1) en onwaar (0).|
|Lang|Vertegenwoordigt een 64-bits (8-byte) geheel getal met teken.|
|String|Alle String-waarden binnen het protocol MOETEN UNICODE UTF-16 zijn. Standaard beginnen alle String-waarden met een geheel getal dat de lengte van de String definieert. Stringwaarden worden in het protocol weergegeven als een array van bytes; het aantal bytes MOET gelijk zijn aan het aantal karakters in de String vermenigvuldigd met twee.|

### Rapportstructuren
De rapportstructuren bevatten de definities en afmetingen van hun relevante structuren en elementen.

De volgende lijst specificeert de rapportstructuren:

- Rapport
- Versie
- Rapporteigenschappen
- Offset array-element
- Pagina inhoud
- Bladzijde
- Pagina-eigenschappen
- Pagina layout
- Sectie
- Eenvoudige sectie
- Gemengde sectie
- Sectie Eigenschappen
- Element lichaamsgebied
- Paginakoptekstelement
- Element paginavoettekst
- Lichaamselement
- Elementeigenschappen
- Eigenschappen van gedeelde elementen
- Eigenschappen van gedeelde elementen gebruiken
- InlineSharedElementProperties
- Niet-gedeelde elementeigenschappen
- Stijl
- SharedStyleProperties
- Niet-gedeelde stijleigenschappen
- ActieInfo
- ActionInfoContent
- Actie
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidation Offsets
- Meld item
- Lijn
- Afbeelding
- ImageDataProperties
- Gebruik SharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- Afbeeldingsgegevens
- ImageMapAreas
- ImageMapArea
- Grafiek
- Meterpaneel
- Kaart
- Rechthoek
- Subrapport
- RichTextBox
- ParagraafInhoud
- TextRun
- Paragraaf
- RichTextBox-structuur
- Tablix
- TablixContent
- TablixStructuur
- TablixMetingen
- Kolombreedtes
- Kolominfo
- Rijhoogten
- RowInfo
- TablixRij
- TablixRowCell
- TablixCorner
- TablixKolomkop
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Afmetingen
- Meting
- RapportElementEinde

### Eigendommen
Hieronder volgt de lijst met eigenschappen die in een RPL-stream kunnen worden gebruikt:

- ID KAART
- Kolomtelling
- Kolomafstand
- Unieke naam
- Naam
- Label
- Bladwijzer
- ToolTip
-ToggleItem
- Beschrijving
- Plaats
- ConsumeContainerWhiteSpace (RPL 10.6)
- Taal
- Uitvoertijd
- Auteur
- Automatisch vernieuwen
- Rapportnaam
- Paginahoogte
- Paginabreedte
- MargeTop
- Marge Links
- MargeRechts
- Marge Bodem
- Kolommen
- Paginanaam (RPL 10.6)
- Schuin
- Kan groeien
-CanShrink
- Waarde
- Schakelstatus
- CanSorteren
- Sorteerstatus
- Formule
- IsToggleParent
- Typecode
- Originele waarde
- Is simpel
- Inhoudscompensatie
- Streamnaam
- Maatvoering
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- Verwerkt met fout
- ImageMIMEType
- Afbeeldingsnaam
- Breedte
- Hoogte
- Horizontale resolutie
- Verticale resolutie
- RawFormaat
- Hyperlink
- BookmarkLink
- DrillthroughId
- DrillthroughUrl
- Rand kleur
- BorderColorLinks
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- Grensstijl
- BorderStyle Left
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Grensbreedte
- BorderBreedte Links
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- Padding Links
- VullingRechts
- Vulling Top
- Vulling Bodem
- Lettertype
- FontFamilie
- Lettertypegrootte
- Lettertype dikte
- Formaat
- Tekstdecoratie
- TextAlign
- VerticalAlign
- Kleur
- Lijnhoogte
- Richting
- Schrijfmodus
- UnicodeBiDi
- Achtergrond afbeelding
- Achtergrond kleur
- Achtergrond herhaling
- CijferTaal
- CijferVariant
- Kalender
- ColumnHeaderRijen
- RowHeaderColumns
- ColsBeforeRowHeader
- Lay-outRichting
- Definitiepad
- Niveau
- MemberCellIndex
- CellItemOffset
- ColSpan
- Rijspan
- DefIndex
- ColumnIndex
- RijIndex
- Groepslabel
- Recursief ToggleLevel
- Lijststijl
- Lijstniveau
- Alineanummer
- RechtsInspringen
- Links inspringen
- Hangende inspringing
- SpaceBefore
- SpaceAfter
- Eerste lijn
- Markup
- InhoudTop
- Inhoud Links
- InhoudBreedte
- Inhoud Hoogte
- Staat
- CellItemState
- LidDefState

### Opsommingen
De volgende lijst toont de opsommingen die kunnen worden gebruikt in de RPL-stroom:

- Sorteeropties
- Maten
- Vormtype
- ImageRawFormat
- Lettertypestijlen
- Lettertypegewichten
- Tekstdecoraties
- Tekstuitlijningen
- Verticale uitlijningen
- Routebeschrijving
- Schrijfmodi
- UnicodeBiDiTypes
- Kalenders
- Grensstijlen
- Achtergrondherhalingstypen
- Lijststijlen
- Opmaakstijlen
- Typecode
- Staatswaarden
- TablixMemberStateValues
- TablixMemberDefStateValues
-RPLSmaat





## Referenties ##

- [Report Page Layout (RPL) Binary Stream Format](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

