{
  "date": "2021-03-02",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RPL - Leagan Amach Leathanach na Tuarascála",
  "keywords": [
"rpl",
"Tuairisc Leagan Amach",
"XSD",
"Freastalaí SQL",
"tuairisceoireachta"
],
  "description": "Foghlaim faoi fhormáid srutha RPL ar formáid dhénártha inmheánach í a úsáideann Seirbhísí Tuairiscithe Microsoft SQL Server agus iad i dteagmháil le rialuithe breathnóirí.",
  "linktitle": "RPL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rp-gal"
}
},
  "lastmod": "2021-03-02"
}

## Cad is comhad RPL ann? ##

Is formáid dhénártha inmheánach í an fhormáid srutha RPL (Tuairisc Leagan Amach) a úsáideann Seirbhísí Tuairiscithe MS SQL Server agus iad i dteagmháil le rialuithe breathnóirí chun cuid den obair rindreála a laghdú ón bhfreastalaí go dtí an cliant rialaithe féachana. Is féidir le forbróirí dearthóirí tuairiscí saincheaptha a chruthú trí úsáid a bhaint as RPL, a ghinfidh RPL chomh maith le rindreálaithe tuairisce saincheaptha a phróiseálann agus a thaispeánann an comhad RPL chun tuairiscí a thaispeáint.

## Struchtúir RPL

Áirítear le sruth RPL struchtúr srutha, struchtúr tuairisce, airíonna tuairisce, agus áirimh. Áirítear na nithe seo a leanas i ngach struchtúr:

- Sainmhíniú ar an struchtúr.

- Gramadach na Foirme Méadaithe Backus-Naur (ABNF) don struchtúr.

- Léaráid ghiotán den struchtúr.

- Sainmhínithe ar na réimsí go léir laistigh den struchtúr.

Seo iad na nótaí gairide faoi chuid de na Struchtúir RPL:

### Struchtúr an tSrutha
Tá struchtúr an tsrutha comhdhéanta de shraith taifead. Tá nialas nó níos mó réimsí struchtúrtha i dtaifead ina bhfuil leagan amach na tuarascála.

#### Sruth RPL
Ní mór go mbeadh ach taifead Tuarascála amháin ag an sruth RPL agus ní mór gur sraith de thaifid dhénártha a choimeádann an t-ordlathas tuairisce a bheidh sa sruth.

#### Taifead
Is bloc tógála bunúsach é an taifead a úsáidtear chun an fhaisnéis faoi thuairisc a choinneáil. Is éard atá i dtaifead seicheamh faid éagsúla beart. Tá dhá chomhpháirt i dtaifead:
- Cineál taifead
- Na sonraí taifid a bhaineann go sonrach leis an gcineál taifid sin.
Beart amháin is ea an cineál taifid a shainíonn cén cineál faisnéise atá sonraithe sa taifead agus conas a ordaítear agus a struchtúraítear struchtúr na sonraí taifid a bhaineann leis an taifead. Tá luach an taifid ag brath ar an gcineál sonraí a bhaineann go háirithe leis an taifead sin.

#### Struchtúir Shimplí Cineál Sonraí

Sainmhíníonn an tábla seo a leanas na cineálacha sonraí i sruth RPL.

|Cur síos| formáid |
---|---|
|Char|Is luach uimhriúil (gnáth-ghiotán) 16-giotán (2-bheart).
| Beart|Is ionann é agus slánuimhir 8-giotán (1-bheart) gan síniú.|
|Int16|Is ionann é agus slánuimhir sínithe 16-giotán (2-bheart).
|Aonair|Is ionann é agus luach snámhphointe aonbheachtais 32-giotán (4-beart).
|Deachúil|Is cineál sonraí 128-giotán (16-beart).
|DateTime|Is ionann é agus ionchódú 64-giotán (8-bheart) de luach dáta agus ama. ||
|Int64|Is ionann é agus slánuimhir sínithe 64-giotán (8-bheart).
|Int32|Is ionann é agus slánuimhir sínithe 32-giotán (4-bheart).
|Snámhphointe|Is ionann é agus luach snámhphointe aonbheachtais 32-giotán (4-beart).
|Boolean|Is ionann é agus luach cineáil Boole loighciúil 8-giotán (1-bheart). Tá na luachanna bailí fíor (1) agus bréagach (0) ||
|Fada|Is ionann é agus slánuimhir sínithe 64-giotán (8-bheart).
|String|All String values within the protocol MUST be UNICODE UTF-16. De réir réamhshocraithe, tosaíonn gach luach Teaghrán le slánuimhir a shainíonn fad an Teaghráin. Léirítear luachanna teaghrán sa phrótacal mar raon beart; NÍ MÓR líon na mbeart a bheith comhionann le líon na gcarachtar sa Teaghrán iolraithe ar dhá. ||

### Struchtúir Tuairisce
Áirítear i struchtúir na tuarascála sainmhínithe agus méideanna na struchtúr agus na ngnéithe ábhartha.

Sonraíonn an liosta seo a leanas na struchtúir tuairisce:

- Tuairisc
- Leagan
- Airíonna Tuairisc
- Eilimint Eagar Fritháireamh
- Ábhar Leathanach
- Leathanach
- Airíonna leathanach
- Leagan Amach na leathanach
- Alt
- Alt Simplí
- Alt Measctha
- Airíonna Alt
- Eilimint Achar Coirp
- Eilimint Ceanntásc Leathanaigh
- Leathanach Buntásc Eilimint
- Eilimint Coirp
- Airíonna Eiliminte
- Airíonna Eiliminte Roinnte
- Úsáid Airíonna Eiliminte Roinnte
- Airíonna InlineSharedElement
- Airíonna Neamhroinnte
- Stíl
- Airíonna SharedStyle
- Airíonna Neamh-SharedStyle
- ActionInfo
- ActionInfoContent
- Gníomh
- ActionImageMapAreas
- ActionInfoWithMaps
- DinimiciúlaImageData
- ImageConsolidationOffsets
- TuairiscItem
- Líne
- Íomha
- Airíonna ImageData
- UseSharedImageDataProperties
- Airíonna InlineSharedImageData
- Airíonna NeamhSharedImageData
- ÍomháData
- ImageMapAreas
- ImageMapArea
- Cairt
- Painéal Tomhsaire
- Léarscáil
- Dronuilleog
- Fo-Thuairisc
- RichTextBox
- Ábhar Alt
- TextRun
- Alt
- Struchtúr RichTextBox
- Táblaics
- Ábhar Tablix
- Struchtúr Tablix
- Tomhais Tablix
- Leithead na gColún
- ColumnInfo
- RowHeights
- RowInfo
- TáblaixRow
- TablixRowCell
- Cúinne Tablix
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TáblaixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TáblaixMemberDef
- Tomhais
- Tomhas
- ReportElementEnd

### Airíonna
Seo a leanas liosta na n-airíonna is féidir a úsáid i Sruth RPL:

- ID
- Colún Líon
- Spásáil Colún
- Ainm Uathúil
- Ainm
- Lipéad
- Leabharmharc
- Leid Uirlisí
- ToggleItem
- Cur síos
- Suíomh
- ConsumeContainerWhiteSpace (RPL 10.6)
- Teanga
- Am Forghníomhaithe
- Údar
- Athnuachan Uathoibríoch
- TuairiscName
- PageHeight
- Leathan Leathanaigh
- ImeallTop
- Imeall ar chlé
- Imeall Ceart
- Imeall Bun
- Colúin
- Ainm an Leathanaigh (RPL 10.6)
- Slant
- CanGrow
- CanShrink
- Luach
- ToggleState
- CanSort
- SortState
- Foirmle
- IsToggleParent
- Cineál-Chód
- Bunluach
- IsSimplí
- ContentOffset
- StreamName
- Sizing
- LinkToChild
- PrintOnFirstPage
- PrintIdirRanna (RPL 10.4)
- FormáiditheValueExpressionBased
- ProcessedWithError
- Cineál ÍomháMIMET
- ÍomháName
- Leithead
- Airde
- Rún Cothrománach
- Réiteach Ingearach
- RawFormat
- Hipearnasc
- BookmarkLink
- DrillthroughId
- DrillthroughUrl
- Dath Teorainn
- Teorainn Dath Clé
- TeorannColorCeart
- TeorainnColorTop
- TeorainnColorBottom
- Stíl Teorainn
- Stíl Teorainn ar Chlé
- BorderStyleCeart
- BorderStyleTop
- Stíl TeorannBun
- Leithead na Teorann
- BorderWidthLeft
- BorderWidthCeart
- BorderWidthTop
- BorderWidthBottom
- PaddingLeft
- PaddingCeart
- Barr na bPoll
- Bun stuáil
- Stíl Chló
- FontFamily
- Méid cló
- Clómheáchan
- Formáid
- TextDecoration
- TéacsAlign
- Ailíniú Ingearach
- Dath
- Airde Líne
- Treo
- Modh Scríbhneoireachta
- UnicodeBiDi
- Íomhá Chúlra
- Dath Cúlra
- CúlraAthchraoladh
- UimhirTeanga
- Athrú Uimhriúil
- Féilire
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- Treoir Leagan Amach
- Cosán Sainmhíniú
- Leibhéal
- MemberCellIndex
- CellItemOffset
- ColSpáin
- RóSpáinn
- DefIndex
- ColúnInnéacs
- RowIndex
- Lipéad Grúpa
- AthchúrsachToggleLevel
- Stíl Liosta
- Leibhéal Liosta
- Uimhir Alt
- CeartIndent
- LeftIndent
- HangingIndent
- Spás Roimh
- SpásAfter
- An Chéad Líne
- Marcáil
- ÁbharTop
- ÁbharLeft
- ÁbharWidth
- ÁbharAirde
- Stáit
- CellItemState
- BallStáit

### Áirimh
Taispeánann an liosta seo a leanas na háirimh is féidir a úsáid sa sruth RPL:

- SortOptions
- Méideanna
- Cineál Cruth
- ÍomháRawFormat
- Stíleanna Cló
- Meáchan Cló
- Maisiúcháin Téacs
- Ailínithe Téacs
- Ailínithe Ingearach
- Treoracha
- Modhanna Scríbhneoireachta
- Cineálacha UnicodeBiDi
- Féilirí
- Stíleanna Teorann
- Cineálacha Athdhéanta Cúlra
- Stíleanna Liosta
- Stíleanna Markup
- Cineál-Chód
- Luachanna Stáit
- Luachanna TablixMemberState
- Luachanna TablixMemberDefState
- RPLSize





## Tagairtí ##

- [Report Page Layout (RPL) Binary Stream Format](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

