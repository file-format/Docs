{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Foghlaim faoi fhormáid comhaid SAV agus APIanna ar féidir leo comhaid SAV a chruthú agus a oscailt.",
  "title" : "SAV - Comhad Sonraí SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav-ga",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Cad is comhad SAV ann?
Is comhad sonraí é comhad SAV a chruthaigh an Pacáiste Staidrimh do na hEolaíochtaí Sóisialta (SPSS), ar feidhmchlár é a úsáideann taighdeoirí margaidh, taighdeoirí sláinte, cuideachtaí suirbhéireachta, an rialtas, taighdeoirí oideachais, eagraíochtaí margaíochta, mianadóirí sonraí le haghaidh anailíse staitistiúla. Sábháiltear an SAV i bhformáid dhénártha dhílseánaigh agus cuimsíonn sé tacar sonraí chomh maith le foclóir a léiríonn an tacar sonraí, a shábhálann sonraí i sraitheanna agus i gcolúin.

## Formáid Chomhaid SAV
Tá formáid comhaid SAV éirithe sách cobhsaí, ach ní féidir linn a rá go statach. Tá comhoiriúnacht siar agus ar aghaidh ar fáil go roghnach nuair is gá, ach ní dhéantar é a chothabháil i gceart. Déantar na sonraí i gcomhad SAV a chatagóiriú sna rannáin seo a leanas:

### Ceanntásc comhaid
Tá sé comhdhéanta de 176 beart. Léiríonn na chéad 4 beart an teaghrán **$FL2** nó **$FL3** san ionchódú carachtar a úsáidtear don chomhad. Léiríonn na trí bhearta deiridh go bhfuil na sonraí sa chomhad comhbhrúite ag baint úsáide as **ZLIB**. Tosaíonn an chéad teaghrán 60 beart eile ** @(#) SPSS SONRAÍ COMHAD** agus socraíonn sé freisin an córas oibriúcháin agus an leagan SPSS a chruthaigh an comhad. Leanann an ceanntásc ar aghaidh ansin le réimsí sé dhigit, ina bhfuil líon na n-athróg in aghaidh an bhreathnaithe agus cód digite le haghaidh comhbhrú, agus críochnaíonn sé le sonraí carachtar a léiríonn dáta agus am cruthaithe agus lipéad comhaid.
### Taifid tuairisceora inathraithe
Tá seicheamh seasta réimsí sa taifead, ag rangú cineál agus ainm na hathróige mar aon le faisnéis formáidithe a úsáideann SPSS. Féadfaidh lipéad athróg suas le 120 carachtar agus suas le trí shonraíocht luacha in easnamh a bheith i ngach taifead athróg go roghnach.
### Lipéid luacha
The value labels are optional and stored in pairs of records with integer tags 3 and 4. Tá seicheamh péirí réimsí ar an gcéad taifead ar a bhfuil clib 3, gach péire ina bhfuil luach agus an lipéad luacha gaolmhar. Léiríonn an dara taifead ar a bhfuil clib 4 na hathróga a mbaineann an tacar luachanna/lipéad leo.
### Doiciméid
Single or multiple records with integer tag 6. Doiciméadú roghnach. Tá línte 80-charachtar.
### Taifid síneadh
Single or multiple records with integer tag 7. Soláthraíonn taifid sínte faisnéis ar féidir neamhaird a dhéanamh uirthi go sábháilte, ach a chaomhnaítear, i go leor cásanna, is féidir comhaid a scríobhann bogearraí níos nuaí chun comhoiriúnacht siar a chaomhnú. Tá clibeanna fochineála slánuimhreacha ar thaifid sínte.
### Críochnaitheoir an fhoclóra
Only record with integer tag 999. Scarann sé foclóir ó bhreathnuithe sonraí.
### Breathnuithe sonraí
Meastar go bhfuil na sonraí in ord breathnóireachta, m.sh. gach luach athraitheach don chéad bhreathnóireacht, agus gach luach don dara breathnóireacht ina dhiaidh sin, etc. Athraíonn formáid an taifid sonraí ag brath ar an gcód comhbhrú i dtaifead ceanntásca an chomhaid. Is féidir an chuid sonraí de chomhad .sav a dhí-chomhbhrú:
- **cód 0**: comhbhrúite le bytecode
- **cód 1**: comhbhrúite ag baint úsáide as comhbhrú ZLIB
 






## Tagairtí ##

* [Teaghlach Formáid Chomhaid Sonraí an Chórais SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)


