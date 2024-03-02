{
  "date": "2021-06-30",
  "keywords": [
"comhad mst",
"formáid comhaid mst",
"Cad is comhad mst ann",
"comhad",
"mst shampla",
"síneadh comhad mst",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid MST agus APIanna ar féidir leo comhaid MST a chruthú agus a oscailt.",
  "title": "MST - Comhad Pacáiste Suiteálaí Windows",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-gat"
}
},
  "lastmod": "2021-06-30"
}

## Cad is comhad MST ann?
Úsáidtear na comhaid le síneadh .mst chun ábhar pacáiste MSI a athrú. Úsáideann riarthóirí córais iad go coitianta chun na socruithe saincheaptha a chur i bhfeidhm ar chomhad MSI atá ann cheana féin. Úsáidtear na comhaid MST mar aon leis an bpacáiste bunaidh MSI ina gcórais dáileacháin bogearraí ar nós polasaithe grúpa. Úsáidtear comhaid MST go ginearálta i bhforbairt bogearraí agus i dtástáil chun a gcuid leaganacha de na bogearraí atá á bhforbairt a chumrú.

## Formáid comhaid MST
Úsáidtear comhad MST nó Transform chun na roghanna suiteála a bhailiú do chláir a úsáideann an Suiteálaí Microsoft Windows i gcomhad. Úsáidtear na comhaid seo go coitianta ar líne ordaithe an Suiteálaí (MSIEXEC.EXE), nó úsáidtear iad i mBeartas Grúpa maidir le suiteáil bogearraí; i bhfearann Microsoft Active Directory. Is féidir na comhaid MST a úsáid freisin le suiteálaithe inrite fillte. Is cás ginearálta é gur mian le duine paraiméadair na n-orduithe a chur ar aghaidh chuig an suiteálaí fillte. Chun é sin a dhéanamh, beidh comhad MST uait a chuireann an t-airí WRAPPED_ARGUMENTS leis an tábla réadmhaoine. Ní féidir na comhaid seo a chruthú ná a chur in eagar le heagarthóirí ginearálta. Tá uirlisí sonracha ar fáil chun na críche seo.

### Conas comhaid MST a úsáid?
Is féidir na comhaid MST a ghiniúint trí úsáid a bhaint as uirlisí éagsúla agus go ginearálta úsáidtear Ocra chun comhaid MST a ghiniúint. Ansin is féidir socruithe a shaincheapadh de réir an ghá agus iad a shábháil ag suíomh ar leith. Ina dhiaidh sin is féidir na comhaid MST a úsáid i gcomhar le comhaid MSI. Más mian leat na comhaid seo a thástáil; bain úsáid as an chomhréir seo a leanas ar an líne ordaithe

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS maoin

Is féidir leat maoin **TRANSFORMS** suiteálaí Windows a úsáid freisin, arb é atá ann i ndáiríre liosta de na claochluithe a chuireann an suiteálaí i bhfeidhm agus an pacáiste á shuiteáil. Déanann an suiteálaí na trasfhoirmeoirí a fhorghníomhú san ord céanna agus atá siad liostaithe san airí TRANSFORM. Is féidir Trasfhoirmeacha a shonrú de réir ainm comhaid le síneadh .mst nó cosán iomlán. Chun níos mó ná claochluithe amháin a shonrú, scar gach ainm comhaid nó leathstad mar shampla seo a leanas.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Tagairtí 

* [Comhaid Trasfhoirmithe MST]( https://www.exemsi.com/documentation/mst-transformation-files/)

* [maoin TRANSFORMS]( https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



