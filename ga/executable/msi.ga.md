{
  "date": "2021-06-30",
  "keywords": [
"comhad msi",
"Formáid comhaid MSI",
"cad is comhad msi ann",
"comhad",
"msi shampla",
"síneadh comhad msi",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid MSI agus APIanna ar féidir leo comhaid MSI a chruthú agus a oscailt.",
  "title": "MSI - Comhad Pacáiste Suiteálaí Windows",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-gai"
}
},
  "lastmod": "2021-06-30"
}

## Cad is comhad MSI ann?
Comhad MSI a úsáidtear chun cláir Windows a shuiteáil agus a sheoladh; pacáiste iomlán do Microsoft Windows ina bhfuil faisnéis suiteála do ghnáthchlár bogearraí, lena n-áirítear comhaid riachtanacha le suiteáil agus faisnéis faoin suíomh suiteála. Féadfaidh an pacáiste le haghaidh nuashonruithe bogearraí a bheith sna comhaid MSI freisin. Tá comhaid MSI cosúil le [EXE](/executable/exe/), ach b'fhéidir nach n-áiríonn EXE an t-eolas suiteálaí uaireanta agus d'fhéadfadh an clár bogearraí a bheith ag rith go díreach agus an comhad EXE á rith.

## Formáid comhaid MSI
Is éard atá i Windows Installer i ndáiríre ná API (Comhéadan Ríomhchláraithe Feidhmchláir) agus comhpháirt bogearraí de Microsoft Windows a úsáidtear chun clár bogearraí a shuiteáil, a bhaint agus a chothabháil. Déantar an fhaisnéis suiteála, agus na comhaid roghnacha, a phacáistiú mar phacáistí suiteála agus bunachair shonraí ghaolmhara atá struchtúrtha mar Stórálacha Struchtúrtha COM; ar a dtugtar go maith mar **comhaid MSI**, a bhfuil an síneadh comhad .msi. Sna pacáistí leis an síneadh comhad **.mst** tá **Scripteanna Claochlaithe** de Shuiteálaí Windows, tá **Merge Modules** agus an síneadh comhad **.pcp** i gcomhaid leis an síneadh **.msm** a úsáidtear le haghaidh **Airíonna Cruthaithe Paiste**. Éiríonn Windows Installer níos forbartha tar éis athruithe suntasacha a dhéanamh óna leaganacha níos luaithe, Setup API. Is gnéithe nua de Windows Installer iad creat GUI agus giniúint uathoibríoch den seicheamh díshuiteála. Breathnaíodh anois air mar mhalairt ar chreata suiteálaithe inrite aonair.

### Struchtúr loighciúil na bpacáistí MSI
Ainmnítear i bpacáiste suiteáil táirge iomlán amháin nó níos mó agus sainaithnítear go ginearálta é i **TREOIR**. Tá táirge comhdhéanta de chomhpháirt amháin nó iolrach agus grúpáilte i ngnéithe éagsúla. Ní láimhseálann an Suiteálaí Windows spleáchais idir táirgí éagsúla ag an am céanna. Tá na gnéithe seo a leanas i struchtúr loighciúil na bpacáistí:

- **Táirgí**: Is táirge é clár oibre amháin suiteáilte nó sraith de chláir iolracha a chuirtear le chéile. Sainaithnítear táirge le GUID uathúil.
- **Gnéithe**: D’fhéadfadh go mbeadh líon ar bith comhpháirteanna agus fo-ghnéithe eile ann. Is féidir gné amháin a bheith i bpacáistí níos lú.
- **Comhpháirteanna**: Láimhseálann Windows Installer an chomhpháirt mar aonad; is féidir comhaid chláir, fillteáin, eochracha clárlainne, comhpháirteanna COIM, agus aicearraí a bheith iontu.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## Tagairtí 

* [Suiteálaí Windows - le Vicipéid]( https://en.wikipedia.org/wiki/Windows_Installer)



