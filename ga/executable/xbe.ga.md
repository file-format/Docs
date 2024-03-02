{
  "date": "2021-08-31",
  "keywords": [
"Comhad xbe",
"Formáid comhaid xbe",
"Cad is comhad xbe ann",
"comhad",
"sampla xbe",
"Síneadh comhad xbe",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid XBE agus APIs ar féidir leo comhaid XBE a chruthú agus a oscailt.",
  "title": "XBE - iOS Comhad Pacáiste Iarratais",
  "linktitle": "XBE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-xb-gae"
}
},
  "lastmod": "2021-08-31"
}

## Cad is comhad XBE ann?
Is feidhmchlár inrite é comhad a bhfuil síneadh .xbe aige ó diosca físchluiche Xbox. Is iad na comhaid XBE na príomhchomhaid a fhorghníomhaítear sa Chóras Xbox agus níl siad ceaptha a oscailt go hiondúil ar ríomhaire, ach is féidir iad a oscailt ar ríomhaire ag baint úsáide as clár aithrise Xbox. De ghnáth is forbróirí cluiche a chruthaíonn na comhaid seo, agus ansin sínithe ag Microsoft. Tá struchtúr an chomhaid cosúil le comhaid Windows PE, ach cuirtear roinnt athruithe tábhachtacha de réir na socruithe XBox i bhfeidhm chun é a dhéanamh in rith ag XBox.

## Formáid comhaid XBE
Tá an comhad XBE comhdhéanta de cheanntásc íomhá, bailiúchán ceanntásca rannóg, teastas, snáithe sonraí stórála áitiúla, bailiúchán de leaganacha leabharlainne, Microsoft giotánmap, agus na hailt ina bhfuil an cód agus acmhainní.

### Ceanntásc Íomhá
Cuimsíonn an ceanntásc íomhá an fhaisnéis a mhíníonn cá háit a bhfuil na comhpháirteanna eile den inrite suite laistigh den chomhad, agus conas ba cheart an inrite a chóireáil agus a luchtú.

### Tábla TLS
Is éard atá sa Tábla TLS an fhaisnéis go léir a theastaíonn ón XBE chun stóráil áitiúil snáithe a chur ar bun i gceart. Go bunúsach tá sé uathúil don Eolaire TLS atá le fáil i gcomhaid PE32, agus is féidir é a chóipeáil go díreach as sin. Féadfar an tábla seo a fhágáil ar lár, mura n-úsáideann an comhad XBE aon stóráil snáithe-áitiúil, agus an réimse faoi seach sa cheanntásc íomhá socraithe go nialas.

| Fritháireamh | Méid | Ainm | Cur Síos |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Sonraí Amh Tosaigh | Seoladh iomlán (.i. ní RVA) ar cuireadh tús leis na sonraí athróg TLS in íomhá an chláir. |
| 0x0004 | 0x0004 | Amh Sonraí Deireadh | Seoladh iomlán (.i. ní RVA) de chríoch na sonraí athróg TLS in íomhá an chláir. |
| 0x0008 | 0x0004 | Seoladh an Innéacs | Seoladh iomlán (ie ní RVA) den athróg Innéacs TLS. |
| 0x000C | 0x0004 | Seoladh na nAisghlao | Seoladh iomlán (ie ní RVA é) an tábla feidhmeanna aisghlao TLS ar cuireadh deireadh leis ar bhealach neamhní. |
| 0x0010 | 0x0004 | Méid Líon Nialais | Líon na mbeart tar éis na sonraí amh ba cheart a shocrú go nialas sa chuimhne. |
| 0x0014 | 0x0004 | Tréithe | Cur síos ar ailíniú. |

### Teastas

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- An t-am agus an dáta ar cruthaíodh an deimhniú
- Aitheantas Teidil
- Ainm teidil
- Aitheantais teidil eile
- Cineálacha meán ceadaithe ónar féidir an inrite a rith (HD, DVD, CD, etc.)
- Réigiún cluiche
- Rátálacha cluiche
- Uimhir diosca
- Leagan
- Eochairshonraí LAN amh a úsáidtear le haghaidh Nasc an Chórais
- Síniú príomhshonraí amh (a úsáidtear chun cluichí a shábháil)
- Eochracha síniú malartach
- Méid bunaidh an deimhnithe
- Ainm na seirbhíse ar líne (níl sé i láthair sna míreanna inrite go luath)
- Bratacha slándála ama a rith (níl siad i láthair sna míreanna inrite luath)
 
### Cineálacha meán ceadaithe
Cineálacha meán a cheadaítear leis an inrite a rith ó. Tá na luachanna seo a leanas ar eolas:
| Cineál meán | Luach |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Ailt
Cuirtear na hailt in iúl ag na ceannteidil rannáin. Tosaíonn na ceanntásca rannáin díreach tar éis an deimhnithe agus tá faisnéis iontu nuair a bhíonn na hailt iarbhír sa chomhad. Bíonn ar a laghad dhá chuid i gcónaí in inrite Xbox:
- .téacs
- .rdata


## Tagairtí 

* [Xbe - XBox Inrite](https://xboxdevwiki.net/Xbe)



