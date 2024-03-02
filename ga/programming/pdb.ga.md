{
  "date": "2019-10-11",
  "keywords": [
"comhad pdb",
"pdb",
"síneadh",
"formáid",
"Cad is comhad pdf ann",
"Formáid comhaid pdb",
"meiteashonraí PDB"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid PDB - Comhad Bunachar Sonraí Cláir",
  "description": "Foghlaim faoi fhormáid comhaid PDB agus APIs ar féidir leo comhaid PDB a chruthú agus a oscailt.",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pd-gab"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad PDB ann?

Comhad le síneadh .pdb is ea comhad bunachar sonraí cláir ina bhfuil faisnéis dífhabhtaithe le haghaidh inrite tiomsaithe (EXE/DLL). Gintear comhaid PDB ag Microsoft Compilers nuair a chuirtear clár feidhmchláir le chéile i mód dífhabhtaithe. Is féidir le láithreacht comhad PDB cuidiú le hinnealtóireacht droim ar ais inrite mar go bhfuil faisnéis shuntasach ann faoi shiombail uile na modúl. Is ar an gcúis sin a choimeádtar na comhaid seo ar leithligh ón inrite deiridh. Is féidir le [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) de chuid Microsoft comhad PDB a oscailt chun faisnéis a fháil ar nós poiblí agus easpórtálacha, siombailí domhanda, siombailí áitiúla, cineál sonraí, comhaid foinse agus uimhreacha líne.

## Formáid Comhaid PDB

Is é PDB formáid comhaid dílseánaigh Microsoft agus níl sé doiciméadaithe go hoifigiúil in áit ar bith fós. Mar sin féin, tá doiciméadú tosaigh ar fáil [here](https://github.com/Microsoft/microsoft-pdb) agus is féidir tagairt a dhéanamh dó.

### Sruthanna PDB

Is éard atá i gcomhaid PDB ná sruthanna iolracha ina bhfeidhmíonn gach sruth mar chomhad aonair fíorúil agus ina bhfuil faisnéis. Is féidir le scríbhneoirí comhad PDB scríobh chuig na comhaid seo agus ní thugtar an comhad chun críche go dtí go n-eisítear gealltanas sainráite. Is féidir le tiomsaitheoir leanúint ar aghaidh ag scríobh chuig comhad PDB ach ní dhéanfaidh sé gealltanas ach amháin má thiomsaíonn an cód úsáideora go léir go rathúil. Tá na sruthanna seo a leanas i gcomhad PDB:

|Uimh. an tSrutha |Ábhair |Cur síos gairid|
---|---|---|
|1| Pdb (ceanntásc) |Faisnéis faoin leagan, agus faisnéis chun an PDB seo a nascadh leis an EXE|
|2| Tpi (bainisteoir cineáil) |Gach cineál a úsáidtear san inrite.|
|3| Dbi (faisnéis dífhabhtaithe) |Coinníonn sé ranníocaíochtaí na rannóige, agus liosta de 'Modhanna'|
|4| Mapa Ainm| Tá tábla teaghrán hashed|
|4-(n+4)| n Mod's (Eolas modúil)| Coinníonn gach sruth Mod siombailí agus uimhreacha líne le haghaidh tiomsú amháin|
|n+4| Siombail dhomhanda hash| Innéacs a cheadaíonn cuardach i siombailí domhanda de réir ainm|
|n+5| Siombail phoiblí hash| Innéacs a cheadaíonn cuardach i siombailí poiblí de réir seoltaí|
|n+6| Taifid siombailí| Taifid siombailí iarbhír de shiombailí domhanda agus poiblí|
|n+7| Cineál hash| Hash a úsáideann an sruth TPI.|

Cuimsíonn gach sruth i gcomhad PDB roinnt leathanach nach gá a bheith uimhrithe i ndiaidh a chéile.

### ceanntásc PDB

Tá comhad PDB ann le Ceanntásc arb é atá ann síniú chun an fhormáid shonrach a shainaithint agus a bhailíochtú. Braitheann fad an tsínithe ar an bhformáid PDB. Féadfaidh an ceanntásc a bheith níos faide ná leathanach amháin.

### Meiteashonraí PDB
The PDB metadata is responsible to recognize all of the component streams, giving the length, and sequence of pages for each stream. Orders are given to streams consecutively; starting with 0. Tá sruth fréimhe neamh-ordaithe ann freisin, ina bhfuil cuid de na meiteashonraí.

## Tagairtí
 * [PDB - Vicipéid](https://ga.wikipedia.org/wiki/Program_database)
 * [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

