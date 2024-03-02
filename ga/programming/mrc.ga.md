{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"comhad",
"síneadh",
"formáid comhaid",
"cur i bhfeidhm mrc",
"Treoir Ríomhchlárúcháin",
"mrc shampla",
"mIRC",
"Teanga scriptithe mIRC",
"comhaid INI",
"teanga scriptithe mSL",
"teanga mIRC",
"Scripteanna mIRC",
"teanga scriptithe"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC - Comhad Teanga Script mIRC",
  "description": "Foghlaim faoi fhormáid comhaid MRC agus APIanna ar féidir comhaid MRC a chruthú agus a oscailt.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-gac"
}
},
  "lastmod": "2021-09-14"
}

## Cad is comhad MRC ann?

Is teanga scriptithe í mIRC atá leabaithe mar chliant IRC (Internet Relay Chat) i gcóras oibriúcháin Windows. Soláthraíonn sé saoráid cosanta ó thurscar le haghaidh úsáide pearsanta agus cainéal. Chun eispéireas níos fearr ar chomhoiriúnacht úsáideora a sholáthar, ceadaíonn an teanga scriptithe mIRC seo fuinneoga comhphlé a chruthú. Stóráiltear na comhaid ina bhfuil scripteanna, i bhformáid gnáth-théacs den chuid is mó leis an síneadh MRC nó mar chomhaid [INI](/system/ini/). Tugtar orduithe agus aitheantóirí ar fheidhmeanna na teanga seo (nuair a thugann siad luach ar ais).

Soláthraíonn teanga mIRC lódáil comhaid scripte iolracha ag aon am amháin. Ar an láimh eile, is féidir le comhad amháin a chur faoi deara nach n-úsáidtear an ceann eile a thuilleadh nuair a luchtaítear é go comhuaineach. Sábháiltear orduithe agus is féidir leo a bheith ann go huathoibríoch in IRC. Ní chuimsíonn na horduithe agus na hailiasanna a úsáidtear sa teanga seo tosaíocht d'aon cheann de na carachtair.

Úsáidtear mIRC go forleathan chun na róbónna a dhéanamh chun cainéal a bhainistiú go huathoibríoch ach is féidir leis an teanga scriptithe mSL é a athrú freisin. Is féidir leis go leor gnéithe nua a thabhairt isteach cosúil le macraí, cumas seinm ceoil, macraí agus feidhmeanna beaga, cluichí bunúsacha, nó feidhmchláir bheaga a oibriú.


## Stair Ghearr ##

D'fhorbair Khaled Adam Bey an teanga scriptithe seo den chéad uair i 1995. Chruthaigh Khalid dearadh na teanga scripte freisin. Ba é sprioc na teanga seo ná cláir a bhí bunaithe ar imeachtaí. Ar dtús, ba é .mrc agus .ini an síneadh comhad a úsáideadh do chomhaid na teanga ríomhchlárúcháin seo. Thairis sin, forbraíodh é faoi cheadúnas bogearraí dílseánaigh.

## Sonraíocht Theicniúil ##

Déantar roinnt feidhmeanna a shaincheapadh tríd an teanga mIRC seo agus tugtar ailiasanna orthu. Nuair a thugann na hailiasanna seo luachanna ar ais tugtar aitheantóirí saincheaptha orthu. Déantar na hathróga go léir atá sa teanga miRC seo a chlóscríobh go dinimiciúil. Úsáideann na scripteanna mIRC sigils. Gné eile den teanga scriptithe seo ná pop-ups. Is féidir leis na húsáideoirí pop-ups a ghlaoch ach iad a roghnú. Sonraítear cianda chuig imeachtaí áirithe. Tugtar na remotes nuair a tharlaíonn an teagmhas coibhneasta.

Úsáidtear comharthaí teorannaithe spáis chun gach líne de chód na teanga seo a bhriseadh. Tá roinnt síntí coitianta eile a úsáidtear le haghaidh comhaid mIRC cosúil le MDX (Míneadh Dialóige mIRC) agus DCX (Síneadh Rialaithe Dialóg). Is síntí idirphlé iad an dá cheann seo agus tá níos mó tóir orthu i gcomparáid lena chéile. Tagraíonn ainmníocht na teanga scriptithe seo do na tógálacha teanga. Baineann an teanga mIRC le gnéithe éagsúla de theanga scriptithe mar athróga áitiúla agus domhanda, athróga dénártha, táblaí hash, agus láimhseáil comhad.


## Sampla Formáid Chomhaid MRC ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Tagairt ##

* [MIRC - le Vicipéid]( https://en.wikipedia.org/wiki/MIRC_scripting_language )




