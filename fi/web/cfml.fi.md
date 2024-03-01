{
  "date": "2021-08-19",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFML - ColdFusion Markup Language File",
  "description": "Opi mikä on CFML-tiedosto ja API:t, jotka voivat luoda ja avata CFML-tiedostoja.",
  "linktitle": "CFML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-cfm-fil"
}
},
  "lastmod": "2021-08-19"
}

## Mikä on CFML-tiedosto?

Tiedosto, jonka pääte on .cfml, on ColdFusion Markup Language -tiedosto, jota käytetään verkkosivun luomiseen. Se viittaa sääntöihin, joita käytetään määrittämään, kuinka ohjelmoija kehittää ColdFusion-sovelluksen. ColdFusion on ohjelmointikieli, jota käytetään luomaan palvelinpuolen verkkosovelluksia nopeasti ja vähemmän kuin muut tekniikat, kuten [ASP](/web/asp/), [PHP](/programming/php/) jne. Joitakin sovelluksia, jotka voivat avata CML-tiedostoja, ovat mm. Adobe ColdFusion 2018, Adobe ColdFusion Builder ja Adobe Dreamweaver.

## CFML-tiedostomuoto – lisätietoja

CFML-tiedostot ovat merkintätiedostoja ja sisältävät verkkoelementtejä tunnisteiden muodossa. Nämä ovat tekstitiedostoja, jotka voidaan avata ja muokata missä tahansa tekstieditorissa. CFML-tiedostot koostuvat useista tunnisteista, jotka ovat samankaltaisia kuin [HTML](/web/html/) ja sisältävät yleensä aloitus- ja sulkemistunnisteen. Nämä tunnisteet voivat sisältää myös yhden tai useamman attribuutin.

### Tunnisteiden syntaksi

Seuraavassa on CFML-tunnisteiden yleinen syntaksi.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Useimmat tunnisteet hyväksyvät attribuutit ja ne määritellään seuraavasti.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Jotkut näistä tunnisteista hyväksyvät myös useita määritteitä seuraavalla syntaksilla.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Esimerkki CFML-koodista

Tässä on esimerkki, joka käyttää todellista CFML-tunnistetta - cfoutput-tunnistetta:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Viitteet

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)


