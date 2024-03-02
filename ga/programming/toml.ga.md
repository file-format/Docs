---
date: 2019-10-11
keywords: toml, .toml, toml file format, how to open toml files, .toml extension, toml extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: TFoirm Chomhaid OMLat
linktitle: TOML
description: Ltuilleamh faoi fhormáid comhaid TOML agus APIs ar féidir leo comhad TOML a chruthú agus a oscailts.
menu:
  docs:
    parent: "programming"
lastmod: 2020-12-01
---

## Cad is comhad TOML ann? ##

Is formáid comhaid cumraíochta íosta é TOML (Teanga Íosta Soiléir Tom) a úsáideann an síneadh .toml. Tá sé mar aidhm ag TOML a bheith éasca le léamh, mapáil gan athbhrí ar fhoclóirí, agus a bheith éasca a pharsáil chuig struchtúir sonraí éagsúla. Tá sonraíocht foinse oscailte ag TOML a fuair ranníocaíochtaí pobail. Tacaíonn go leor teangacha ríomhchlárúcháin le TOML mar C, C#, Dart, Elixir, Erlang, Go, Java, PHP, Python, Ruby, Swift, etc. Is é an cineál MIME do chomhaid TOML ná *app/toml*.


## Formáid Chomhaid TOML ##

Is éard atá i gcomhaid TOML go príomha ná Péirí eochair/luacha, ranna/táblaí, nótaí tráchta agus caithfidh gur doiciméad bailí Unicode ionchódaithe UTF-8 iad. Tacaíonn TOML le cineálacha sonraí Teaghrán, Slánuimhir, Snámhphointe, Boole, Datetime, Array, agus Tábla (hash tábla / foclóir). Teanga chás-íogair is ea TOML.

### Comhréir ###

- **Péirí Príomhluacha**: Déantar péirí eochairluacha a dheighilt le comhartha comhionann (=). Caithfidh gach péire a bheith ar líne nua.

```toml
chéad = Tom
last = Preston-Werner
```

- **Tuairimí**: Tosaíonn na tuairimí leis an tsiombail hash (#).

```toml
# Is doiciméad TOML é seo.
```

- **Teaghráin**: Tá comharthaí athfhriotail () timpeallaithe ag teaghráin.

```toml
string = Teaghrán Samplach
```

- **Teaghráin Illíne**: Tá trí mharc athfhriotail () timpeallaithe ag Teaghráin Illíne.

```toml
[seoladh baile]
sráid =  123 Alley Tornado
Suite 16
cathair = East Centerville
stát = KS
```

- **Slánuimhreacha/Snámháin**

```toml
slánuimhir = 20
snámhphointe = 20.5
```

- **Booleans**: Is cás íochtair na Booles i gcónaí.

```toml
bool1 = fíor
bool2 = bréagach
```

- **Date-Time**: For DateTime, you may use an RFC 3339 formatted date-time as shown in the example below.

```toml
  offset_date_time = 1979-05-27 07:32:00Z
  local_date_time = 1979-05-27T07:32:00
logánta_dáta = 1979-05-27
local_time = 07:32:00
```

- **Arrays**: Tá lúibíní cearnacha timpeallaithe ar eagair le heilimintí atá scartha le camóga (,).

```toml
dathanna = [ dearg, buí, glas ]
```

- **Táblaí**: Is éard atá i dtáblaí ná bailiúcháin de phéirí eochair/luacha atá sainmhínithe ag ceanntásca ar líne nua agus lúibíní cearnacha timpeall orthu ([]). Críochnaíonn an tábla nuair a chuirtear ceanntásc nua ar fáil nó nuair a chríochnaíonn an comhad.

```toml
[seoladh baile]
sráid =  123 Alley Tornado
Suite 16
cathair = East Centerville
stát = KS

[seoladh oifige]
sráid =  123 Alley Tornado
Suite 16
cathair = East Centerville
stát = KS
```

Tá na táblaí inlíne timpeallaithe ag braces curly ({}) agus gach péire eochair/luacha scartha le camóg (,).

```toml
ainm = { chéad = Tom, deireanach = Pitt }
```

## Tagairtí ##

- [TOML - Wikipedia](https://en.wikipedia.org/wiki/TOML)
- [TOML](https://toml.io/en/)

