{
  "date": "2021-08-09",
  "keywords": [
"comhad cso",
"formáid comhaid cso",
"cad is comhad cso ann",
"comhad",
"sampla cso",
"síneadh comhad cso",
"síneadh",
"formáid",
"iso",
"Comhbhrú DAX"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid an CSO agus APIanna ar féidir leo comhaid CSO a chruthú agus a oscailt.",
  "title": "CSO - Íomhá Diosca Comhbhrúite ISO",
  "linktitle": "CSO",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-cs-gao"
}
},
  "lastmod": "2021-08-09"
}

## Cad is comhad CSO ann?

Is comhad íomhá ISO comhbhrúite é comhad leis an síneadh .cso. Is rogha eile í an Phríomh-Oifig Staidrimh ar mhodh comhbhrú DAX; ar a dtugtar freisin CISO; Ba é an chéad mhodh chun na comhaid [ISO](/compression/iso/) a chomhbhrú agus de ghnáth is é an modh is fearr chun rudaí PlayStation Inaistrithe a chartlannú. Úsáideann an fhormáid seo comhbhrú Deflate, ar féidir suas le naoi sraithe comhbhrú a áireamh. Úsáidtear bogearraí ar nós Prometheus agus YACC chun na híomhánna a chruthú.

## Formáid comhaid CSO

Ba í formáid comhaid an Phríomh-Oifig Staidrimh an chéad mhodh comhbhrú don ISO chun níos mó spáis cuimhne a shábháil. Rinneadh na feabhsuithe ó am go ham le haghaidh comhbhrú níos fearr. Tá an Phríomh-Oifig Staidrimh ag baint úsáide as comhbhrú Deflate le naoi leibhéal réamhshocruithe, de ghnáth, is féidir le gach leibhéal 2 bhloc KiB a láimhseáil ina n-aonar. Cé gur féidir leis na leibhéil is airde comhbhrú moill a chur ar amanna fada ualaigh i mbogearraí a bhraitheann go mór ar shruthú dioscaí, is féidir leis na leibhéil níos ísle comhbhrú suntasach a dhéanamh freisin.

### Struchtúr comhaid CSO

Tá ceanntásc 24 beart, bloic sonraí agus tábla innéacs i bhformáid comhaid an CSO. Glactar leis an endian beag do réimsí níos mó ná beart. Tugtar endianness ailtireachta PlayStation Inaistrithe thíos.

#### Ceanntásc

| Fritháireamh (bearta) | Ainm | Méid (bearta) | Cuspóir |
----------|----------|--------------|---------|
| 0x0 | Draíocht | 4 | CISO i gcónaí, nó 0x4F534943 nuair a léitear é mar shlánuimhir 32-giotán. Úsáidtear an réimse seo chun comhad CSO a shainaithint. Tabhair faoi deara gur féidir leis an réimse seo a bheith difriúil do na díorthaigh eile den CSO, mar shampla, d'úsáid ZSO an cód draíochta ZISO. |
| 0×4 | Méid ceanntásca | 4 | Maidir le formáid comhaid bhunaidh v1 an Phríomh-Oifig Staidrimh, ní thugtar aird ar an réimse seo agus mar sin ní gá a bheith cruinn. Mar sin féin, éilíonn an fhormáid v2 agus ZSO go mbeadh an réimse seo i gcónaí 0x18 (24 bytes). |
| 0×8 | Méid neamh-chomhbhrúite | 8 | Méid an ISO neamh-chomhbhrúite bunaidh i mbearta. |
| 0×10 | Méid bloc | 4 | Méid gach bloc sonraí i mbearta roimh chomhbhrú. De ghnáth 2048 beart, comhionann le méid gach earnála ISO 9660. |
| 0x14 | Version | 1 | The version of the file format in use. For the "v1" format, the value can be either 0 or 1. Maidir leis an bhformáid v2, ní mór gur 2 é seo. Ina theannta sin, éilíonn formáid ZSO gur 1 é seo. |
| 0×15 | Ailíniú innéacs | 1 | Ailíniú gach iontráil innéacs, sonraithe i giotáin. |
| 0×16 | Curtha in áirithe | 2 | Níl an réimse seo in úsáid. San fhormáid v1, déantar neamhaird den réimse seo agus d'fhéadfadh luachanna treallach a bheith ann. San fhormáid v2, caithfidh an réimse seo a bheith nialas. |

#### Innéacs tábla

Tá roinnt iontrálacha 4-bheart sa tábla innéacs, a léiríonn suíomh gach bloc sonraí, agus iontráil dheireanach bhreise a dhíríonn ar dheireadh an chomhaid.
Seo a leanas ábhar gach iontrála:
| Giotán | Fad | Masc | Ainm | Cuspóir |
-----|-----|----|-------|------------|
| 0 | 31 | 0x7FFFFFF | Seasamh | Nuair a aistrítear an réimse seo ar chlé ag an ailíniú innéacs a thugtar sa cheanntásc, tugann sé amach an suíomh ina dtosaíonn an bloc sonraí. |
| 31 | 1 | 0x80000000 | Cineál comhbhrúite | Tá séimeantaic den chineál céanna ag formáid ZSO, ach is ionann 0 agus LZ4 in ionad Deflate. San fhormáid v2. Meastar go hintuigthe go bhfuil an bloc neamh-chomhbhrúite má tá méid an bhloic cothrom le nó níos mó ná an méid bloc atá sonraithe sa cheanntásc comhaid. |

#### Bloic sonraí

Cuimsíonn na bloic sonraí na sonraí neamh-chomhbhrúite nó comhbhrúite. Ríomhtar méid bloc trína shuíomh a fháil, agus ansin é a dhealú ó shuíomh an bhloc seo a leanas. Má tá an t-ailíniú innéacs níos mó ná nialas, is dócha go bhfuil an méid bloc níos mó ná na sonraí a shealbhaíonn sé.


## Tagairtí 

* N / A


