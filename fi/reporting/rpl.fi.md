{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL - Raporttisivun asettelu",
  "keywords": [
"rpl",
"Raportoi sivun asettelu",
"XSD",
"SQL Server",
"raportointi"
],
  "description": "Opi RPL-virtamuodosta, joka on sisäinen binaarimuoto, jota Microsoft SQL Server Reporting Services käyttää ottaessaan yhteyttä katseluohjelman ohjaimiin.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-fil"
}
},
  "lastmod": "2021-03-02"
}

## Mikä on RPL-tiedosto? ##

RPL (Report Page Layout) -virtamuoto on sisäinen binaarimuoto, jota MS SQL Server Reporting Services käyttää ottaessaan yhteyttä katseluohjelman ohjaimiin vähentääkseen osan renderöintityöstä palvelimelta asiakkaan katseluohjelman ohjaukseen. Kehittäjät voivat luoda mukautettuja raporttisuunnittelijoita RPL:n avulla, jotka luovat RPL:n sekä mukautettuja raporttien hahmontajia, jotka käsittelevät ja näyttävät RPL-tiedoston raporttien näyttämiseksi.

## RPL-rakenteet

RPL-virta sisältää virtarakenteen, raporttirakenteen, raportin ominaisuudet ja luettelot. Jokainen rakenne sisältää seuraavat:

- Rakenteen määritelmä.

- Augmented Backus-Naur Form (ABNF) -kielioppi rakenteelle.

- Pieni kaavio rakenteesta.

- Kaikkien rakenteen sisältämien kenttien määritelmät.

Tässä lyhyet huomautukset joistakin RPL-rakenteista:

### Virran rakenne
Virtausrakenne koostuu sarjasta tietueita. Tietue sisältää nolla tai useampia jäsenneltyjä kenttiä, jotka sisältävät raportin asettelun.

#### RPL-stream
RPL-virrassa on oltava vain yksi raporttitietue, ja virran on oltava sarja binääritietueita, jotka säilyttävät raporttihierarkian.

#### Ennätys
Tietue on perusrakennuspalikka, jota käytetään raportin tietojen säilyttämiseen. Tietue koostuu vaihtelevan pituisesta tavujonosta. Tietue koostuu kahdesta osasta:
- Tietuetyyppi
- Tietuetiedot, jotka liittyvät kyseiselle tietuetyypille.
Tietuetyyppi on yksi tavu, joka määrittää, minkä tyyppistä tietoa tietue määrittää ja miten tietueeseen liittyvän tietuetietojen rakenne on järjestetty ja jäsennelty. Tietueen arvo riippuu tietueelle ominaisen tiedon tyypistä.

#### Yksinkertaiset tietotyyppirakenteet

Seuraavassa taulukossa määritellään RPL-virran tietotyypit.

|Kuvaus| muoto|
---|---|
|Char|Esittää 16-bittistä (2-tavuista) numeerista (järjestysarvoa).|
|Byte|Esittää 8-bittinen (1-tavu) etumerkitön kokonaisluku.|
|Int16|Esittää 16-bittinen (2-tavuinen) etumerkillinen kokonaisluku.|
|Single|Esittää 32-bittistä (4-tavuista) yhden tarkkuuden liukulukuarvoa.|
|Desimaali|Esittää 128-bittistä (16-tavuista) tietotyyppiä.|
|DateTime|Esittää päivämäärän ja kellonajan 64-bittistä (8-tavuista) koodausta.|
|Int64|Esittää 64-bittinen (8-tavuinen) etumerkillinen kokonaisluku.|
|Int32|Esittää 32-bittistä (4-tavuista) etumerkillistä kokonaislukua.|
|Float|Esittää 32-bittistä (4-tavua) yhden tarkkuuden liukulukuarvoa.|
|Boolean|Esittää 8-bittisen (1-tavun) loogisen Boolen tyypin arvoa. Kelvolliset arvot ovat tosi (1) ja false (0).|
|Long|Esittää 64-bittinen (8-tavuinen) etumerkillinen kokonaisluku.|
|String|All String values within the protocol MUST be UNICODE UTF-16. Oletusarvoisesti kaikki merkkijonoarvot alkavat kokonaisluvulla, joka määrittää merkkijonon pituuden. Merkkijonoarvot esitetään protokollassa tavujen joukkona; tavujen määrän TÄYTYY olla yhtä suuri kuin merkkijonon merkkien määrä kerrottuna kahdella.|

### Raporttirakenteet
Raporttirakenteet sisältävät niiden oleellisten rakenteiden ja elementtien määritelmät ja koot.

Seuraava luettelo määrittää raporttien rakenteet:

- Raportoi
- Versio
- Raportin ominaisuudet
- Offset Array Element
- Sivun sisältö
- Sivu
- Sivun ominaisuudet
- Sivun asettelu
- Osio
- Yksinkertainen osa
- Sekaosasto
- Osion ominaisuudet
- Body Area Element
- Sivun otsikkoelementti
- Sivun alatunniste
- Runkoelementti
- Elementin ominaisuudet
- Jaetut elementin ominaisuudet
- Käytä jaettujen elementtien ominaisuuksia
- InlineSharedElementProperties
- NonSharedElementProperties
- Tyyli
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- Toiminta
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- Linja
- Kuva
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Kaavio
- Mittaripaneeli
- Kartta
- Suorakulmio
- Alaraportti
- RichTextBox
- Kappalesisältö
- TextRun
- Kohta
- RichTextBoxStructure
- Tablix
- TablixContent
- TablixStructure
- TablixMeasurements
- SarakkeetWidths
- Saraketiedot
- Rivinkorkeudet
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
- Mitat
- Mittaus
- ReportElementEnd

### Ominaisuudet
Seuraavassa on luettelo ominaisuuksista, joita voidaan käyttää RPL-streamissa:

- ID
- ColumnCount
- Sarakeväli
- Ainutlaatuinen nimi
- Nimi
- Etiketti
- Kirjanmerkki
- Työkaluvinkki
- ToggleItem
- Kuvaus
- Sijainti
- ConsumeContainerWhiteSpace (RPL 10.6)
- Kieli
- Suoritusaika
- Tekijä
- AutoRefresh
- Raportin nimi
- Sivun korkeus
- Sivun leveys
- MarginTop
- Marginaali Vasen
- Margin Right
- MarginBottom
- Sarakkeet
- Sivun nimi (RPL 10.6)
- Viistot
- CanGrow
- CanShrink
- Arvo
- ToggleState
- Voi lajitella
- SortState
- Kaava
- IsToggleParent
- TypeCode
- OriginalValue
-OnSimple
- ContentOffset
- StreamName
- Mitoitus
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- Kuvan nimi
- Leveys
- Korkeus
- Vaakaresoluutio
- Pystyresoluutio
- RawFormat
- Hyperlinkki
- Kirjanmerkkilinkki
- DrillthroughId
- DrillthroughUrl
- Reunuksen väri
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
- Pehmustepohja
- Fonttityyli
- FontFamily
- Fonttikoko
- FontWeight
- Muoto
- Tekstin koristelu
- TextAlign
- VerticalAlign
- Väri
- Viivankorkeus
- Suunta
- Kirjoitustila
- UnicodeBiDi
- Taustakuva
- Taustaväri
- Taustatoisto
- NumeralLanguage
- NumeralVariant
- Kalenteri
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- Taso
- MemberCellIndex
- CellItemOffset
- ColSpan
- Riviväli
- DefIndex
- ColumnIndex
- RowIndex
- GroupLabel
- RecursiveToggleLevel
- ListStyle
- Listataso
- kohtaNumber
- Oikea sisennys
- Vasen sisennys
- Riippuva sisennys
- SpaceBefore
- Space After
- Ensimmäinen linja
- Merkintä
- SisältöTop
- Sisältö Vasen
- ContentWidth
- Sisältökorkeus
- Valtio
- CellItemState
- MemberDefState

### Luettelot
Seuraava luettelo näyttää luettelot, joita voidaan käyttää RPL-virrassa:

- Lajitteluvaihtoehdot
- Mitoitukset
- Muototyyppi
- ImageRawFormat
- FontStyles
- FontWeights
- Tekstikoristeet
- TextAlignments
- VerticalAlignments
- Ohjeet
- Kirjoitustilat
- UnicodeBiDiTypes
- Kalenterit
- BorderStyles
- BackgroundRepeatTypes
- ListStyles
- MarkupStyles
- TypeCode
- State Values
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLS-koko





## Viitteet ##

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

