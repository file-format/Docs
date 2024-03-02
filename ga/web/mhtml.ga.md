{
  "date": "2019-10-11",
  "keywords": [
"mhtml",
"comhad mhtml",
"Formáid comhaid mhtml",
"cineál comhaid mhtml",
"comhad",
"cineál",
"Cad is comhad mhtml ann"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHTML - Comhad HTML MIME",
  "description": "Foghlaim faoi fhormáid comhaid MHTML agus APIanna ar féidir leo comhaid MHTML a chruthú agus a oscailt.",
  "linktitle": "MHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mhtm-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad MHTML ann?

Is ionann comhaid a bhfuil síneadh MHTML acu agus formáid chartlainne leathanaigh ghréasáin ar féidir a chruthú trí roinnt feidhmchlár éagsúla. Tugtar formáid chartlainne ar an bhformáid toisc go sábhálann sé an cód Gréasáin **[HTML](/web/html/)** agus acmhainní gaolmhara i gcomhad amháin. Áirítear leis na hacmhainní seo aon rud atá nasctha leis an leathanach gréasáin mar íomhánna, feidhmchláiríní, beochan, comhaid fuaime agus mar sin de. Is féidir comhaid MHTML a oscailt i bhfeidhmchláir éagsúla ar nós Internet Explorer agus Microsoft Word. Úsáideann Microsoft Windows formáid comhaid MHTML chun cásanna fadhbanna a breathnaíodh le linn úsáid aon fheidhmchláir ar Windows a ardaíonn ceisteanna a thaifeadadh. Ionchódaíonn formáid an chomhaid MHTML inneachar an leathanaigh cosúil leis na sonraíochtaí a shainítear sa teachtaireacht/rfc822 atá ina sonraíochtaí gnáth-théacs a bhaineann le ríomhphost. Tá sonraíochtaí iarbhír na formáide mar atá sonraithe ag [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Formáid Chomhaid MHTML

Tugtar Ionchamháil MIME ar dhoiciméid HTML Comhiomlána ar MHTML freisin as a chumas leathanaigh ghréasáin HTML mar aon lena acmhainní a ionchódú chuig cartlann amháin gréasáin. De réir sonraíochtaí RFC 2557, is teachtaireacht ionchódaithe MIME é doiciméad comhiomlán ina bhfuil acmhainn fhréamh (réad) chomh maith le hacmhainní eile atá nasctha leis trí URIanna. D'fhéadfadh gur léiriú ar phictiúir inlíne, stílbhileoga, feidhmchláiríní, etc. iad na hacmhainní eile seo. Ina theannta sin, is féidir iad seo a bheith mar fhréamh do dhoiciméid ilmheán eile. Tá sonraíochtaí iomlána na gcáipéisí maidir le formáid comhaid MHTML mar atá sonraithe sa [RFC 2557](https://tools.ietf.org/html/rfc2557) agus ba chóir iad a chur ar aghaidh d’aon chineál forbartha feidhmchláir chun an fhormáid comhaid seo a léamh/a scríobh. Sonraíonn an caighdeán gur féidir na baill choirp atá le tagairt a aithint trí Aitheantas Ábhair nó trí Shuíomh Ábhar.

### Ceanntásca Ábhar MIME

Sainmhínítear ceanntásc inneachair MIME, Content-Location, chun tagairtí URI d'acmhainní i gcodanna eile den chorp a réiteach. Is féidir an ceanntásc seo a bheith in aon teachtaireacht nó ceannteideal ábhair.

### Ceanntásc Ábhar-Suíomh

Is éard is Suíomh Ábhar ann ná léiriú ar URI a chuireann lipéad ar a bhfuil i gcuid den choirp san áit a gcuirtear é. Féadfaidh a luach a bheith ina URI absalóideach nó ina URI coibhneasta. Is féidir é a úsáid chun lipéad a chur ar acmhainn nach féidir a fháil ar ais ag roinnt nó gach faighteoir teachtaireachta. Tá cead ag teachtaireacht amháin ceanntásc amháin Content-Suíomh a bheith aici. Sampla de struchtúr ilpháirteach/gaolmhar ina bhfuil baill choirp ar a bhfuil lipéid Suímh Ábhar agus Aitheantas Ábhar:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URIanna de Chomhiomláin MHTML

Tá URI comhiomlán MHTML difriúil ná URI a fhréamh URI. Ba cheart go mbeadh feidhm ag an réimse ceannteidil Ábhar-Suíomh maidir leis an gcomhiomlán iomlán má úsáidtear é i gceannteideal ilpháirteach/ceannteideal gaolmhar. Ar an gcaoi chéanna, is féidir leis an tsraith acmhainní a aisghabhtar a bheith difriúil leis an tacar acmhainní a aisghabhtar trí úsáid a bhaint as Suímh Ábhar a chuid páirteanna nuair a úsáidtear an URI a thagraíonn don chomhiomlán MHTML chun an comhiomlán seo a aisghabháil. Mar shampla, d’fhéadfaí seanleagan a thabhairt ar ais má fhaigheann tú comhiomlán MHTML, agus d’fhéadfaí leagan níos nuaí a thabhairt ar ais má fhaightear an fhréamh URI agus a réada nasctha inlíne.

## Tagairtí

* [IME Imchoimeád Doiciméad Comhiomlán - RFC 2557](https://tools.ietf.org/html/rfc2557)

* [Formáid Comhaid MHTML - Le Vicipéid](https://en.wikipedia.org/wiki/MHTML)


