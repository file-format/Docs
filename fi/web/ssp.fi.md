---
date: 2021-07-05
keywords: ssp, .ssp, ssp file format, how to open ssp files, Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages -tiedostolomakeat
linktitle: SSP
description: Ltienaa SSP-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SSP-tiedostons.
menu:
  docs:
    identifier: "web-ss-fip"
    parent: "web"
lastmod: 2021-09-30
---

## Mikä on SSP-tiedosto?

Tiedosto, jonka pääte on .ssp, on verkkosivu, joka on luotu Scala-koodilla lausekkeille pelkän HTML:n sijaan. Se toimii palvelinpuolen komentosarjana käyttämällä HTML:n ja Scalan yhdistelmää. Nämä tiedostot sijaitsevat palvelimella, ja niitä käytetään staattisten verkkosivujen luomiseen käyttäjille. Scala itsessään on yleiskäyttöinen ohjelmointikieli, jonka syntaksi on tuttu käyttäjille, jotka ovat työskennelleet Velocityn, JSP:n tai Erbin kanssa. SSP-tiedostoja voidaan analysoida ja arvioida käyttämällä [Scalate](https://scalate.github.io/scalate/), joka on Scala-pohjainen mallimoottori tekstin ja merkintöjen luomiseen.

## SSP-tiedostomuoto – lisätietoja

SSP-tiedostot tallennetaan vain tekstitiedostoon, ja ne voidaan arvioida Scalatella. Ssp-malli koostuu pelkkää tekstiä, joka on useammin HTML-dokumentti. Siihen on upotettu Ssp-tunnisteet, jotka saavat renderöintikoneet renderöimään asiakirjan eri osia dynaamisesti. Tunnisteet alkavat ja päättyvät sekvenssiin <% ... %> ja ${ ... }, ja kaikkea näiden ulkopuolella pidetään kirjaimellisena tekstinä.

### SSP Esimerkki

Seuraava esimerkki näyttää SSP-koodin ja sen ulostulon, kun renderöintikone hahmontaa sen.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
Tulos on seuraava.
```
<p>
  hi there reader!
  yo 7
</p>
```

## Viitteet

- {{HYPERLINKKI1}}

