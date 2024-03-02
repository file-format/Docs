{
  "date": "2019-12-12",
  "keywords": [
"PLÉ",
"comhad",
"síneadh",
"formáid",
"Formáid comhaid 3d saor in aisce,"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid PLY agus APIanna ar féidir leo comhaid PLY a chruthú agus a oscailt.",
  "title": "PLY - Polagán Formáid Chomhaid 3D",
  "linktitle": "PLY",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-pl-gay"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad PLY ann?

Seasann PLY, Formáid Chomhaid Polagán, do fhormáid comhaid 3D a stórálann rudaí grafacha a gcuirtear síos orthu mar bhailiúchán polagán. Ba é cuspóir na formáid comhaid seo ná cineál comhaid simplí agus éasca a bhunú a bheadh ginearálta go leor le bheith úsáideach do raon leathan samhlacha. Tagann formáid comhaid PLY mar ASCII chomh maith le formáid Dénártha le haghaidh stórála dlúth agus le haghaidh coigilt agus luchtú tapa. Úsáideann feidhmchláir éagsúla an fhormáid comhaid a thugann tacaíocht do léamh comhaid 3D.

Déantar cur síos ar réada i bhformáid PLY le cnuasach rinn, aghaidheanna agus eilimintí eile, mar aon le hairíonna mar dath agus gnáththreo ar féidir a cheangal leis na heilimintí seo. I measc na n-airíonna eile is féidir a stóráil leis an réad tá:

* Normals dromchla

* comhordanáidí uigeachta

* trédhearcacht

* raon muiníne sonraí

* airíonna chun tosaigh agus ar chúl polagán


Is féidir le réad arna léiriú ag formáid PLY a bheith mar thoradh ar fhoinsí éagsúla cosúil le réada lámhdigitithe, réada polagán ó fheidhmchláir samhaltaithe, sonraí raoin, triantáin ó chiúbanna máirseála, sonraí tír-raoin agus samhlacha radaiochta.

## Stair Ghearr

Forbraíodh an fhormáid PLY sna 1990idí ag Greg Turk agus daoine eile i saotharlann grafaicí Stanford agus sin an fáth a dtugtar Formáid Triantán Stanford air freisin. Tá leagan 1.0 ag an bhformáid comhaid ó shin i leith agus ní dhearnadh aon mhodhnuithe eile.

## Formáid Chomhaid PLY

Is éard atá i réad simplí PLY ná bailiúchán eilimintí chun an réad a léiriú. Is éard atá ann liosta de thríreanna (x,y,z) de rinn agus liosta aghaidheanna ar innéacsanna iarbhír iad i liosta na rinn. Is dhá shampla d’eilimintí iad rinn agus aghaidheanna agus tá an dá eilimint seo i bhformhór an chomhaid PLY. Is féidir airíonna nua a chruthú freisin agus a cheangal le heilimintí réad, ach ba cheart iad seo a chur leis ar bhealach nach bhriseann seanchláir nuair a aimsítear na hairíonna nua seo. Is féidir airíonna den sórt sin a chaitheamh i leataobh trí fheidhmchláir a léamh freisin. Ina theannta sin, is féidir eilimintí nua a chruthú agus is féidir airíonna a shainiú leis an eilimint seo freisin.

### Struchtúr Comhaid

Seo a leanas struchtúr comhaid formáid comhaid PLY:

| Réimse
---|
| Ceanntásc an Chomhaid
| Liosta rinn
| Liosta Aghaidhe
|Liosta d'eilimintí eile

#### Struchtúr Samplach

Úsáidfimid an sampla seo a leanas thíos inár bplé ina dhiaidh sin le haghaidh codanna éagsúla de bhformáid comhaid PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Ceanntásc an Chomhaid

Is éard atá i gceanntásc formáid comhaid PLY ná téacs ASCII don bhformáid ASCII agus don fhormáid dhénártha. Aithnítear tús agus deireadh na rannóige ceanntásca le heochairfhocail sraithe agus ceanntásca deiridh. Ag tús an cheanntásc tá an sraith focal draíochta a úsáidtear chun formáid comhaid PLY a aithint ag léitheoirí. Taispeánann an chéad líne eile uimhir an leagain don chomhad seo. Tosaíonn tuairimí i bhformáid comhaid PLY le heochairfhocal nóta tráchta ag tús gach líne tráchta.

#### Eochairfhocal Eiliminte

Insíonn an eochairfhocal eilimint ansin cad atá taobh istigh den chomhad. Ina dhiaidh sin tá airíonna don chineál saineiliminte sin ina bhfuil a cineál maoine agus a ord maoine sonraithe ag gach maoin mar a thaispeántar thíos:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Sa sampla áirithe seo, tá 3 airí de chineál snámhphointe ag an eilimint rinn ar leith agus a n-ord sonraithe.

#### Cineálacha Cineálacha Sonraí

Tá dhá chineál de chineál sonraí ann a d’fhéadfadh a bheith ag maoin.

`Scalar`: Tá na cineálacha sonraí scálach mar a thaispeántar thíos:

|#Ainm|#Cineál|#Líon Beart
|char | carachtar |1
|uchar|carachtar gan síniú|1
| gearr | slánuimhir ghairid |2
|ushort| slánuimhir ghearr gan síniú|2
|int|Slánuimhir|4
|uint|Slánuimhir gan síniú|4
|snámhán|snámhán aon-chruinneas|4
| dúbailte | snámhán beachtas dúbailte | 8

`Liosta`: Tá foirm speisialta sainmhínithe maoine ann a úsáideann cineál sonraí an liosta. Tá sampla de seo ón gcomhad ciúb thuas:

`liosta maoine uchar int vertex_index`

Ciallaíonn sé seo go bhfuil san airí vertex_index ruabhr gan síniú ar dtús a insíonn cé mhéad innéacs atá sa mhaoin, agus ina dhiaidh sin liosta ina bhfuil an oiread sin slánuimhreacha. Tá gach slánuimhir sa liosta fad athraitheach seo ina innéacs d’ rinn.

## Tagairtí ##

* [Formáid Chomhaid PLY](http://paulbourke.net/dataformats/ply/)

* [PLY - Le Vicipéid](https://en.wikipedia.org/wiki/PLY_(file_format))


