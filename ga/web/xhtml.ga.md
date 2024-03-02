{
  "date": "2019-10-11",
  "keywords": [
"xhtml",
"Comhad",
"Síneadh",
"Formáid Chomhaid",
"Síneadh Comhad",
"html síneadh"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XHTML - Formáid Chomhaid Teanga Marcáil Hipirtéacs Inmhínithe",
  "description": "Foghlaim faoi cad is formáid comhaid XHTML ann agus APIanna ar féidir comhaid XHTML a chruthú agus a oscailt.",
  "linktitle": "XHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xhtm-gal"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad XHTML ann?

The XHTML is a text based file format with markup in the XML, using a reformulation of HTML 4.0. Tá na comhaid seo feiliúnach go maith le bheith oscailte nó le feiceáil i mbrabhsálaí gréasáin. Dearadh XHTML le bheith níos struchtúrtha, níos lú scripte, cineálach; ag baint úsáide as na háiseanna go léir atá ann cheana féin de XML agus níos neamhspleách gléas. Soláthraíonn XHTML sraith iomlán d’eilimintí agus de thréithe atá fiúntach, le roghanna sínte i gcomhcheangal le stílbhileoga. Úsáidtear na tréithe ón mbailiúchán tréithe meiteashonraí. Soláthraíonn XHTML solúbthacht agus inrochtaineacht trí gach eilimint léirithe **[HTML](/web/html/)** a fho-ordú ina stílbhileoga. Tá stílbhileoga níos ilúsáide ná na heilimintí léirithe seo. Tá sonraíochtaí le haghaidh HTML 4.01, HTML5 agus XHTML á bhforbairt go dinimiciúil ag Cuibhreannas an Ghréasáin Dhomhanda (W3C).

## Stair Achomair ar Fhormáid Chomhaid XHTML

The history of XHTML starts with a draft document released in December 1998 by the World Wide Web Consortium. This document refers the "Reformulating HTML in XML", a specification called XHTML 1.0.This new specification reformulated HTML in XML using the existing elements or attributes. In May 1999, W3 Consortium declared that HTML 4.0 had been re-formed as an XML application. i.e. XHTML. In January 26, 2000, the first specification that defines XHTML 1.0 was released by W3C. Further in May 31, 2001, the W3C announced XHTML as an independent language and started working on development of HTML 5.0. In 2005, áfach, bunaíodh grúpa oibre (WHATWG) a raibh sé mar aidhm aige gnáth-HTML a fheabhsú neamhspleách ar XHTML. Sa deireadh thosaigh an WHATWG ag obair ar HTML5 comhthreomhar le XHTML 2.

## Formáid Chomhaid XHTML

XHTML is a format, which is a collection of different document types and modules that mimic, categorize, and extend HTML 4. Tá na comhaid in XHTML bunaithe ar XML, agus bhí sé mar aidhm acu oibriú leis na gníomhairí úsáideora bunaithe ar XML. Tá comhaid XHTML i gcomhréir le XML. Úsáidtear uirlisí caighdeánacha XML chun comhaid XHTML a fheiceáil, a chur in eagar agus a bhailíochtú. Is féidir le Samhail Oibiachta Doiciméad HTML nó Samhail Oibiachta Doiciméad XML [DOM] feidhmiú trí dhoiciméid XHTML. Trí XHTML a roghnú inniu, is féidir le forbróirí inneachair taitneamh a bhaint as na buntáistí uile a bhaineann le XML gan a bheith buartha faoi chomhoiriúnacht a n-ábhar ar aghaidh nó ar gcúl.

Tógann sraith d’eilimintí gaolmhara modúl in XHTML. Féadfaidh foirmeacha nó eilimintí tábla éagsúla a bheith i modúl foirmeacha nó tábla ar féidir iad a thaispeáint ar leathanach gréasáin. Bhí sé mar aidhm ag an modúlú eilimintí HTML a leithlisiú ina thacair d'eilimintí nasctha iomadúla. Ionas gur féidir le forbróirí ábhair leas a bhaint as roghnú modúl le haghaidh cineálacha éagsúla gléasanna. Ina theannta sin, ligeann modúil do ghníomhairí úsáideoirí gnéithe a roghnú gan comhsheasmhacht le caighdeán XHTML a chailleadh. Tá riachtanais pharsála XHTML mar an gcéanna le XML agus cleachtann HTML a chuid féin.

### Comhlíonadh an Doiciméid

XHTML2 offer specifications conforming XHTML 1.0 documents, which uses the namespaces elements and attributes from the XML and XHTML 1.0. Tá dhá chineál i gComhlíonadh Doiciméid.

Tá Doiciméad Comhlíonta go docht bunaithe ar XML nach dteastaíonn ach na seirbhísí éigeantacha atá sainithe sa tsonraíocht seo. Ní mór na critéir seo a leanas a chomhlíonadh maidir le comhaid XHTML:

* Ní mór do chomhad cloí leis na srianta atá sainmhínithe sna DTDanna agus in Aguisín B.

* Ní mór go mbeadh html mar bhuneilimint an chomhaid.

* Ní mór dearbhú don ainmspás XHTML a bheith sa bhuneilimint den chomhad agus ba cheart é a shainmhíniú mar:


```
http://www.w3.org/1999/xhtml.
```

* D’fhéadfaí an bhuneilimint a scríobh mar:


```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Níos luaithe ná an bhuneilimint, ní mór DOCTYPE a dhearbhú, a gcaithfidh a n-aitheantóir poiblí tagairt a dhéanamh do cheann de na trí shainiú cineál doiciméid (DTDanna). Féadfar aitheantóir an chórais a mhodhnú chun na coinbhinsiúin chórais reatha a chomhlíonadh.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

I ndoiciméid XML, ní gá dearbhuithe XML a shonrú i ngach doiciméad; mar sin féin mealltar forbróirí ábhair chun dearbhuithe XML a úsáid ina gcuid doiciméad XHTML go léir. Tá na dearbhú seo éigeantach nuair a bhíonn ionchódú carachtar an doiciméid difriúil ó UTF-8/16 nó nuair nach bhfuil aon ionchódú sonraithe ag prótacal rialaithe. Tar éis sampla de dhoiciméad XHTML sainmhínítear na dearbhuithe XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Ní mór do ghníomhaire úsáideora comhréireach na rialacha seo a leanas a chomhlíonadh:

* Déanann gníomhaire úsáideora parsáil agus meastóireacht ar dhoiciméad XHTML a chinntíonn a chomhsheasmhacht le Moladh XML 1.0.

* I gcás gníomhaire úsáideora a bhailíochtú, ní mór dó bailíocht na ndoiciméad dá DTDanna tagartha a sheiceáil de réir XML. Nuair a phróiseálann gníomhaire úsáideora comhad XHTML mar XML cineálach, admhófar gnéithe ID cineáil mar aitheantóirí blúirí.


Má bhuaileann gníomhaire úsáideora isteach ar eilimint neamhaitheanta, seo a leanas na critéir éigeantacha nach mór dó a bhaint amach

* inneachar na heiliminte anaithnide sin a phróiseáil

* neamhaird a dhéanamh den tréith agus dá luach

* Úsáid luach an aitreabúide a chuirtear ar fáil mar réamhshocrú.


Nuair a thagann gníomhaire úsáideora trasna ar dhearbhú tagartha aonáin nár próiseáladh níos luaithe, ba cheart é a phróiseáil mar charachtair (ag tosú leis an gcomhartha &” agus ag críochnú leis an leathstad). Le linn próiseála inneachair, féadfaidh tagairtí carachtair nó aonáin charachtair atá intuartha ag an ngníomhaire úsáideora ach nach féidir a thabhairt ar aird aon rindreáil eile a úsáid a thugann an bhrí chéanna. I gcás den sórt sin, ní mór an doiciméad a thaispeáint ar bhealach a fhágann go soiléir don úsáideoir nach raibh an próiseas rindreála gnáth. Chun spás bán a phróiseáil, ní mór don ghníomhaire úsáideora breathnú ar shainmhíniú ó charachtair CSS [CSS2].

## XHTML Comhoiriúnacht ar gcúl

The back ward compatibility of XHTML 1.  Tá eolas maith ag na doiciméid ar ghníomhairí úsáideora HTML 4, má leantar na rialacha cearta. Tá XHTML 1.1 comhoiriúnach go hiomlán seachas nótaí ruby, cé go dtugann na brabhsálaithe HTML 4 neamhaird orthu go ginearálta. Tá XHTML 2.0 i bhfad níos lú comhoiriúnach, mar sin féin tugadh aghaidh ar an bhfadhb go pointe áirithe trí úsáid na scripte.

## Tagairtí

* [Stair XHTML: Ó na 1990idí go dtí an lá inniu](https://www.brighthub.com/internet/web-development/articles/109224.aspx)


