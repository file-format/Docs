{
  "date": "2019-12-10",
  "keywords": [
"CSV",
"comhad",
"síneadh",
"formáid comhaid",
"Luachanna Scartha Camóga",
"Scarbhileog"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid CSV agus APIanna ar féidir leo comhaid CSV a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid CSV",
  "linktitle": "CSV",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-cs-gav"
}
},
  "lastmod": "2019-12-10"
}

## Cad is comhad CSV ann?

Is ionann comhaid le síneadh .csv (Luachanna Deighilte Camóg) agus comhaid gnáth-théacs ina bhfuil taifid sonraí le luachanna scartha le camóg. Is taifead nua é gach líne i gcomhad CSV ón tsraith taifead atá sa chomhad. Gintear comhaid den sórt sin nuair a bhíonn aistriú sonraí beartaithe ó chóras stórála amháin go ceann eile. Ós rud é gur féidir le gach feidhmchlár taifid atá scartha le camóg a aithint, déantar comhaid sonraí dá leithéid a allmhairiú chuig an mbunachar sonraí go han-áisiúil. Is féidir le beagnach gach feidhmchlár scarbhileog ar nós Microsoft Excel nó OpenOffice Calc CSV a allmhairiú gan mórán iarrachta. Socraítear sonraí a allmhairítear ó chomhaid den sórt sin i gcealla scarbhileog le léiriú don úsáideoir.

## Stair Ghearr ##

Seo a leanas roinnt fíricí gasta faoi bhunús agus stair fhormáid comhaid CSV.

* 1972 - Thacaigh tiomsaitheoir IBM Fortran (leibhéal H leathnaithe) leo faoi OS/360


* 1978 - Thacaigh FORTRAN 77 le hionchur/aschur liosta-treoraithe a d’úsáid camóga agus spásanna le haghaidh teorannóirí


* 2005 - Rinneadh CSV a chaighdeánú le [RFC4180](https://tools.ietf.org/html/rfc4180 ) mar Chineál Ábhar MIME.


* 2013 - Láimhseáil moladh W3C easnaimh RFC4180


* 2015 - Rinne W3C na chéad dréachtaí de mholtaí le haghaidh caighdeáin CSV-meiteashonraí, ar cuireadh tús leo mar mholadh i mí na Nollag 2015


## Tiontaigh Comhaid CSV ##

Is féidir comhaid CSV a thiontú go formáidí éagsúla comhaid ag baint úsáide as na feidhmchláir ar féidir leo na comhaid seo a oscailt. Mar shampla, is féidir le Microsoft Excel sonraí a iompórtáil ó fhormáid comhaid CSV agus iad a shábháil i bhformáidí comhaid XLS, [XLSX](/spreadsheet/xlsx/), [PDF](/pdf/), [TXT](/word-processing/txt/), XML agus [HTML](/web/html/). Mar an gcéanna, cuireann seirbhísí deisce eile chomh maith le seirbhísí ar líne an cumas ar fáil comhaid CSV a onnmhairiú go HTML, ODS agus [RTF](/word-processing/rtf/).

## Formáid Chomhaid CSV ##

Is eol go bhfuil formáid comhaid CSV sonraithe faoi [RFC4180](https://tools.ietf.org/html/rfc4180). Sainmhíníonn sé aon chomhad a bheith comhlíontach CSV:

* Tá gach taifead suite ar líne ar leith, teorannaithe ag briseadh líne (CRLF). Mar shampla:

  * aaa, bbb, ccc CRLF
  * zzz, bbbb, xxx CRLF
* D’fhéadfadh nó nach mbeadh briseadh líne deiridh ag an taifead deireanach sa chomhad. Mar shampla:

  * aaa, bbb, ccc CRLF
  * zzz, bbbb, xxx
* D’fhéadfadh go mbeadh líne ceanntásca roghnach le feiceáil mar chéad líne an chomhaid leis an bhformáid chéanna leis na gnáthlínte taifid. Beidh ainmneacha sa cheanntásc seo a fhreagraíonn do na réimsí sa chomhad agus ba cheart go mbeadh an líon céanna réimsí ann agus atá sna taifid sa chuid eile den chomhad (ba cheart láithreacht nó easnamh líne an chinn a léiriú tríd an bparaiméadar "ceanntásc" roghnach de seo cineál MIME). Mar shampla:

  * réimse_ainm, réimse_ainm, réimse_ainm CRLF
  * aaa, bbb, ccc CRLF
  * zzz, bbbb, xxx CRLF
* Laistigh den cheanntásc agus de gach taifead, d’fhéadfadh réimse amháin nó níos mó a bheith ann, scartha le camóga. Ba cheart go mbeadh an líon céanna réimsí ar fud an chomhaid i ngach líne. Breathnaítear ar spásanna mar chuid de pháirc agus níor cheart neamhaird a dhéanamh orthu. Ní ceadmhach camóg a bheith i ndiaidh an réimse dheireanach sa taifead. Mar shampla:

  * aaa, bbb, ccc
* D’fhéadfadh nó nach mbeadh gach réimse faoi iamh i Sleachta dúbailte (ach ní úsáideann roinnt clár, mar Microsoft Excel, comharthaí athfhriotail dhúbailte ar chor ar bith). Mura bhfuil réimsí faoi iamh le comharthaí athfhriotail dhúbailte, ní fhéadfaidh comharthaí athfhriotail dhúbailte a bheith le feiceáil laistigh de na réimsí. Mar shampla:\

  * aaa, bbb, ccc CRLF
  * zzz, bbbb, xxx
* Ba cheart réimsí ina bhfuil bristeacha líne (CRLF), Sleachta dúbailte, agus camóga a chur faoi iamh i Sleachta dúbailte. Mar shampla:

  * aaa, b CRLF
  * bb, ccc CRLF
  * zzz, bbbb, xxx
* Má úsáidtear athfhriotail dhúbailte chun réimsí a chur faoi iamh, ní mór athfhriotail dhúbailte atá le feiceáil taobh istigh de réimse a éalú trí luachan dúbailte eile a chur roimhe. Mar shampla:

  * aaa, b bb, ccc

Mar sin féin, i bhfianaise na húsáide nua-aimseartha, níl an teorannóir teoranta do chamóg amháin agus is féidir é a bheith ina leathstad, ina chluaisín nó ina spásanna freisin. Soláthraíonn feidhmchláir ar nós Microsoft Excel rogha chun an carachtar teorannóra a shonrú chun taifid a allmhairiú ó chomhad CSV.

## Tagairtí

* [RFC 4180](https://tools.ietf.org/html/rfc4180)

* [RFC 2048](https://tools.ietf.org/html/rfc2048)

* [CSV - Vicipéid](https://en.wikipedia.org/wiki/Comma-separated_values )


