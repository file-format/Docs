{
  "date": "2021-03-01",
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RDL - Comhad Teanga Sainmhíniú Tuairisce",
  "keywords": [
"rl",
"teanga sainmhínithe tuairisce",
"XmlTextWriter",
"XSD",
"eilimint RDL"
],
  "description": "Foghlaim faoi fhormáid comhaid RDL arb ionann é agus léiriú XML de shainmhíniú tuarascála ó Sheirbhísí Tuairiscithe Freastalaí SQL.",
  "linktitle": "RDL",
  "menu": {
    "docs": {
      "parent": "reporting",
      "identifier": "reporting-rd-gal"
}
},
  "lastmod": "2021-03-01"
}

## Cad is comhad RDL ann? ##

Is tagarmharc é an RDL (Teanga Sainmhínithe Tuairisce) atá socraithe ag Microsoft chun tuairiscí a shainiú. Tá Eilimint RDL amháin nó go leor i gcomhad RDL. Cé go bhfuil eilimint RDL comhdhéanta dá cineál sonraí agus cardinality. Is féidir le heilimint a bheith simplí nó casta. Níl aon eilimint nó tréithe linbh ag an eilimint shimplí, ach tá leanaí agus tréithe roghnacha ag eilimint chasta.

## Sainmhíniú Scéimre XML RDL
Déanann comhad Sainmhíniú Scéimre XML (XSD) an comhad RDL a bhailíochtú. Sainmhíníonn an scéimre na rialacha maidir leis an áit ar féidir le heilimintí RDL tarlú i gcomhad .rdl. Is féidir le heilimint RDL a bheith simplí nó casta. Níl gnéithe nó tréithe linbh ag eilimint shimplí agus bíonn leanaí ag eilimint chasta agus go roghnach, tréithe.

## RDL á chruthú
Ós rud é go bhfuil RDL oscailte agus insínte sa nádúr, is féidir go leor feidhmchlár agus uirlisí a thógáil a ghineann comhaid RDL bunaithe ar a scéimre XML. Ceann de na bealaí is simplí chun RDL a chruthú ó fheidhmchlár ná úsáid a bhaint as na ranganna Microsoft .NET Framework den ainmspás **System.Xml** agus ainmspás System.Linq. Is féidir an rang **XmlTextWriter**, go háirithe, a úsáid chun RDL a scríobh. Is féidir leat sainmhíniú iomlán a ghiniúint ó thús go deireadh in aon fheidhmchlár .NET Framework trí úsáid a bhaint as **XmlTextWriter**. Is féidir le forbróirí freisin míreanna tuairisce saincheaptha a bhfuil airíonna saincheaptha acu a chur leis chun an RDL a leathnú.

## Cineálacha RDL
Liostaíonn an tábla seo a leanas na cineálacha agus na tréithe a úsáidtear in eilimintí RDL.

|Cineál|Cur Síos|
---|---|
|Dénártha |Airmheán le luach dénártha ionchódaithe-64. ||
| Boole | Airí a bhfuil fíor nó bréagach mar luach an réada. Mura sonraítear a mhalairt, is Bréagach luach réad Boole roghnach a fágadh ar lár.|
|Date	|A property with a fully specified date or datetime value specified in ISO8601 date format: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Airí le luach teagh-théacs nach mór a bheith mar cheann de liosta luachanna ainmnithe.|
|Snámhphointe |Airmheán le luach snámhphointe. Úsáidtear tréimhse (.) mar an deighilteoir roghnach deachúla.|
|Slánuimhir |Airmheán a bhfuil luach slánuimhir (int32) aici. ||
|Teanga |Airmheán le luach téacs a bhfuil cód teanga agus cultúir ann, mar en-us do Bhéarla SAM. Caithfidh an luach a bheith ina theanga ar leith nó ina teanga neodrach a bhfuil teanga réamhshocraithe sainithe ina leith i gCreat .NET Microsoft.|
|Ainm | Airí le luach teagh-théacs. Caithfidh ainmneacha a bheith uathúil laistigh d'ainmspás na míre. Mura bhfuil sé sonraithe, is é an t-ainmspás do mhír an réad is faide istigh a bhfuil ainm air.|
|String normálta |Airíonna a bhfuil luach teagh-théacs aige atá normalaithe.|
|Méid |Ní mór uimhir a bheith i dúil mhéide (le carachtar peiriad a úsáidtear mar dheighilteoir deachúlach roghnach). Ní mór ainmneoir d’aonad fad CSS ar nós cm, mm, in, pt, nó ríomhaire a bheith i ndiaidh na huimhreach. Tá spás idir an uimhir agus an t-ainmneoir roghnach. Chun tuilleadh eolais a fháil faoi shainitheoirí méide, féach CSS Luachanna agus Aonaid Tagairt.In RDL, is é 160 isteach an t-uasluach do Méid. Is é an t-íosmhéid 0 in.|
|Teaghrán |Airíonna a bhfuil luach teagh-théacs air.|
|UnsignedInt |Airmheán a bhfuil luach slánuimhir gan síniú (uint32) aici. ||
|Athróg |Airmheán le haon chineál XML simplí.|

## Cineálacha Sonraí RDL
In RDL, sainmhíníonn an Áireamh DataType cineál sonraí aitreabúide, slonn, nó paraiméadar. Léiríonn an tábla seo a leanas conas a fhreagraíonn cineálacha sonraí CLR do chineálacha sonraí RDL.

|Cineál(anna) CLR |Cineál na Sonraí Comhfhreagracha|
---|---|
| Boole | Boole|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Beart, Sbyte | Slánuimhir|
|Aonair, Dúbailte | Snámhphointe|
|Teaghrán, Cara, GUID, Réimse Ama | Teaghrán |


## Tagairtí ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

