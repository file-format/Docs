{
  "date": "2023-07-12",
  "keywords": [
"exp",
"comhad exp",
"Cad é an comhad mpeg exp",
"Conas a oscailt comhad exp",
"comhad",
"síneadh comhad exp",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhad EXP - Comhad Easpórtála Siombailí",
  "description": "Foghlaim faoi fhormáid EXP agus APIs ar féidir leo comhaid EXP a chruthú agus a oscailt.",
  "linktitle": "EXP",
  "menu": {
    "docs": {
      "identifier": "programming-exp-ga",
      "parent": "programming"
}
},
  "lastmod": "2023-07-12"
}

## Cad is comhad EXP ann?

Gintear comhad EXP, a sheasann do chomhad easpórtála siombailí, trí thimpeallacht chomhtháite forbartha (IDE) nó tiomsaitheoir. Cuimsíonn an comhad seo sonraí dénártha maidir le sonraí agus feidhmeanna easpórtáilte. Is é an cuspóir atá leis nasc a bhunú idir an clár as ar tháinig sé agus clár eile trí chabhrú leis an dá cheann a nascadh le chéile. Tá ról ríthábhachtach ag comhaid EXP maidir le comhtháthú gan uaim agus comhoibriú idir feidhmchláir bogearraí éagsúla a éascú.

## Formáid Chomhaid EXP - Tuilleadh Eolais

Nuair is gá do chlár idirghníomhú le clár eile trí shonraí a allmhairiú agus a onnmhairiú, is gá nasc a bhunú ag baint úsáide as leabharlann iompórtála agus comhad easpórtála. Tá an nasc seo ríthábhachtach chun spleáchais chiorclacha ar allmhairí a d’fhéadfadh teacht chun cinn idir na cláir a réiteach.

Tarlaíonn iompórtálacha ciorclach nuair a bhraitheann Clár A ar shonraí nó ar fheidhmeanna áirithe ó Chlár B, agus braitheann Clár B freisin ar shonraí nó ar fheidhmeanna ó Chlár A. Féadfaidh an spleáchas frithpháirteach seo dúshlán a chruthú le linn na céime nasctha den phróiseas forbartha bogearraí.

Chun aghaidh a thabhairt ar allmhairí ciorclach, is éard atá i gceist le cur chuige tipiciúil ná comhad .LIB (leabharlann iompórtála) agus comhad EXP (comhad easpórtála) a úsáid agus na cláir á nascadh. Feidhmíonn an comhad LIB mar leabharlann allmhairithe, ag soláthar na faisnéise is gá chun go bhféadfaidh Clár A rochtain a fháil ar na sonraí nó na feidhmeanna riachtanacha ó Chlár B. Ar an láimh eile, feidhmíonn an comhad EXP mar chomhad onnmhairithe, ina bhfuil an fhaisnéis siombaile ábhartha a onnmhairíonn Clár B. lena gcaitheamh ag Clár A.

Trí úsáid a bhaint as an gcomhad LIB agus an comhad EXP le linn an phróisis nasctha, is féidir na spleáchais allmhairithe ciorclach a réiteach. Is féidir le Clár A na heilimintí riachtanacha a allmhairiú go rathúil ó Chlár B tríd an leabharlann iompórtála, agus is féidir le Clár B na siombailí riachtanacha a bheidh le rochtain ag Clár A a onnmhairiú tríd an gcomhad easpórtála.

## Aidhm agus Úsáid na gcomhad EXP i bhForbairt Bogearraí

Baineann comhaid EXP go príomha le forbairt bogearraí agus úsáidtear iad i gcomhar le teangacha ríomhchlárúcháin agus uirlisí forbartha éagsúla. I measc cuid de na bogearraí agus na huirlisí coitianta a bhaineann le comhaid EXP tá:

- **Tiomsaitheoirí:** Féadfaidh bogearraí tiomsaithe, mar GCC (GNU Compiler Collection) nó Microsoft Visual C++, comhaid EXP a ghiniúint mar chuid den phróiseas tiomsaithe. Tá faisnéis shiombail sna comhaid EXP a chuidíonn le nascadh agus dífhabhtú.
- ** Nascóirí:** Úsáideann nascóirí, ar nós GNU ld (Linker) nó Microsoft Linker, comhaid EXP chun tagairtí siombailí a réiteach agus chun naisc a bhunú idir modúil chóid éagsúla le linn an phróisis nasctha.
- **Timpeallacht Chomhtháite Forbartha (IDEanna):** Is minic a bhíonn tacaíocht ionsuite ag IDEanna mar Visual Studio, Eclipse, nó Xcode chun oibriú le comhaid EXP. Soláthraíonn siad gnéithe chun faisnéis siombailí a bhainistiú, dífhabhtaithe, agus nascadh, ag baint úsáide as na comhaid EXP taobh thiar de na radhairc.
- **Dífhabhtóirí:** Úsáideann uirlisí dífhabhtaithe cosúil le GDB (GNU Debugger) nó WinDbg comhaid EXP chun seoltaí cuimhne a nascadh le siombailí an chóid foinse, rud a chuireann ar chumas forbróirí a gcláir a dhífhabhtú go héifeachtach.
- **Próifíleoirí:** Féadfaidh uirlisí próifílithe, mar Intel VTune nó Visual Studio Profiler, comhaid EXP a úsáid chun sonraí feidhmíochta a mhapáil chuig feidhmeanna sonracha nó réigiúin chóid le linn an phróisis phróifílithe.

## Conas comhad EXP a oscailt?

De ghnáth ní bhíonn i gceist comhaid EXP, ar comhaid easpórtála siombailí iad, a oscailt go díreach nó a fheiceáil ag úsáideoirí deiridh. Is iad na forbróirí a úsáideann go príomha iad agus déanann siad uirlisí a thógáil le linn na bpróiseas tiomsaithe, nasctha agus dífhabhtaithe.

Is gnách go ndéantar comhaid EXP a phróiseáil go huathoibríoch ag uirlisí forbartha nó a chomhtháthú sa chóras tógála. Feidhmíonn siad mar thagairt don tiomsaitheoir, don nascóir, don dífhabhtóir nó don phróifíleoir chun tagairtí siombailí a réiteach, seoltaí cuimhne a chomhlachú le heilimintí cód foinse, agus éascaíonn siad nascadh modúil cód.

Más forbróir thú a oibríonn le comhad EXP, de ghnáth ní gá duit an comhad a oscailt de láimh nó idirghníomhú leis. Ina áit sin, bheifeá ag brath ar uirlisí forbartha nó timpeallachtaí ríomhchlárúcháin a úsáideann an comhad EXP go hinmheánach chun a gcríocha faoi seach, mar nascadh, dífhabhtú nó próifíliú.

## Tagairtí
* [Comhaid Exp mar Ionchur Linker]( https://learn.microsoft.com/en-us/cpp/build/reference/dot-exp-files-as-linker-input?view=msvc-170)


