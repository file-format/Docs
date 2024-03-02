{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Chomhaid TEX",
  "description": "Foghlaim faoi fhormáid comhaid TEX agus APIanna ar féidir comhaid TEX a chruthú agus a oscailt.",
  "linktitle": "TEX",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-te-gax"
}
},
  "lastmod": "2019-09-10"
}

## Cad is Comhad TEX ann? ##

Is teanga é **TeX** a chuimsíonn ríomhchlárú chomh maith le gnéithe marcála suas, a úsáidtear chun doiciméid a chlóchur. Is é Donald Knuth ó Ollscoil Stanford, a chruthaigh an córas clóchuradóireachta seiftiúil seo. Ar fud an domhain, is é TeX an rogha deiridh d’údair agus d’fhoilsitheoirí chun doiciméid theicniúla ardchaighdeáin a tháirgeadh. Déanann TeX sár-jab maidir le formáidiú nathanna casta matamaitice. I gcomhar le fótaitíopaí ardcháilíochta, cuireann TeX in iomaíocht leis na torthaí a ghineann na córais clóchuradóireachta traidisiúnta is fearr. Dá bhrí sin meastar iad mar na córais dhigiteacha chlóghrafacha is fearr.

Tá comhaid ionchuir TeX bunaithe ar chód ASCII, rud a cheadaíonn roinnt lámhscríbhinní i measc scríbhneoirí, bainisteoirí foilsitheoireachta agus léirmheastóirí. Tacaíonn raon leathan timpeallachtaí ríomhaireachta, beagnach gach ardán nua-aimseartha agus go leor ardán níos sine le TeX. Ina theannta sin, is bogearraí saor in aisce é TeX, atá ar fáil do raon leathan tomhaltóirí. Úsáideann go leor suiteálacha UNIX araon UNIX troff agus TeX mar a gcóras formáidithe chun críocha éagsúla. Déantar tascanna clóchuradóireachta eile go sármhaith i bhfoirm LaTeX, ConTeXt, agus pacáistí macra eile.

## Stair Ghearr ##

TeX was designed and written by Donald Knuth in 1978. Rinne Guy Steele ó Institiúid Teicneolaíochta Massachusetts athbhreithniú ar ionchur/aschur TeX chun é a chur ar siúl faoin gcóras oibriúcháin Neamh-chomhoiriúnach cosúil leis an gCóras Roinnt Ama (ITS). Forbraíodh an chéad leagan de TeX faoi chóras oibriúcháin Stanford WAITS sa teanga ríomhchlárúcháin (SAIL) agus tástáladh é le rith ar PDP-10. Thug Knuth isteach an smaoineamh maidir le ríomhchlárú liteartha do réamhleaganacha. Is bealach é ríomhchlárú liteartha chun cód foinse agus clóchuradóireacht in-chomhthiomsaithe (in TeX) a ghiniúint le haghaidh doiciméadú tras-nasctha ag baint úsáide as an mbunchomhad. Tugtar WEB ar an teanga a úsáidtear chun na hardleaganacha seo de TeX a fhorbairt, meascán de chláir Pascal DEC PDP-10 chun inaistritheacht a chinntiú.

A revised new version of TeX published in 1982 and was called TeX82. Is é an t-athrú mór ná an t-algartam nua-scríofa le Frank Liang a chur in ionad an bhunalgartaim fleascaíochta. Chun iniomparthacht thar ardáin éagsúla a chinntiú, In ionad snámhphointe a úsáid, úsáideann TeX82 uimhríocht phointe seasta mar aon le fíortheanga ríomhchlárúcháin turing-iomlán. I 1989, eisíodh leagan nua de TeX agus Metafont. Mar sin éascaíonn an leagan 3.0 de TeX ionchuir 8-giotán, rud a ligeann do 256 carachtar difriúil sa téacs. Tar éis leagan 3, sainítear nuashonruithe trí dhigit bhreise a chur leis ag deireadh an deachúla eg cuirtear an leagan reatha de TeX in iúl mar 3.14159265. Nuashonraíodh an leagan seo an 12-1-2014 go deireanach.

## Ionchur TeX ##

Is féidir comhad Ionchuir chuig TEX a ullmhú le heagarthóir téacs ag baint úsáide as gnáth-théacs. Murab ionann agus gnáthphróiseálaí Focal, ní cheadaíonn an comhad ionchuir seo aon charachtair rialaithe dofheicthe. Is féidir comhad amháin a neadú i gcomhad eile, ina bhfuil sainmhínithe macra agus sainmhínithe cúnta a chuireann le cumas TeX. Má thagann suiteáil TeX le haon chomhaid macra, léiríonn an fhaisnéis áitiúil faoi TeX faoi úsáid a bhaint as macra-chomhaid. Comhtháthaíonn foirm chaighdeánach TeX meascán de mhacraí agus sainmhínithe eile ar a dtugtar plain TEX.

Bunaithe ar eolas beacht ar mhéideanna na gcarachtar agus na siombailí go léir, ríomhann sé an t-eagrú is fearr de litreacha in aghaidh na líne agus línte in aghaidh an leathanaigh. Ag an am próiseála doiciméad, táirgtear comhad .dvi, áit a seasann dvi” do neamhspleách ar an bhfeiste”. Tá gá le cláir tiománaí gléas chun an doiciméad a phriontáil nó a réamhamharc le síneadh dvi. Sa lá atá inniu ann, seachnaíonn pdf-TeX a úsáidtear go coitianta giniúint dvi. Níl aon eolas roimh ré ar chlónna ar fáil laistigh de shuiteáil TeX, mar sin úsáidtear comhaid chló seachtracha, atá mar chuid de thimpeallacht áitiúil TeX chun faisnéis a fháil le haghaidh doiciméad.

## Córas Clóchuradóireachta ##

Is féidir le thart ar 300 primitives (orduithe) a thuiscint ag an gcóras TeX bonn. Is orduithe leibhéal íseal iad primitives, mar sin is annamh a úsáideann úsáideoir coitianta iad go díreach agus is comhaid formáide a dhéantar an chuid is mó den fheidhmiúlacht. Is íomhánna cuimhne réamhlódáilte de TeX iad na comhaid formáide seo agus ina dhiaidh sin lódáiltear bailiúcháin mhóra macra. Cuireann bunfhormáid réamhshocraithe na teanga .i. plain TeX isteach thart ar 600 ordú.

Ciallaíonn cúlslais atá grúpáilte le braces chatach tosú orduithe TeX. Ós rud é gur teanga mhacra agus chomharthaí í TeX, is féidir beagnach gach saintréith chomhréire TeX a athrú ag am rite, lena n-áirítear cinn atá sainithe ag an úsáideoir ach amháin comharthaí nach féidir a leathnú a dhéantar ansin. Tá an leathnú féin beagnach saor ó thrioblóidí. Ní mór roinnt orduithe a theacht i ndiaidh argóintí a chuidíonn le feidhm ordaithe a mhíniú. Mar shampla, ordaíonn an t-ordú \vskip do TEX scipeáil síos / suas an leathanach agus argóint ina dhiaidh sin a shocraíonn cé mhéad spáis le scipeáil.

## Leaganacha ##

Is í LaTeX an fhormáid is minicí a úsáidtear a d’fhorbair Leslie Lamport ar dtús. Comhtháthaíonn LaTeX stíleanna éagsúla doiciméad do chomhaid, litreacha, leabhair agus sleamhnáin agus tairgeann sé tagairt agus uimhriú uathoibríoch do rannóga éagsúla agus do shloinnte matamaitice. Formáid mhóréilimh eile is ea AMS-TeX, arna fhorbairt ag Cumann Matamaitice Mheiriceá.

Cuireann AMS-TeX orduithe i bhfad níos so-úsáidte ar fáil, ar féidir le irisleabhair iad a athshainiú chun teacht lena stíl áitiúil. Is féidir le LaTeX buntáistí AMS-TeX a bhaint amach trí úsáid a bhaint as na pacáistí AMS ar a dtugtar AMS-LaTeX ansin. Formáid eile é ConTeXt a scríobh Hans Hagen a úsáidtear go príomha le haghaidh foilsitheoireacht deisce.

Tairgeann bogearraí TeX roinnt gnéithe nach raibh ar fáil, nó ar cháilíocht níos ísle, i gcórais chlóchuradóireachta eile nuair a cruthaíodh é. Tá cuid de ghnéithe nuálaíocha na teanga seo bunaithe ar algartaim shuimiúla a tháinig as tráchtais scoláirí Knuth. Cé go bhfuil gnéithe úsáideacha TeX á n-ionchorprú ina gcláir ag cláir chlóchuradóireachta eile.

## Tagairtí ##

* [Córas clóchuradóireachta TeX](https://en.wikipedia.org/wiki/TeX)


