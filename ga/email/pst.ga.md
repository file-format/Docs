{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PST - Outlook Personal Information Store Formáid Comhaid",
  "description": "Foghlaim faoi fhormáid comhaid PST agus APIs is féidir comhaid PST a chruthú agus a oscailt.",
  "linktitle": "PST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ps-gat"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad PST ann?

Is ionann comhaid le síneadh .pst agus Comhaid Stórála Pearsanta Outlook (ar a dtugtar Tábla Stórála Pearsanta freisin) a stórálann éagsúlacht faisnéise úsáideora. Stóráiltear faisnéis úsáideora i bhfillteáin de chineálacha éagsúla lena n-áirítear ríomhphoist, míreanna féilire, nótaí, teagmhálacha, agus roinnt formáidí comhaid eile. Úsáidtear comhaid PST chun sonraí ríomhphoist a chur i gcartlann as líne ar féidir iad a lódáil agus a fheiceáil níos déanaí i bhfeidhmchláir éagsúla.

## Sonraíochtaí Formáid Comhaid PST

Tá formáid comhaid PST [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546) ar fáil ó Microsoft mar cheadúnú paitinne saor in aisce agus neamh-inchúlghairthe tríd an nGealltanas Sonraíochta Oscailte.

### Cineál Formáidí PST

Déantar formáidí comhaid PST a chatagóiriú in dhá chineál bunaithe ar ionchódú an chineáil comhaid. Is formáidí comhaid níos sine iad comhaid PST ionchódaithe ANSI agus tacaítear leo ó Outlook 2002 agus leaganacha níos luaithe amháin. Tá teorainn mhéid uasta de 2 GB (2^^31^^ Beart) ag comhaid dá leithéid agus ní thacaíonn siad le Unicode. Baineann cineál formáid comhaid níos nua-aimseartha, bunaithe ar ionchódú Unicode, an teorainn ar mhéid an chomhaid amach agus is féidir leis uasmhéid sonraí de 50GB a bhaint amach.

### Eagraíocht Loighciúil Formáid Chomhaid PST

Ag bun formáid comhaid PST tá B-Tree a choinníonn sonraí curtha in eagar agus a cheadaíonn cuardaigh, rochtain sheicheamhach, cuir isteach, scriosadh srl. in am logartamach. Eagraítear struchtúr foriomlán comhad PST i dtrí shraith.

![Logical layers of a PST file](/email/PST-1.png "Logical layers of a PST file")

`Ciseal Bunachar Sonraí Nód (NDB)` - Tá sraith bhunachar sonraí nód suite ag an leibhéal is ísle de chomhad PST agus áirítear leis bunachar sonraí na nóid. Léiríonn na nóid seo saoráidí stórála ar leibhéal níos ísle formáid comhaid PST. Cuimsíonn ciseal NDB ceanntásc, faisnéis maidir le leithdháileadh comhad, bloic, agus BTrees (Nóid BTree agus Bloc BTree) ó thaobh na stórála. Tá Nóid agus Bloic de Chiseal NDB nasctha trí Sonraí BID atá ar cheann de na ceithre airí de thagairt Nód .i. NID (ID Nód), NID Tuismitheora, BID Sonraí (Bloc BID) agus Fonód BID.

`Liostaí, Táblaí agus Ciseal Airíonna -` Soláthraíonn ciseal LTP an tuiscint loighciúil ar choincheapa ardleibhéil ar bharr an NDB. Seachas eilimintí eile, is éard atá i gciseal LTP den chuid is mó Comhthéacs Maoine (PC) agus Comhthéacs Tábla (TC). Cnuasach réadmhaoine is ea PC, agus seasann TC do mhaitrís dhéthoiseach de bhailiúcháin maoine vs. láithreacht na maoine sin. Cur i bhfeidhm éifeachtach ríomhairí pearsanta agus TCanna, úsáideann an ciseal LTP dhá chineál struchtúir sonraí ar bharr Nód NDB:

* Heap On Node (HN) - is féidir sruth sonraí nód a fho-leithdháileadh i blúirí beaga, inathraithe.

* BTree on Heap (BTH) - Soláthraíonn BTH bealach áisiúil agus praiticiúil chun cuardach a dhéanamh trí ríomhairí pearsanta, a gcuirtear síos orthu thuas, a chuirtear i bhfeidhm mar BTHanna agus is é sin an fáth go gcuirtear i bhfeidhm é trí thógáil taobh istigh de struchtúr HN.


`Ciseal Teachtaireachtaí -` Cuirtear rialacha ardleibhéil agus loighic ghnó chun oibriú le comhaid PST i bhfeidhm ag an tsraith seo. Is éard a bhíonn mar thoradh ar aschur loighciúil na sraithe seo ná réada Fillteán, réada Teachtaireachta, réada Ceangaltáin agus Airíonna is féidir trí shraitheanna LTP agus NDB a chomhcheangal. Sainmhínítear rialacha agus ceanglais, ar gá iad a leanúint agus an t-ábhar PST á mhodhnú, ag an gciseal seo freisin.

### Eagrú Fisiciúil Formáid Chomhaid PST

Tá leibhéal ard eagrúcháin comhad PST mar a thaispeántar san fhigiúr thíos. Níl anseo ach forbhreathnú ar choincheapa éagsúla ó ghnéithe loighciúla de chomhad PST.

![Physical organization of the PST file format](/email/PST-2.png "Physical organization of the PST file format")


#### Eolas Ceanntásca PST

Tá struchtúr HEADER an chomhaid PST suite ag tús an chomhaid ag 0 fhritháireamh. Tá faisnéis meiteashonraí ann maidir leis an gcomhad PST agus an fhaisnéis ROOT chun rochtain a fháil ar struchtúir sonraí Chiseal an NDB a gcuirtear síos orthu thuas. Tá difríocht idir struchtúr HEADER do na leaganacha Unicode agus ANSI de PST File Formáid.

Tosaíonn an ceanntásc le focal draíochta 4-bheart **!BDN** arna léiriú ag beart (0x21, 0x42, 0x44, 0x4E). Tá uimhir draíochta 2-bheart eile, **SM** (0x53, 0x4D), suite ag fritháireamh 8 ó thús an chomhaid. Tá faisnéis faoin leagan (ANSI nó Unicode) ag fritháireamh 10 ó thús an chomhaid. Sonraíonn luach heicsidheachúlach (0x17) comhad Unicode PST agus seasann 0x0E nó 0x0F formáid comhaid ANSI.

| Réimse | Cur síos
---|---|
|dwMagic (4 beart)|NÍ MÓR é a bheith { 0x21, 0x42, 0x44, 0x4E } (!BDN)
|dwCRCPpartial (4 byte)|An luach CRC 32-giotán ar na 471 beart sonraí ag tosú ó wMagicClient (0ffset 0x0008)
|wMagicClient (2 beart)|NÍ MÓR é a bheith { 0x53, 0x4D }.
|wVer (2 beart)|Leagan formáid an chomhaid. NÍ MÓR an luach seo a bheith 14 nó 15 más comhad ANSI PST an comhad, agus NÍ MÓR a bheith 23 más comhad Unicode PST é.
|wVerClient   (2 bytes)|Client file format version. The version that corresponds to the format described in this document is 19. BA CHÓIR do chruthaitheoirí comhaid PST nua bunaithe ar an doiciméad seo an luach seo a thúsú go 19.
|bPlatformCreate (1 bheart)|Caithfear an luach seo a shocrú go 0x01.
|bPlatformAccess (1 beart)|Caithfear an luach seo a shocrú go 0x01.
|dwArchoimeád (8 mbeart)|
|bidUnused (8 bytes Unicode amháin)|Cuireadh stuáil neamhúsáidte leis nuair a cruthaíodh formáid comhaid Unicode PST.
|bidNextP (Unicode: 8 bytes; ANSI: 4 bytes)|An chéad leathanach eile CFG. Tá cuntar speisialta ag leathanaigh chun luachanna bidIndex a leithdháileadh. Leithdháiltear luach bidIndex le haghaidh CFGanna do leathanaigh ón gcuntar seo.
|bidNextB     (4 bytes ANSI only): |Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Le haghaidh tuilleadh sonraí, féach cuid 2.2.2.2.
|dwUnique (4 byte)|Is luach é seo a mhéadaíonn go mona-tonach agus a athraítear gach uair a athraítear struchtúr HEADER an chomhaid PST. Is é feidhm an luacha seo luach uathúil a sholáthar, agus a chinntiú go bhfuil na CRCanna HEADER difriúil tar éis gach modhnú ceannteidil.
|rgnid[](128 beart)|Eagar seasta de 32 NID, gach ceann ag freagairt do cheann amháin de na 32 NID_TYPE (NID_TYPE, NID_TYPE_NORMAL_FOLDER, NID_TYPE_SEARCH_FOLDER, NID_TYPE_NORMAL_MESSAGE, NID_TYPE_ASSAGE)
|qwUnused (8 beart)|Spás gan úsáid; NÍ MÓR a shocrú go nialas. Formáid comhaid Unicode PST amháin.
|fréamh (Unicode: 72 beart; ANSI: 40 beart) | Struchtúr Fréamh (Roinn 2.2.2.5).
|dwAilíniú (4 beart)|Bearta ailínithe neamhúsáidte; NÍ MÓR a shocrú go nialas. Formáid comhaid Unicode PST amháin.
|rgbFM (128 bytes)|Fap FMa thite. Ní úsáidtear é seo a thuilleadh agus NÍ MÓR é a líonadh le 0xFF. BA CHÓIR do léitheoirí neamhaird a dhéanamh de luach na mbeart seo.
|rgbFP (128 bytes)|FPMap neamhcheadaithe. Ní úsáidtear é seo a thuilleadh agus NÍ MÓR é a líonadh le 0xFF. BA CHÓIR do léitheoirí neamhaird a dhéanamh de luach na mbeart seo.
|bSentinel (1 beart)|NÍ MÓR é a shocrú go 0x80.
|bCryptMethod (1 beart)|Léiríonn sé conas a dhéantar na sonraí laistigh den chomhad PST a ionchódú. NÍ MÓR é a shocrú go ceann de na luachanna réamhshainithe (NDB_CRYPT_NONE, NDB_CRYPT_PERMUTE, NDB_CRYPT_CYCLIC).
|rgbArchoimeád (2 beart)| Curtha in áirithe; NÍ MÓR a shocrú go nialas.
|bidNextB (8 beart)|Léiríonn an chéad luach CFG eile atá ar fáil. Formáid comhaid Unicode PST amháin.
|bidNextB     (Unicode ONLY: 8 bytes)|Next BID. This value is the monotonic counter that indicates the BID to be assigned for the next allocated block. BID values advance in increments of 4. Le haghaidh tuilleadh sonraí, féach cuid 2.2.2.2.
|dwCRCFull (4 byte)|An luach CRC 32-giotán ar na 516 beart sonraí ag tosú ó wMagicClient go bidNextB, san áireamh. Formáid comhaid Unicode PST amháin.
|ullArchoimeád (8 mbeart)|Ar cosaint; NÍ MÓR a shocrú go nialas. Formáid comhaid ANSI PST amháin.
|dwArchoimeád (4 beart)|Ar cosaint; NÍ MÓR a shocrú go nialas. Formáid comhaid ANSI PST amháin.
|rgbReserved2 (3 beart)|
|b forchoimeádta (1 beart) |
|rgbReserved3 (32 beart) |

### Cosaint Sonraí ###

Ar mhaithe le slándáil, is féidir comhaid PST a chosaint ag pasfhocal freisin a éilíonn ar an bhfeidhmchlár luchtaithe pasfhocal a chur i bhfeidhm sular féidir féachaint air. Stóráiltear an pasfhocal a chuirtear i bhfeidhm ar an gcomhad PST sa stór teachtaireachtaí. Mar sin féin, ní sholáthraíonn sé seo cosaint sonraí láidir mar is féidir an pasfhocal a bhaint as na huirlisí atá ar fáil. Chomh maith leis sin, ní úsáidtear pasfhocal sonraithe ag an úsáideoir mar chuid den eochair chun halgartaim siffr a ionchódú agus a dhíchódú. Dá bhrí sin, níl aon tairbhe as sonraí a chosaint a mbeidh rochtain ag páirtithe neamhúdaraithe orthu. Déanann stóráil pasfhocail mar hash CRC-32 den teaghrán bunaidh freisin gur modh lag é do shlándáil sonraí i gcoinne cur chuige brúidiúil.

## Tagairtí ##

* [Formáid Comhaid Fillteáin Phearsanta Outlook (.pst)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)

* [Sonraíochtaí Formáid Comhaid an Fhillteáin Phearsanta](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)


