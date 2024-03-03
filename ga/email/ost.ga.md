{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OST - Formáid Comhad Stórála Outlook",
  "description": "Foghlaim faoi fhormáid comhaid OST agus APIs is féidir comhaid OST a chruthú agus a oscailt.",
  "linktitle": "OST",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-os-gat"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad OST ann?

Léiríonn OST nó Comhaid Stórála As Líne sonraí bhosca poist an úsáideora sa mhód as líne ar an meaisín áitiúil ar chlárú le Exchange Server ag baint úsáide as Microsoft Outlook. Cruthaítear go huathoibríoch é ar an gcéad úsáid de Microsoft Outlook nuair a nasctar é leis an bhfreastalaí. Nuair a chruthaítear an comhad, déantar na sonraí a shioncronú leis an bhfreastalaí ríomhphoist ionas go mbeidh siad ar fáil as líne freisin i gcás dícheangailteachta ón bhfreastalaí ríomhphoist. Is féidir le comhaid OST míreanna bosca poist úsáideoirí cosúil le ríomhphoist, teagmhálacha, faisnéis féilire, nótaí, tascanna agus sonraí eile dá samhail. Is féidir le húsáideoirí ríomhphoist agus míreanna sonraí eile a chruthú i gcomhad OST fiú in éagmais nasc leis an bhfreastalaí, ach ní dhéanfar iad seo a shioncronú leis an bhfreastalaí. Nuair a bheidh an nasc bunaithe, déantar an comhad áitiúil a shioncronú leis an bhfreastalaí arís ionas go mbeidh an freastalaí agus an chóip áitiúil ag an leibhéal céanna faisnéise.

## Formáid Comhaid OST

The OST (Offline Storage Table) and [PST](/email/pst/) (Personal Storage Table) file format consist of the Personal Folder File (PFF) format that corresponds to storing user's emails, contacts and appointments. Data in a PFF file is stored in little-endian with all dates and times represented as FILETIME in UTC. [MS-PST] defines two types of PFF:

* Formáid ANSI 32-giotán

* Formáid Unicode 64-giotán


Tá formáid comhaid PST [specifications](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546), mar atá ar fáil ó Microsoft, infheidhme freisin maidir le formáid comhaid OST mar cheadúnú paitinne saor in aisce agus neamh-inchúlghairthe tríd an nGealltanas Sonraíochta Oscailte. Tá sé comhdhéanta de na heilimintí so-aitheanta seo a leanas:

* Fle header

* Sonraí ceanntásca Comhad

* Innéacs nód brainse

* Innéacs nód duille

* (Comhad) innéacs fhritháireamh

* (Mír) innéacs tuairisceora

* Tuairisceoirí áitiúla

* Cineál tábla Mír


### Eolas Ceannteidil

Tá struchtúr HEADER an chomhaid OST suite ag tús an chomhaid ar fhritháireamh 0. Tá faisnéis meiteashonraí ann faoin gcomhad OST agus faoin bhfaisnéis ROOT chun rochtain a fháil ar struchtúir sonraí Chiseal an NDB a gcuirtear síos orthu thuas. Tá difríocht idir struchtúr HEADER do na leaganacha Unicode agus ANSI d'Fhormáid Chomhaid OST.

Tosaíonn an ceanntásc le focal draíochta 4-bheart **!BDN** arna léiriú ag beart (0x21, 0x42, 0x44, 0x4E). Tá uimhir draíochta 2-bheart eile, **SM** (0x53, 0x4D), suite ag fritháireamh 8 ó thús an chomhaid. Tá faisnéis faoin leagan (ANSI nó Unicode) ag fritháireamh 10 ó thús an chomhaid. Sonraíonn luach heicsidheachúlach (0x17) comhad Unicode OST agus seasann 0x0E nó 0x0F formáid comhaid ANSI.

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

## Tagairtí

* [Formáid Comhaid Fillteáin Phearsanta Outlook (.ost)](https://learn.microsoft.com/en-us/openspecs/office_file_formats/ms-pst/141923d5-15ab-4ef1-a524-6dce75aae546)
* [Sonraíochtaí Formáid Comhaid an Fhillteáin Phearsanta](https://github.com/libyal/libpff/blob/main/documentation/Personal%20Folder%20File%20(PFF)%20format.asciidoc)
