{
  "date": "2021-07-15",
  "keywords": [
"TMP",
"síneadh",
"comhad",
"formáid",
"córas",
"Comhad TMP",
"Doiciméid TMP",
"Comhaid TMP",
"Temporary file",
"iarratas",
"cláir"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "TMP - Formáid Chomhaid Shealadach",
  "description": "Foghlaim faoi fhormáid comhaid TMP agus APIanna ar féidir leo comhaid TMP a chruthú agus a oscailt.",
  "linktitle": "TMP",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-tm-gap"
}
},
  "lastmod": "2021-07-15"
}

## Cad is comhad TMP ann? ##

Tagraíonn comhad TMP do chúltaca sealadach, do stóráil nó do chóras comhaid eile a ghineann clár bogearraí. Cruthaítear é ó am go chéile mar chomhad dofheicthe agus scriostar go minic é nuair a scoirtear den chlár. Is féidir comhaid TMP a úsáid freisin chun faisnéis a stóráil go sealadach agus comhad nua á thógáil.

## Formáid Chomhaid TMP ##

Is gnách go mbíonn comhad TMP comhdhéanta d’amhshonraí a úsáidtear mar chéim sa phróiseas aistrithe ábhair ó stíl amháin go stíl eile. Is dhá aip iad Microsoft Word agus Apple Safari ar féidir leo formáid comhaid TMP a tháirgeadh agus a úsáid.

Go teoiriciúil, ba cheart na doiciméid TMP a ghintear a bhaint go huathoibríoch nuair a dhúntar an clár nó nuair a bhíonn an meaisín múchta. Go praiticiúil, ní mar sin a bhíonn i gcónaí. Mar thoradh air sin, agus tú ag seoladh trí dhoiciméid do chláir, féadfaidh tú teacht ar chomhaid neamhbhuan nach n-úsáideann an córas nó aon bhogearraí eile go gníomhach.

### Cuimhne cúnta ###

Úsáidtear cuimhne fhíorúil i gcórais oibriúcháin, áfach, d’fhéadfadh go mbeadh gá le cláir a úsáideann méideanna ollmhóra faisnéise chun doiciméid shealadacha a dhéanamh.

### Cumarsáid idirphróisis ###

Soláthraíonn an chuid is mó de na córais oibriúcháin primitives chun sonraí a rith idir cláir, mar phíopaí, soicéid, nó príomhchuimhne, ach is é an modh is simplí ná comhaid a aistriú go comhad sealadach agus comhairle a thabhairt don iarratas glactha ar shuíomh an chomhaid shealadaigh.


## Sonraíocht Theicniúil ##

Is iondúil go soláthraíonn córais oibriúcháin agus cláir bogearraí ainmneacha sainiúla doiciméad sealadacha a fháil.
Is féidir comhaid shealadacha a ghiniúint go sábháilte ar chórais POSIX ag baint úsáide as na feidhmeanna leabharlainne mkstemp nó tmpfile. Áirítear ar roinnt córas an feidhmchlár mktemp POSIX (ó imithe) roimhe seo. Faightear na comhaid seo de ghnáth san eolaire sealadach rialta ar ardáin Unix in /TMP, nó % TEMP% (tá sé sainiúil le haghaidh logáil isteach) ar mheaisíní Windows.

Nuair a stopann an clár nó nuair a dhúntar an doiciméad, baintear an comhad neamhbhuan a ghintear leis an gcomhad tmp go huathoibríoch. Is féidir GetTempFileName (Windows) nó tmpnam (POSIX) a úsáid chun ainm comhaid sealadach a chruthú a mhairfidh níos faide ná an clár a chruthaigh é.

## Tagairt ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
