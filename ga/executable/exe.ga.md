{
  "date": "2021-06-30",
  "keywords": [
"comhad exe",
"Formáid comhaid exe?",
"Cad é an comhad exe?",
"comhad",
"shampla exe",
"síneadh comhad exe",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Is comhad inrite Microsoft é comhad .exe a reáchtáiltear ar Windows OS. Tuilleadh eolais faoi fhormáid comhaid EXE.",
  "title": "Cad is Comhad Inrite EXE ann?",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-gae"
}
},
  "lastmod": "2021-06-30"
}

## Cad is comhad EXE ann?

Tá an focal EXE gearr do **inrite**. Is clár é comhad .exe is féidir a fhorghníomhú ar chóras oibriúcháin Microsoft Windows. Foilsíonn forbróirí feidhmchlár a gcuid clár do Windows OS den chuid is mó i bhformáid inrite mar chomhaid exe. Is é an fhormáid comhaid caighdeánach é chun feidhmchláir a rith ar Windows. Tá **Setup.exe**, **Install.exe** agus **cmd.exe** ar roinnt ainmneacha coitianta agus eolach ar chomhaid EXE.

## Formáid Comhaid EXE

Tugadh isteach tiomsaitheoirí MS-DOS agus tá an teorannú cuimhne 64K ag na samhlacha cuimhne. Is é an coincheap ginearálta ná cláir dheighleogacha éagsúla a shocrú sa LAP x86 (CS, DS, ES, SS) chun na codanna difriúla nó na míreanna céanna a dhíriú, rud a cheadaíonn céimeanna éagsúla rochtana ar chuimhne. Seo a leanas roinnt samhlacha cuimhne ar leith:

- **Bídeach**: Tá gach rochtain chuimhne 16-giotán (cláir na ndeighleog gan athrú). Táirgeann comhad .COM in ionad comhad .EXE.
- **Beag**: Tá gach rochtain chuimhne 16-giotán (cláir na míre gan athrú).
- **Dlúth**: Áirítear le seoltaí sonraí deighleog agus fritháireamh, athlódáil na gclár DS nó ES ar rochtain agus ceadaíonn sé suas le 1M de shonraí. Ní athraíonn rochtain cód an clár CS, rud a cheadaíonn 64K de chód.
- **Meánach**: Áirítear le seoltaí cód seoladh na míre, CS a athlódáil ar rochtain agus ceadú suas le 1M de chód. Ní athraíonn rochtain sonraí na cláir DS agus ES, rud a cheadaíonn 64K sonraí.
- **Mór**: Is péirí (deighleog, fritháireamh) iad na seoltaí cód agus sonraí araon, ag athlódáil seoltaí na mírlíne i gcónaí. Tá an spás cuimhne beart 1M ar fad ar fáil le haghaidh cód agus sonraí araon.
- **Ollmhór**: Mar an gcéanna leis an tsamhail mhór, agus uimhríocht bhreise á giniúint ag an tiomsaitheoir chun rochtain a cheadú ar eagair atá níos mó ná 64K.

Caithfidh na forbróirí a chinneadh cén tsamhail ba cheart a roghnú agus comhad exe á chruthú.

### Formáid Chomhaid EXE Inaistrithe

Tá roinnt ceanntásca faisnéise san fhormáid comhaid inrite iniompartha (PE), seo a leanas liosta na gceanntásca:

- ** Ceanntásc DOS **: Cinntíonn ceanntásc MS-DOS comhoiriúnacht ar gcúl, nó meath galánta ar chineálacha nua comhaid.
- ** Ceanntásc PE**: Ag fritháireamh 60 (0x3C) ó thús cheanntásc an DOS tá pointeoir chuig ceanntásc an Chomhaid PE
- **Ceanntásc COFF**: Tá roinnt faisnéise sa cheanntásc COFF atá úsáideach d'inrite, agus roinnt faisnéise atá níos úsáidí do chomhad oibiachta.
- ** Ceanntásc Roghnach PE**: Tarlaíonn Ceanntásc Roghnach PE díreach i ndiaidh an chinnteidil COFF, agus léiríonn roinnt foinsí fiú go bhfuil an dá cheanntásc mar chuid den struchtúr céanna.
- **Tábla Rannóige**: Díreach tar éis an Cheanntásca Roghnach Corpoideachas aimsímid tábla rannáin. Tá sraith de struchtúir IMAGE_SECTION_HEADER sa tábla rannáin.
- **Rannóga Inmhínithe**: Is féidir spás a shábháil sa chuimhne trí chód leabharlainne a mhapáil i níos mó ná próiseas amháin.

## An féidir leat comhad EXE a rith ar Mac?

Ní úsáidtear comhaid exe mar earraí inrite ar Mac OS. Mar sin féin, más mian leat comhad exe a reáchtáil ar Mac OS, is féidir na modhanna seo a leanas a úsáid.

 1. **Fíon** - Is é fíon an réiteach foirfe do dhaoine ar mian leo a bhfeidhmchláir ríomhaire a úsáid ar chórais Mac. Is acrainm é a sheasann do Wine Is Not A Emulator, a chiallaíonn. Cruthaíonn Fíon an timpeallacht chéanna d’eolairí agus a úsáideann Microsoft ionas gur féidir leat d’fheidhmchlár Windows a rith agus é á úsáid.
 2. **Meaisíní Fíorúla** - Cruthaigh Meaisín Fíorúil Windows ag baint úsáide as Deasc Comhthreomhar nó Bosca Fíorúil VM agus rith d’iarratas laistigh den mheaisín fíorúil.
 3. ** Boot Camp** - Ligeann suiteáil agus cumrú Windows Boot Camp ar Mac OS duit an meaisín Windows OS a rith ar Mac.

## Tagairtí

* [.exe- le Wikipewdia](https://en.wikipedia.org/wiki/.exe)

* [x86 Disassembly/Comhaid Inrite Windows](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


