{
  "date": "2021-04-23",
  "keywords": [
"Comhad RES",
"Conas comhad res a oscailt",
"cad is comhad res",
"síneadh",
"formáid",
"Formáid comhaid RES"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RES - C++ Script Acmhainní Tiomsaithe",
  "description": "Foghlaim faoi fhormáid comhaid RES le sampla RES agus APIanna ar féidir leo comhaid RES a chruthú agus a oscailt.",
  "linktitle": "RES",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-re-gas"
}
},
  "lastmod": "2021-04-23"
}

## Cad is comhad RES ann?
Is féidir leis an gcomhad a bhfuil iarmhír .res nó iarmhír air a bheith bainteach le go leor catagóirí formáid comhaid. Anseo táimid ag plé formáid comhaid RES arb é C++ Script Acmhainní Tiomsaithe é; comhad dénártha cruthaithe ag an Microsoft Resource Compiler (rc) ina bhfuil sonraí acmhainne; bunaithe ar a bhfuil sa chomhad sainmhínithe acmhainne; ábhartha dá thionscadal bogearraí tuismitheora. De ghnáth déantar an comhad .res a athfhormáidiú ina chomhad oibiachta acmhainne chun é a nascadh le comhad inrite feidhmchláir.

## Formáid comhaid RES
Baineann formáid comhaid RES leis an Microsoft Resource Compiler (rc). Uirlis is ea an tiomsaitheoir acmhainní a thiomsaíonn acmhainní amhail cúrsóirí, deilbhíní, biachláir agus boscaí dialóige a úsáideann d’fheidhmchlár. De ghnáth bíonn síneadh .res ag na comhaid acmhainne; ina bhfuil acmhainní, mar chúrsóirí, íomhánna, agus faisnéis faoin leagan. D’fhéadfadh comhad RES a bheith ina chomhad acmhainne 16 nó 32-giotán.
## Struchtúr comhaid acmhainne
Tá sraith iontrálacha acmhainne éagsúla i gcomhad acmhainní. Tá ceanntásc acmhainne agus sonraí ábhartha i ngach iontráil. De ghnáth déantar ceanntásc acmhainne a ailíniú le DWORD sa chomhad agus tá na nithe seo a leanas ann:

- A **DWORD** chun méid an cheannteidil acmhainne a shonrú
- A **DWORD** chun méid na sonraí acmhainne a shonrú
- An cineál acmhainne
- An t-ainm acmhainne
- Faisnéis acmhainne breise

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Acmhainní Tábla Luasaire
Is éard is tábla luasaire ann ná iontráil acmhainne i gcomhad RES gan ceanntásc grúpa. Sainmhíníonn an patrún **CELTABLEENTRY** gach iontráil sa tábla luasaire. D'fhéadfadh táblaí Iolrluasaire a bheith i gcomhad RES.

### Acmhainní Cúrsóra agus Deilbhíní
Cé go measann an córas gach deilbhín agus cúrsóir mar chomhad amháin, ach stóráiltear iad seo i gcomhaid RES mar ghrúpa acmhainní deilbhíní nó mar ghrúpa acmhainní cúrsóra. Tá formáidí comhaid na n-acmhainní deilbhín agus cúrsóra mar an gcéanna. Leanann ceanntásc grúpa acmhainne na deilbhíní aonair nó na comhpháirteanna grúpa cúrsóra sa chomhad .res.

### Acmhainní Bosca dialóige
Baintear amach bosca dialóige freisin mar iontráil acmhainne sa chomhad RES. Tá patrún ceanntásc bhosca dialóige amháin **DLGTEMPLATE** ann agus patrún **DLGITEMTEMPLATE** amháin do gach rialú sonrach sa bhosca dialóige. Míníonn na patrúin **DLGTTEMPlateEX** agus an **DLGITEMTEMPLATEEX** formáid acmhainní sínte an bhosca dialóige.

### Acmhainní Cló
Tá patrún **MENUHEADER** in acmhainn roghchláir ina dhiaidh sin patrún **NORMALMENUITEM** nó **POPUPMENUITEM**, patrún do gach mír roghchláir sa teimpléad roghchláir. Míníonn na patrúin **MENUEX_TEMPLATE_HEADER** agus an **MENUEX_TEMPLATE_ITEM** formáid acmhainní sínte roghchláir.

### Acmhainní Tábla Teachtaireachta
Tá tábla teachtaireachta comhdhéanta de théacs formáidithe le taispeáint mar theachtaireacht earráide nó i mbosca teachtaireachta. Is é an príomhphatrún in acmhainn tábla teachtaireachta an struchtúr **MESSAGE_RESOURCE_DATA**.

### Acmhainní Leagan
Is é an patrún is mó in acmhainn leagain ná an **VS_FIXEDFILEINFO**. Áirítear le patrúin breise an **VarFileInfo** chun sonraí a bhaineann le faisnéis teanga a stóráil, agus **StringFileInfo** le haghaidh faisnéise saincheaptha teaghrán.




## Tagairtí

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 

