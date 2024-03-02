---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Foirm Comhad Leathanaigh Freastalaí Scalaat
linktitle: SSP
description: Lthuilleamh faoi cad is formáid comhaid SSP agus APIs is féidir a chruthú agus a oscailt comhad SSPs.
menu:
  docs:
    identifier: "web-ss-gap"
    parent: "web"
lastmod: 2021-09-30
---

## Cad is comhad SSP ann?

Is leathanach gréasáin é comhad le síneadh .ssp cruthaithe le cód Scala le haghaidh nathanna cainte seachas gnáth-HTML amháin. Feidhmíonn sé mar script taobh freastalaí ag baint úsáide as an teaglaim de HTML agus Scala. Cónaíonn na comhaid seo ar an bhfreastalaí agus úsáidtear iad chun leathanaigh ghréasáin statacha a chruthú le freastal ar úsáideoirí. Is teanga ríomhchláraithe ghinearálta í Scala féin a bhfuil eolas ag úsáideoirí a d’oibrigh le Velocity, JSP nó Erb ar chomhréir. Is féidir comhaid SSP a anailísiú agus a mheas trí úsáid a bhaint as [Scalate](https://scalate.github.io/scalate/), inneall teimpléid bunaithe ar Scala chun téacs agus marcáil a ghiniúint.

## Formáid Chomhaid SSP - Tuilleadh Eolais

Déantar comhaid SSP a shábháil i gcomhad gnáth-théacs agus is féidir iad a mheas ag úsáid Scála. Is éard atá i dteimpléad Ssp gnáth-théacs arb é an doiciméad HTML é níos minice. Tá clibeanna Ssp leabaithe ann a fhágann go ndéanann na hinnill rindreála codanna éagsúla den doiciméad a sholáthar go dinimiciúil. Tosaíonn agus críochnaíonn na clibeanna le seicheamh <% ... %> agus ${ ... } agus breathnaítear ar aon rud lasmuigh díobh seo mar théacs litriúil.

### Sampla SSP

Taispeánann an sampla seo a leanas cód SSP agus a aschur nuair a bhíonn sé rindreáilte ag an inneall rindreála.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Seo a leanas an t-aschur.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Tagairtí

- [SSP Reference](https://scalate.github.io/scalate/documentation/ssp-reference.html)

