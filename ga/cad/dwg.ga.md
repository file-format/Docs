{
  "date": "2020-03-16",
  "keywords": [
"DWG",
"Formáid Chomhaid",
"CAD",
"Oscail",
"Cruthaigh"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid DWG agus APIanna ar féidir leo comhaid DWG a chruthú agus a oscailt.",
  "title": "Formáid Comhaid DWG",
  "linktitle": "DWG",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dw-gag"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad DWG ann?

Is ionann comhaid le síneadh DWG agus comhaid dhénártha dílseánaigh a úsáidtear chun sonraí dearaidh 2T agus 3D a bheith iontu. Cosúil le DXF, ar comhaid ASCII iad, is ionann DWG agus formáid dhénártha comhaid le haghaidh líníochtaí CAD (Dearadh Ríomhchuidithe). Tá íomhá veicteora agus meiteashonraí ann chun ábhar comhaid CAD a léiriú. Tá lucht féachana saor in aisce ar fáil chun féachaint ar chomhaid DWG ar Chóras Oibriúcháin Windows ar nós DWG TrueView saor in aisce Autodesk. Tá feidhmchláir tríú páirtí eile ann freisin a thacaíonn le comhaid DWG a bhaint amach. Tá faisnéis cruthaithe ag úsáideoirí i gcomhaid DWG agus áirítear leo:

* Dearthaí

* Sonraí geoiméadracha

* Léarscáileanna agus grianghraif


Úsáideann ailtirí, innealtóirí agus dearthóirí an fhormáid seo go forleathan chun críocha dearaidh éagsúla.

## Stair Ghearr ##

DWG file format has evolved with the time since its formal introduction in 1982. Seo a leanas forbhreathnú gairid ar imeachtaí an ama atá caite ó thaobh na staire de.

**1982:** Thug Autodesk ceadúnas don fhormáid comhaid DWG , a d’fhorbair Mike Riddle i 1970, mar bhunús do AutoCAD.

**1998:** Nuair a scaoileadh AutoCAD R14.01, chuir Autodesk fíorú comhad leis trí fheidhm ar a dtugtar DWGCHECK a ionchorpraíodh seiceála criptithe agus cód táirge, ar a dtugtar WaterMark le Autodesk, i gcomhaid DWG cruthaithe ag an gclár.

**2006:** D'athraigh Autodesk AutoCAD 2007, chun teicneolaíocht TrustDWG a chur san áireamh chun teaghrán téacs Autodesk DWG a leabú. Is DWG Iontaofa é an comhad seo a shábháil an t-iarratas Autodesk nó feidhmchlár ceadúnaithe Autodesk sna comhaid DWG. Ba é an cuspóir a bhí leis seo cabhrú le húsáideoirí bogearraí Autodesk a chinntiú gur feidhmchlár Autodesk nó RealDWG a chruthaigh na comhaid seo, agus ba cheart go gcabhródh sé sin go cinnte le riosca neamhluí a laghdú.

## Struchtúr Comhaid ##

Tá DWG ar cheann de na formáidí comhaid a úsáidtear go forleathan i raon feidhmchlár agus tá struchtúr comhad láidir aige. Ós rud é gur formáid dhénártha comhaid é DWG, níl sé inléite ag an duine ar nós an ghnáthfhormáid chomhaid ASCII [DXF](/cad/dxf/). Cuimsíonn comhaid DWG faisnéis faoi chomhordanáidí na híomhá agus aon meiteashonraí a bhaineann leo de ghnáth. Tá [specifications](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf) iomlán de fhormáid comhaid DWG ar fáil le híoslódáil ag OpenDesign. Tá achoimre mar seo a leanas ar struchtúr comhaid formáid comhaid DWG.

**Ceanntásc**: Is éard atá i gceanntásc an chomhaid athróga Ceanntásca DWG agus faisnéis faoi Sheiceáil Iomarcaíochta Timthrialla (CRC) a úsáidtear chun earráidí a bhrath. Is veicteoir speisialaithe é gach fo-alt ina n-úsáidtear faid éagsúla giotán chun lipéid éagsúla a léiriú. Mar shampla, seasann an chéad 6 ghiotán den athróg Ceanntásc DWG don teaghrán leagain.

**Sainmhínithe Aicme:** D’fhéadfadh go mbeadh go leor ranganna i gcomhad DWG ag brath ar shainchuspóir an chomhaid .dwg. Eolas ar nós meiteashonraí ranga méid an limistéir sonraí ranga, uimhir ranga agus seiceálacha i dteannta le cinn eile.

**Teimpléad**: Tá sé seo roghnach agus le haghaidh leaganacha R15 agus R15, tá an chuid seo faoi bhun na rannóige Object Free Space.

**Stadáil**: Iarmhaítear na meiteashonraí agus iarshocrú le líon sonrach beart a fhágann go mbeidh na seanleaganacha bogearraí AutoCAD comhoiriúnach don fhormáid comhaid DWG nua.

**Sonraí Íomhá**: Braitheann na meiteashonraí don roinn seo ar an gcineál .dwg sonrach. I gcás úsáideoirí R14 agus R15, tá an chuid seo roghnach.

**Sonraí Réada**: Is éard atá i sonraí an oibiachta liosta iomlán d’eintitis tábla, iontrálacha foclóir, etc. a fhreagraíonn don liosta réad atá ann cheana féin.

**Léarscáil Réada**: Sonraítear suíomh gach oibiachta sa chomhad sa chuid seo den chomhad. Láimhseálann comhaid is ea an chuid is mó de na meiteashonraí sa chuid seo a bhfuil ról acu in aithint agus in ath-rindreáil an réad.

**Spás Saor ó Réada**: Tá an chuid seo roghnach do gach úsáideoir

**An Dara Ceanntásc**: dúblach de mhír cheanntásc an chomhaid i dtreo dheireadh an chomhaid DWG

## Tagairtí ##

* [Sonraíochtaí Formáid Comhaid DWG]( https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)

* [Sonraíocht an Chomhaid DWG]( https://www.scan2cad.com/blog/dwg/file-spec/)

* [DWG - Le Vicipéid]( https://ga.wikipedia.org/wiki/.dwg)


