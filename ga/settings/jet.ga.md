{
  "date": "2023-09-05",
  "keywords": [
"scaird",
"comhad scaird",
"cad is scairdchomhad ann",
"Pacáiste Páirtí Jackbox",
"conas a oscailt comhad scaird",
"comhad",
"síneadh comhad scaird",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid JET - Socruithe an Phacáiste Cóisir don Bhosca Poill",
  "description": "Foghlaim faoi fhormáid JET agus APIs ar féidir leo comhaid JET a chruthú agus a oscailt.",
  "linktitle": "JET",
  "menu": {
    "docs": {
      "identifier": "settings-jet-ga",
      "parent": "settings"
}
},
  "lastmod": "2023-09-05"
}

## Cad is comhad JET ann?

Is comhad socruithe é comhad .jet atá uathúil don tsraith físchluichí **The Jackbox Party Pack**. Tá na comhaid seo ríthábhachtach chun gnéithe éagsúla de chluichí cóisire ar leith a chumrú laistigh den bhailiúchán. Go hiondúil, stórálann siad socruithe agus treoracha i bhformáid JSON nó XML. Tá sampla de seo le feiceáil sa Jackbox Party Pack 2, áit a mbaineann cluiche cosúil le Earwax úsáid as comhad JET darb ainm EarwaxAudio.jet” chun comhaid fuaime a bhaineann leis an gcluiche a bhainistiú agus a imirt.

Feidhmíonn na comhaid .jet seo go bunúsach mar ghormchlónna do pharaiméadair chluiche, ag cuidiú lena chinntiú go n-oibríonn gach cluiche páirtí laistigh den tsraith Pacáiste Páirtí Jackbox go réidh agus go dtugann sé an taithí gameplay atá beartaithe. Ligeann siad socruithe cluiche a shaincheapadh, amhail leideanna fuaime, rialacha cluiche, agus sonraí tábhachtacha eile, rud a chuireann leis an taithí il-imreora uathúil agus taitneamhach a bhfuil aithne ag na cluichí seo air.

## Pacáiste Páirtí Jackbox

Is sraith de bhailiúcháin cluichí físeáin é Pacáiste Páirtí Jackbox arna bhforbairt ag Jackbox Games, Inc. De ghnáth bíonn éagsúlacht cluichí páirtí sna bailiúcháin seo deartha le haghaidh gameplay il-imreora, rud a fhágann go bhfuil siad oiriúnach le haghaidh cruinnithe sóisialta, páirtithe, nó seisiúin chearrbhachais ócáideacha le cairde agus teaghlaigh. Tá cáil ar na cluichí as a n-inrochtaineacht agus a n-úsáid a bhaintear as fóin chliste, táibléad, nó ríomhairí mar rialaitheoirí, rud a ligeann d’imreoirí a bheith rannpháirteach ag baint úsáide as a gcuid gléasanna féin.

Áirítear le gach tráthchuid de The Jackbox Party Pack rogha éagsúil de chluichí cóisire, ó chluichí mionaithnidiúla go líníocht chruthaitheach agus ghreannmhar nó cluichí focal. I measc roinnt cluichí coitianta ó leaganacha éagsúla de The Jackbox Party Pack tá Quiplash, Fibbage, Drawful, Trivia Murder Party, agus go leor eile.

Spreagann na cluichí cruthaitheacht, greann agus idirghníomhú sóisialta, rud a fhágann gur roghanna coitianta iad maidir le heispéiris il-imreora pearsanta agus ar líne. Is minic a vótálann imreoirí ar na freagraí nó na líníochtaí is fearr leo, agus is gnách go n-áiríonn na cluichí gnéithe le haghaidh sruthú agus craolacháin, rud a fhágann go bhfuil siad buailte i measc cruthaitheoirí ábhar agus sruthóirí.

Tá na cluichí Pacáiste Páirtí Jackbox ar fáil ar ardáin éagsúla, lena n-áirítear PC, consóil cluichíochta, agus ardáin sruthú, rud a fhágann go bhfuil sé éasca d'imreoirí taitneamh a bhaint as na heispéiris siamsúla agus idirghníomhacha seo i suíomhanna éagsúla. Tugann gach eisiúint nua de The Jackbox Party Pack cluichí úra agus spreagúla, ag cinntiú go bhfuil rud éigin ann a mbainfidh gach duine taitneamh as.

## Formáid Chomhaid JET - Tuilleadh Eolais

Is bailiúchán de fhíschluichí é Pacáiste Cóisir Jackbox, gach ceann acu ina bhfuil éagsúlacht de chluichí páirtí spraoiúla atá deartha le haghaidh siamsaíochta il-imreora. Mar shampla, sa Jackbox Party Pack 2, gheobhaidh tú rogha de chúig chluiche páirtí, lena n-áirítear Fibbage 2, Earwax, Bidiots, Quiplash XL, agus Bomb Corp.

Chun tic a chur leis na cluichí seo, bíonn siad ag brath ar shonraí cluiche ar leith atá stóráilte i bhfo-eolaire tiomnaithe. Glacaimis Earwax mar shampla. Stórálann Earwax a shonraí cluiche i struchtúr eolaire mar seo:

```
~/Jackbox Games/The Jackbox Party Pack 2/games/Earwax
```

Laistigh de na fo-eolaire seo, aimseoidh tú comhad socruithe JET amháin nó níos mó. Tá ról ríthábhachtach ag na comhaid seo maidir le gnéithe éagsúla den chluiche a shainiú, mar shampla cén téacs atá le feiceáil, cé na comhaid meán a úsáidtear, agus cathain a léirítear na heilimintí seo ar fud an chluiche. Go háirithe, is comhaid gnáth-théacs iad gach comhad JET, rud a chiallaíonn go mbíonn deis ag modders agus díograiseoirí iad a chur in eagar. Ligeann an cumas eagarthóireachta seo an t-ábhar in-chluiche a shaincheapadh, ó théacs agus íomhánna go fuaimeanna, ag cur ar chumas na n-imreoirí a n-eispéireas cearrbhachais a phearsanú nó cineálacha uathúla a chruthú ar na cluichí.

## Conas comhad JET a oscailt?

Ós rud é go bhfuil comhaid JET i bhformáid gnáth-théacs, is féidir iad a rochtain agus a mhodhnú trí úsáid a bhaint as aon bhogearraí eagarthóireachta téacs. m.sh

- Microsoft Notepad (Windows)
- Apple TextEdit (MAC)
- Notepad++

## Comhaid JET eile

- [JET - Microsoft JET Database File](/database/jet/)

## Tagairtí
* [Paca Cóisir an Bhosca Jack]( https://en.wikipedia.org/wiki/The_Jackbox_Party_Pack)


