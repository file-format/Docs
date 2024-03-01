{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PÄÄtiedosto - ASP.NET-pääsivun tiedostomuoto",
  "description" : "Opi MASTER-tiedostomuodosta ja API-liittymistä MASTER-tiedostojen luomiseen ja avaamiseen.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master-fi",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Mikä on MASTER-tiedosto?

MASTER-tiedosto on ASP.NET:llä luotu web-sivun mallipohjatiedosto. Sitä käytetään lähtökohtana luotaessa useita sivuja, joilla on sama asettelu ja asetukset kuin MASTER-tiedostolla. Mallin MASTER-tiedosto sisältää ylätunnisteen, navigointivalikoiden, alatunnisteen, fontin ja tyylitietojen asetukset. MASTER-tiedoston käyttäminen auttaa luomaan useita verkkosivuja nopeasti.

Voit avata MASTER-tiedoston Microsoft Visual Studio 2022:lla tai uudemmalla.

## MASTER-tiedostomuoto - lisätietoja

MASTER-tiedosto luodaan ja tallennetaan HTML-tiedostomuodossa, ja se on samanlainen kuin mikä tahansa muu verkkosivun tiedosto. Se on jaettu muokattavissa oleviin ja ei-muokattaviin osiin. Muokattavat osat ovat niitä, joita voidaan muokata vastaamaan käyttäjän vaatimuksia. Ei-muokattavat osat näkyvät harmaina, kun MASTER-tiedosto avataan Microsoft Visual Studiossa.

Pääsivut koostuvat kahdesta osasta eli itse sivupohjasta ja yhdestä tai useammasta sisältösivusta.

### PÄÄsivu

Pääsivulla on .master-tunniste ja se on tehty ASP.NETissä. Siinä on ennalta määritetty asettelu, joka sisältää staattista tekstiä, HTML-tunnisteita ja palvelinpuolen ohjaimia. Tavallisilla .aspx-sivuilla käytetään @ Page -direktiiviä. .master-tiedostojen tapauksessa tämä korvataan @-pääkäskyllä.

### Sisältösivut

Sisältösivu edustaa sivupohjan paikkamerkkisäätimien sisältöä. Nämä ovat .aspx-sivuja, jotka ovat itse asiassa pääsivun takana oleva koodi. Sisältösivut sidotaan @ Page -ohjeella lisäämällä MasterPageFile-attribuutti, joka osoittaa sivupohjaan käytettäväksi alla kuvatulla tavalla.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Viitteet

* [ASP.NET Master Pages Overview](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))


