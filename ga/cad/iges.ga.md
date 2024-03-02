{
  "date": "2020-03-16",
  "keywords": [
"Comhad IGES",
"Formáid Chomhaid",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid IGES agus APIanna ar féidir leo comhaid IGES a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid IGES",
  "linktitle": "IGES",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-ige-gas"
}
},
  "lastmod": "2020-07-28"
}

## Cad is comhad IGES ann?

Úsáidtear comhad le síneadh .iges chun faisnéis dearaidh a mhalartú idir feidhmchláir deartha ríomhchuidithe (CAD). Seasann IGES do Sonraíochtaí Malartaithe Grafaice Tosaigh. Áirítear léaráid chiorcaid, sreangfhráma, dromchla saorfhoirme, nó samhaltú soladach san fhaisnéis a mhalartaítear ag baint úsáide as IGES. Faigheann IGES a fheidhmchláir i líníochtaí innealtóireachta traidisiúnta, anailís samhlacha, agus feidhmeanna déantúsaíochta. Is féidir leis an bhformáid faisnéis dearaidh 2T nó 3D araon a mhalartú idir cláir CAD. Is féidir comhaid IGES a oscailt le roinnt feidhmeanna CAD mar Autodesk agus CADSoftTools ABViewer. Tá roinnt API ar fáil freisin chun comhaid IGES a oscailt agus a thiontú go ríomhchláraithe.

## Formáid Chomhaid IGES

Tá comhaid IGES i bhformáid téacs ASCII agus is féidir iad a oscailt in aon eagarthóir téacs chun a bhfuil sa chomhad a fheiceáil. Léirítear faisnéis téacsúil i gcomhad IGES i bhformáid Hollerith”. Is féidir na mílte líne a bheith i gcomhad coiteann IGES chun an fhaisnéis 2T nó 3T a léiriú is féidir a mhalartú de réir na formáide seo. Roinntear comhad IGES i gcúig chuid, sainaitheanta ag an litir chás uachtair ar leith sa 73ú colún. Is iad na hailt sin na rannáin `Tosaigh` (S), `Domhanda` (G), `Iontráil Sonraí` (D), `Sonraí Paraiméadar` (P), agus `Críochnaigh` (T). Déantar na hailt Iontrála Sonraí agus Sonraí Paraiméadair a ghiorrú go coitianta DE agus PD, faoi seach.

### Ceanntásc Comhad IGES

Tá faisnéis bhunúsach sna rannáin Tús agus Domhanda faoi:
 * Ainm an chomhaid agus a fhoinse
 * Teorainneoirí don rannán Sonraí Paraiméadar
 * Údar an chomhaid, agus faisnéis ghinearálta eile.

Seo a leanas na rannáin Tosaigh agus Domhanda ón doiciméad samplach ar Vicipéid.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
As can be seen, the start field contains human readable descriptions of the file, and my have any characters in columns 1-72, with the line ending with the section header and section line number. There must be at least 1 line of the Start section. The global section contains preprocessor data. It also must be present in the file and end with the G000000# format.

### Iontráil Sonraí (DE) agus Rannóg Sonraí Paraiméadar (PD).

#### Rannóg Iontrála Sonraí
Is éard atá i gcomhad IGES ná roinnt eintiteas ina bhfuil an fhaisnéis maidir le sonraí bunúsacha formáid comhaid IGES. Tá faisnéis ag aonán faoi ghnéithe éagsúla d’fhormáid sonraí IGES agus úsáidtear é le haghaidh líníochta. I measc na n-eintiteas a úsáidtear níos coitianta tá:
 * Ciorclán Arc
 * Cuar Ilchodach
 * Arc cónúil
 * Eitleán
 * Líne

Níl iontu seo ach roinnt bheag agus tá thart ar 150 eintiteas éagsúil san IGES. Sainaithnítear gach aonán le huimhir Chineáil mar:
 * CIRCULAR ARC(Cineál 100)
 * LÍNE (Cineál 110)

##### Airíonna an Aonáin

Tá na hairíonna seo a leanas ag gach aonán dearbhaithe.

|Ainm Réimse|Cur Síos|
---|---|
|Cineál Eintitis |Seo an cineál aonáin a bhfuil cur síos air. Mar shampla, cuireann 116 síos ar aonán Pointe.|
| Pointeoir PD |Tugann sé seo suíomh na sonraí aonáin seo sa rannán Sonraí Paraiméadar. Níl sa suíomh seo ach an uimhir líne laistigh den roinn PD a bhfuil an chéad líne de na sonraí aonáin seo aige.|
|Struchtúr |Aonán nialasach nó pointeoir don sainmhíniú. Neamhbhainteach i gcás fhormhór na n-eintiteas|
|Line Font Pattern| Number or pointer to line font pattern entity. Number signifies: * 0 Gan patrún sonraithe (réamhshocraithe) * 1 Soladach * 2 Daise * 3 Phantom * 4 Lárlíne * 5 Ponc |
|Leibhéal| Sonraíonn sé na leibhéil atá le baint leis an eintiteas seo. Ligeann sé d'aonán le feiceáil ar níos mó ná leibhéal amháin|
|Féach| Sonraítear roghanna féachana. Is iad seo: 0 Léiríonn infheictheacht agus tréithe comhionann i ngach radharc. Pointeoir Réamhshocraithe chuig an eintiteas View (Cineál 410) gur féidir é a fheiceáil ó Thagairt d’aonán View Infheicthe Associativity (Cineál 402, Foirm 3)
| pointeoir Maitrís Claochlaithe | Tagraíonn sé d'aonán maitrís trasfhoirmithe (Cineál 124) nó do nialas de réir réamhshocraithe (gan claochlú)|
|Comhlachas Taispeána Lipéad| Tagraíonn sé do Chomhlachú Taispeána Lipéid (Cineál 402, Foirm 5) a shainíonn an chuma ar an lipéad aonáin.|
|Uimhir Stádais| Tá ceithre roinn de dhá uimhir ann. 1-2: Stádas bán. Ceachtar 00 le haghaidh gnáth nó 01 i gcás bánaithe. 3-4: Lasc aonán fo-eintiteas: is é 00 do neamhspleách, 01 do chleithiúnaí fisiceach, 02 do chleithiúnaí loighciúil, agus 03 don dá cheann. 5-6: Bratach Úsáide Aonáin: tá ceachtar 00 le haghaidh Céimseata, 01 le haghaidh nótaí, 02 le haghaidh sainmhínithe, 03 le haghaidh Eile, 04 le haghaidh Loighciúil, 05 le haghaidh paraiméadracha 2T, agus 06 le haghaidh Céimseata Tógála. Ar deireadh, is é 7-8 an t-ordlathas, áit a léiríonn 00 ón mbarr anuas domhanda (úsáid tréithe an aonáin seo), is iarchur domhanda é 01 (ná húsáid saintréithe an aonáin seo), agus is é 02 úsáid airí ordlathais (úsáid Ordlathas Aonán (Cineál 406, Foirm 10) chun saintréithe na grúpála ordlathais a chinneadh).|
|Uimhir na Seicheamh| Sonraithe ag D#, áit arb í # uimhir na líne don roinn seo (ní ó bharr an chomhaid). Úsáidtear é seo freisin chun an t-aonán Iontrála Sonraí seo a chur in iúl.|
|Cineál Aonáin| tá sé sonraithe faoi dhó in aghaidh liostú eintitis|
|Uimhir Meáchain Líne| Sonraíonn sé tiús agus aonán á thaispeáint. Is é 1 an ceann is lú, is é 0 réamhshocraithe|
|Dathuimhir| Sonraítear dath an aonáin. Is iad na luachanna slánuimhir a cheadaítear: 0 Gan dath (réamhshocraithe) 1 Dubh 2 Dearg 3 Glas 4 Gorm 5 Buí 6 Mageanta 7 Cian 8 Bán |
|Uimhir Áireamh Líne Paraiméadar| Sonraítear líon na línte a ghlacann an t-aonán seo sa Roinn Sonraí Paraiméadair|
|Uimhir na Foirme| Léiríonn an fhoirm, nó léiriú an aonáin seo. Athruithe ar an gcaoi a ndéantar na sonraí paraiméadar a léirmhíniú. Is é 0| an réamhshocrú
|Réimse Forchoimeádta| Gan úsáid|
|Réimse Forchoimeádta| Gan úsáid|
|Lipéad Aonáin| Aitheantóir sonraithe i bhfeidhm - tá údar maith leis an gceart|
|Uimhir na Suibscríbhinne| Cáilitheoir uimhriúil don lipéad aonáin. Cruthaíonn an dá cheann le chéile aitheantóir uathúil don eintiteas|
|Seicheamh Uimhir Féach thuas. |D#+1 a bheidh anseo, toisc go sonraítear gach aonán ar dhá líne.|

#### Rannóg Sonraí Paraiméadar
Leanann an rannán Sonraí Paraiméadar an chuid Iontrálacha Sonraí. Liostaíonn sé na sonraí maidir le gach iontráil faoi seach agus liostaíonn sé paraiméadair don eintiteas bunaithe ar na teorainneacha a shonraítear sa roinn Domhanda (go hiondúil camóga go paraiméadair dheighilte agus leathchoilín chun deireadh a chur leis an liostú).


## Tagairtí
 * [IGES le WikiPedia]( https://en.wikipedia.org/wiki/IGES)

