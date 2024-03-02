{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EML - Teachtaireacht Ríomhphoist",
  "description": "Foghlaim faoi fhormáid comhaid EML agus APIs ar féidir leo comhaid EML a chruthú agus a oscailt.",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-em-gal"
}
},
  "lastmod": "2019-09-16"
}

## Cad is comhad EML ann?

Léiríonn formáid comhaid EML teachtaireachtaí ríomhphoist a shábháiltear ag baint úsáide as Outlook agus feidhmchláir ábhartha eile. Tacaíonn beagnach gach cliant ríomhphoist leis an bhformáid comhaid seo dá gcomhlíontar Caighdeán Formáid Teachtaireachta Idirlín RFC-822. Is é Microsoft Outlook na bogearraí réamhshocraithe chun cineálacha teachtaireachtaí EML a oscailt. Is féidir comhaid EML a úsáid chun iad a shábháil ar diosca chomh maith le seoladh amach chuig faighteoirí trí úsáid a bhaint as prótacail chumarsáide.

## Stair Achomair EML

Tá sonraíochtaí formáid comhaid EML ar fáil de réir [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Formáid Chaighdeánach. Roimh RFC-822, rialaigh RFC-733 na rialacha malartaithe teachtaireachtaí líonra go dtí i 1982, cruthaíodh an chéad cheann mar fheabhsú go cliathánach trí chaighdeáin ARPA a bhunú. Ag an am céanna, chruthaigh Microsoft a modúil COM féin chun a chliant ríomhphoist féin a fhorbairt ie Outlook Express. Ghlac RFC-822 an cosán le bheith bunaithe mar fhormáid dhílsithe nuair a d'imigh Microsoft ón gcaighdeán oscailte agus chruthaigh sé [PST](/email/pst/) formáid comhaid ina ndéantar ríomhphoist a shábháil i bhformáid bhunachair shonraí an-struchtúrtha. Mar thoradh air seo bhí fadhbanna ag úsáideoirí na gcliant ríomhphoist neamh-Microsoft nuair a cuireadh ríomhphoist ar aghaidh ó Microsoft Outlook.

Ba i 2001 nuair a feabhsaíodh an caighdeán 822 go 2822 - Formáid Teachtaireachtaí Idirlín atá in úsáid faoi láthair chun teachtaireachtaí EML a chruthú, a léamh agus a sheoladh i bhformáid MIME RFC-822.

## Sonraíochtaí Formáid Comhaid EML

Tá dhá chuid ar leith i gcomhaid EML:

* **Ceanntásca** - Tá faisnéis ann faoi cheanntásc na teachtaireachta

* **Comhlacht na dTeachtaireachtaí** - Tá sraith faisnéise ann ar féidir ábhar na teachtaireachta, íomhánna leabaithe agus ceangaltáin a áireamh


### Eolas Ceanntásca ###

Is éard atá i gcomhad EML ná faisnéis Ceanntásca agus comhlacht teachtaireachta go roghnach. Tá dhá chuid ag gach ceanntásc san EML agus idirstad :. Tugtar Ainm an Cheanntásc ar an gcéad cheann agus is corp ceanntásca é an ceann a leanann an idirstad. Mar shampla, áirítear le ceanntásca den sórt sin:

* Seoladh ríomhphoist an tseoltóra

* Seoladh ríomhphoist an fhaighteora

* Ábhar an R-phoist

* Stampa ama agus dáta na teachtaireachta


**Ceanntásc Sampla**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### Comhlacht Teachtaireachta ###

Is éard atá i gcorp na teachtaireachta EML an phríomhfhaisnéis ríomhphoist i bhfoirm téacs, hipearnasc agus ceangaltán. Is féidir téacs simplí inléite a bheith i gcorp ríomhphoist ach ní gá é. Sa chás seo, is féidir leis an gcomhlacht teachtaireachta a bheith folamh nó sonraí ceangaltáin ionchódaithe a bheith ann.

Déanann a Chineál Ábhar cur síos ar ábhar an chomhlachta teachtaireachta a chuireann ar chumas na bhfeidhmchlár léitheoireachta an fhaisnéis a léamh i bhformáidí faoi seach. Léiríonn sé nádúr agus formáid doiciméad. Tá struchtúr cineál MIME nó cineál ábhair an-simplí; tá sé comhdhéanta de chineál agus de fhochineál, dhá teaghrán, scartha le '/'. Ní cheadaítear spás. Seasann an `cineál` don chatagóir agus féadann sé a bheith ina chineál scoite nó ina chineál ilpháirteach. Baineann an `fochineál` go sonrach le gach cineál. Tá liosta na gcineálacha, a thagann sa chatagóir Cineál Ábhar, fada ach tá roinnt cineálacha ábhair tábhachtacha mar seo a leanas:


|**Cineál**|**Cur síos**|** Sampla de Fhochineálacha**
---|---|---|
|téacs|Léiríonn leis formáid atá inléite ag an duine|téacs/gnáth, téacs/html, téacs/css, téacs/javascript
|íomhá|Léiríonn íomhá d'aon chineál gan físeáin a áireamh | íomhá/bmp, íomhá/png, íomhá/jpg, íomhá/gif
|audio|Léiríonn aon fhormáid comhaid fuaime | fuaime/mdi, fuaime/wav
|iarratas|Léiríonn sé de chineál ar bith sonraí dénártha | iarratas/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Léiriú Ceangaltán i gCoirp EML

Tá teorainneacha i gcorp EML do gach cineál ábhair atá ann. Aithnítear ceangaltán i gcorp na teachtaireachta trína Chineál Ábhar agus a Dhiúscairt Ábhar mar a thaispeántar sa sampla seo a leanas:

Cineál Ábhar: téacs/plain; charset#fuinneoga-1252; ainm#apple appstore.txt
Ábhar-Diúscairt: ceangaltán; ainm comhaid#apple appstore.txt
Ábhar-Aistriú-Ionchódú: base64
X-Iatán-Aitheantas: f_jkhztmd02

Mar is léir, cuireann an tacar Ábhar-Diúscairt le ceangaltán ar chumas na n-iarratas a léamh chun faisnéis ceangaltáin a fháil, mar shampla ainm an chomhaid ceangaltáin agus an t-ionchódú aistrithe. Leanann inneachar na gceangaltán ionchódaithe atá le léamh i ndiaidh an fhaisnéis faoi cheannteidil na gceangaltán.

#### Sampla de Scarbhileog mar Iatán

Ábhar-Cineál: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; ainm#Béarla_spodr.xlsx
Ábhar-Diúscairt: ceangaltán; ainm comhaid#Béarla_spodr.xlsx
Ábhar-Aistriú-Ionchódú: base64
X-Iatán-Aitheantas: f_jkhztmd43

## Conas comhad EML a oscailt

Is féidir leat comhaid EML a oscailt ag baint úsáide as ríomhchláir ríomhphoist éagsúla mar:

 * **Apple Mail ar macOS**
 * **Mozilla Thunderbird**
 * **Microsoft Outlook**

Déantar comhaid EML a shábháil i bhformáid gnáth-théacs agus is féidir leat na comhaid EML seo a oscailt freisin le heagarthóirí téacs móréilimh ar nós **TextEdit** ar macOS agus **Microsoft Notepad** ar Windows OS.

## Conas comhad EML a thiontú

Is féidir leat comhaid EML a thiontú go formáidí éagsúla eile le feidhmchláir ar nós Apple Mail agus Microsoft Outlook.

Mar shampla, is féidir le Microsoft Outlook comhad EML a thiontú go dtí na formáidí seo a leanas:

**[.MSG](/eml/msg/)** - Formáid Teachtaireachta Microsoft Outlook
**{{ HYPERLINK1}}** - Formáid Doiciméad Protable

## Tagairtí

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)


