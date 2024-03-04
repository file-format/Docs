{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL – ataskaitos puslapio išdėstymas",
  "keywords": [
"rpl",
"Ataskaitos puslapio išdėstymas",
"XSD",
"SQL serveris",
"ataskaitų teikimas"
],
  "description": "Sužinokite apie RPL srauto formatą, kuris yra vidinis dvejetainis formatas, kurį naudoja Microsoft SQL Server Reporting Services, kai susisiekia su peržiūros valdikliais.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-ltl"
}
},
  "lastmod": "2021-03-02"
}

## Kas yra RPL failas? ##

RPL (ataskaitos puslapio išdėstymo) srauto formatas yra vidinis dvejetainis formatas, kurį naudoja MS SQL Server Reporting Services, kai susisiekia su peržiūros valdikliais, kad sumažintų tam tikrą atvaizdavimo darbą iš serverio į kliento peržiūros valdiklį. Kūrėjai gali sukurti pasirinktinius ataskaitų kūrėjus naudodami RPL, kurie generuos RPL, taip pat pasirinktinius ataskaitų pateikimo įrenginius, kurie apdoroja ir rodo RPL failą, kad būtų rodomos ataskaitos.

## RPL struktūros

RPL srautas apima srauto struktūrą, ataskaitos struktūrą, ataskaitos ypatybes ir sąrašus. Kiekviena struktūra apima šiuos elementus:

- Struktūros apibrėžimas.

- Papildytos Backus-Naur formos (ABNF) struktūros gramatika.

- Šiek tiek struktūros diagrama.

- Visų struktūroje esančių laukų apibrėžimai.

Štai trumpos pastabos apie kai kurias RPL struktūras:

### Srauto struktūra
Srauto struktūra susideda iš įrašų serijos. Įraše yra nulis arba daugiau struktūrinių laukų, kuriuose yra ataskaitos išdėstymas.

#### RPL srautas
RPL sraute turi būti tik vienas ataskaitos įrašas, o srautas turi būti dvejetainių įrašų, išlaikančių ataskaitų hierarchiją, serija.

#### Įrašas
Įrašas yra pagrindinė sudedamoji dalis, naudojama informacijai apie ataskaitą saugoti. Įrašas susideda iš įvairaus ilgio baitų sekos. Įrašas susideda iš dviejų komponentų:
- Įrašo tipas
– tam įrašo tipui būdingi įrašo duomenys.
Įrašo tipas yra vienas baitas, apibrėžiantis, kokio tipo informaciją nurodo įrašas ir kaip sutvarkoma ir struktūrizuojama su įrašu susijusių įrašo duomenų struktūra. Įrašo reikšmė priklauso nuo tam įrašui būdingų duomenų tipo.

#### Paprastos duomenų tipo struktūros

Šioje lentelėje apibrėžiami duomenų tipai RPL sraute.

|Aprašymas| formatas|
---|---|
|Char|Nurodo 16 bitų (2 baitų) skaitinę (eilės) reikšmę.|
|Baitas|Nurodo 8 bitų (1 baito) sveikąjį skaičių be ženklo.|
|Int16|Nurodo 16 bitų (2 baitų) pasirašytą sveikąjį skaičių.|
|Single|Nurodo 32 bitų (4 baitų) vieno tikslumo slankiojo kablelio reikšmę.|
|Dešimtainis|Nurodo 128 bitų (16 baitų) duomenų tipą.|
|DateTime|Nurodo 64 bitų (8 baitų) datos ir laiko reikšmės koduotę.|
|Int64|Nurodo 64 bitų (8 baitų) sveikąjį skaičių.|
|Int32|Nurodo 32 bitų (4 baitų) sveikąjį skaičių.|
|Slankioji reikšmė|Nurodo 32 bitų (4 baitų) vieno tikslumo slankiojo kablelio reikšmę.|
|Boolean|Nurodo 8 bitų (1 baito) loginę Būlio tipo reikšmę. Galiojančios reikšmės yra true (1) ir false (0).|
|Long|Nurodo 64 bitų (8 baitų) pasirašytą sveikąjį skaičių.|
|String|All String values within the protocol MUST be UNICODE UTF-16. Pagal numatytuosius nustatymus visos eilutės reikšmės prasideda sveikuoju skaičiumi, kuris apibrėžia eilutės ilgį. Eilučių reikšmės protokole pateikiamos kaip baitų masyvas; baitų skaičius TURI būti lygus simbolių skaičiui eilutėje, padaugintam iš dviejų.|

### Ataskaitų struktūros
Ataskaitų struktūros apima atitinkamų struktūrų ir elementų apibrėžimus ir dydžius.

Šis sąrašas nurodo ataskaitų struktūras:

- Pranešti
- Versija
- Ataskaitos ypatybės
- Poslinkio masyvo elementas
– Puslapio turinys
- Puslapis
– Puslapio ypatybės
- Puslapio išdėstymas
- Skyrius
- Paprastas skyrius
- Mišrus skyrius
- Skyriaus ypatybės
- Kūno srities elementas
- Puslapio antraštės elementas
- Puslapio poraštės elementas
- Kūno elementas
- Elemento savybės
- Bendros elemento savybės
- Naudokite bendrinamų elementų ypatybes
– InlineSharedElementProperties.
– NonSharedElementProperties.
- Stilius
- SharedStyleProperties
– NonSharedStyleProperties.
- ActionInfo
- ActionInfoContent
– Veiksmas
– ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData.
- ImageConsolidationOffsets
- Pranešti apie elementą
- Linija
- Vaizdas
- ImageDataProperties
– UseSharedImageDataProperties
– InlineSharedImageDataProperties
– NonSharedImageDataProperties.
- Vaizdo duomenys
– ImageMapAreas.
- ImageMapArea
- Diagrama
- GaugePanel
- Žemėlapis
- Stačiakampis
- SubReport
- RichTextBox
- Pastraipos turinys
- TextRun
- Pastraipa
- RichTextBoxStructure
- Tablix
- TablixContent.
- TablixStructure
- TablixMeasurements.
- StulpeliaiPločiai
- Stulpelio informacija
- Eilutės aukščiai
- Eilutės informacija
- TablixRow
- TablixRowCell.
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
– TablixBodyRowCells.
- TablixBodyRow.
- TablixBodyCell.
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Išmatavimai
- Matavimas
- ReportElementEnd

### Savybės
Toliau pateikiamas ypatybių, kurias galima naudoti RPL sraute, sąrašas:

- ID
- Stulpelių skaičius
- Stulpelių tarpai
- Unikalus pavadinimas
- Vardas
- Etiketė
- Skirtukas
- Įrankio patarimas
- Perjungti elementą
- Apibūdinimas
- Vieta
– ConsumeContainerWhiteSpace (RPL 10.6)
– Kalba
- Vykdymo laikas
– Autorius
- Automatinis atnaujinimas
- Pranešimo pavadinimas
- Puslapio aukštis
- Puslapio plotis
- MarginTop
- Kairė paraštė
- MarginRight
- MarginBottom
- Stulpeliai
– Puslapio pavadinimas (RPL 10.6)
- Pasviręs
- Gali augti
- CanShrink
– Vertė
- ToggleState
- Gali Rūšiuoti
– Rūšiavimo būsena
- Formulė
– IsToggleParent
- Tipo kodas
- Original Value
- Yra paprasta
- Turinio poslinkis
- Srauto pavadinimas
- Dydžio nustatymas
- LinkTo Child
- PrintOnFirstPage
– PrintBetweenSections (RPL 10.4)
– FormattedValueExpressionBased
– ProcesedWithError
- VaizdoMIMEType
- Vaizdo pavadinimas
- Plotis
- Aukštis
- Horizontali raiška
- Vertikali skiriamoji geba
- neapdorotas formatas
- Hipersaitas
- Žymės nuoroda
- DrillthroughId
- Gręžimas per URL
- BorderColor
- BorderColorLeft
– BorderColorRight
– BorderColorTop
- BorderColorBottom
- BorderStyle
– BorderStyleLeft
– BorderStyleRight
– BorderStyleTop
- BorderStyleBottom
- BorderWidth
– BorderWidthLeft
– BorderWidthRight
– BorderWidthTop
– BorderWidthBottom
- PaddingLeft
- PaddingRight
- PaddingTop
- Padding Bottom
- Šrifto stilius
- Šrifto šeima
- Šrifto dydis
- Šrifto svoris
- Formatas
- Teksto dekoravimas
- TextAlign
- Vertikalus išlygiavimas
- Spalva
- Linijos aukštis
- Kryptis
- Rašymo režimas
- UnicodeBiDi
- Fono vaizdas
- Fono spalva
- Fono kartojimas
- Skaičių kalba
- Skaičių variantas
- Kalendorius
- Stulpelio antraštės eilutės
- Eilučių antraštės stulpeliai
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Lygis
- MemberCellIndex
- CellItemOffset
- ColSpan
- Eilučių ilgis
- DefIndex
- ColumnIndex
- Eilutės indeksas
- GroupLabel
- RecursiveToggleLevel
- Sąrašo stilius
- Sąrašo lygis
- PastraiposNumber
- Dešinioji įtrauka
- Kairioji įtrauka
- Kabanti įtrauka
- SpacePrieš
- Kosmosas po
- Pirma eilė
- Žymėjimas
– Turinio viršus
- Turinys kairėje
- Turinio plotis
- Turinio aukštis
– Valstybė
- CellItemState
- MemberDefState

### Sąrašai
Šiame sąraše pateikiami sąrašai, kuriuos galima naudoti RPL sraute:

- Rūšiavimo parinktys
- Dydžiai
- ShapeType
- ImageRawFormat
- Šriftų stiliai
- FontWeights
- Teksto dekoracijos
- Teksto lygiavimas
- Vertikalus lygiavimas
- Nurodymai
- Rašymo režimai
- UnicodeBiDiTypes
- Kalendoriai
– BorderStyles
- BackgroundRepeatTypes
- Sąrašo stiliai
- MarkupStyles
- Tipo kodas
- StateValues
– TablixMemberStateValues.
– TablixMemberDefStateValues.
- RPLS dydis





## Nuorodos Nr.

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

