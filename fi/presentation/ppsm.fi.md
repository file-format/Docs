{
  "date": "2019-10-11",
  "keywords": [
"ppsm tiedosto",
"ppsm tiedostomuoto",
"mikä on ppsm-tiedosto",
"tiedosto",
"ppsm esimerkki",
"ppsm tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PPSM - Makrokäyttöinen PowerPoint-esitystiedosto",
  "description": "Opi PPSM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PPSM-tiedostoja.",
  "linktitle": "PPSM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pps-fim"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PPSM-tiedosto?

PPSM-laajennuksella varustetut tiedostot edustavat Macro-yhteensopivaa diaesitystiedostomuotoa, joka on luotu Microsoft PowerPoint 2007:llä tai uudemmalla. Toinen samanlainen tiedostomuoto on [PPTM](/presentation/pptm/), joka eroaa Microsoft PowerPointin avaamisesta muokattavassa muodossa sen sijaan, että se toimisi diaesityksenä. Kun PPSM-tiedosto suoritetaan diaesityksenä, se näyttää esityksen diat sisällöltään ennallaan ja se on oletusarvoisesti vain luku -tilassa. PPSM-tiedostoja voidaan edelleen muokata Microsoft PowerPointissa avaamalla se PowerPointissa.

## Tiedosto muoto ##

PPSM-tiedostomuoto otettiin käyttöön PowerPoint 2007:n kanssa, ja se perustuu OpenXML-tiedostomuotoon, joka käyttää XML:n ja [ZIP](/compression/zip/):n yhdistelmää sisällön tallentamiseen. Office Open XML -tiedostomuodolla luodut tiedostot on kokoelma XML-tiedostoja sekä muita tiedostoja, jotka tarjoavat linkit kaikkien osatiedostojen välillä. Tämä kokoelma on itse asiassa pakattu arkisto, joka voidaan purkaa ja tarkastella sen sisältöä. Voit tehdä tämän nimeämällä PPSM-tiedostotunnisteen uudelleen zip:llä ja purkamalla sen sisällön tarkkailemista varten.

Seuraavat osiot valaisevat jokaista näistä.

### [Content_Types].xml ###

Tämä on ainoa tiedosto, joka löytyy perustasolta, kun zip-tiedosto puretaan. Siinä luetellaan paketin osien sisältötyypit. Kaikki viittaukset paketin XML-tiedostoihin viitataan tässä XML-tiedostossa. Seuraava on diaosan sisältötyyppi:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jos pakettiin on lisättävä uusia osia, se voidaan tehdä lisäämällä uusi osa ja päivittämällä mahdolliset suhteet .rels-tiedostoissa. On pidettävä mielessä, että tällaista muutosta varten Content_Types.xml on myös päivitettävä.

### \_rels (kansio) ###

Muiden osien ja paketin ulkopuolisten resurssien välisiä suhteita ylläpitää suhteet-osa. Relationships-kansio sisältää yhden XML-tiedoston, joka tallentaa pakettitason suhteet. Linkit esitystiedostojen tärkeimpiin osiin sisältyvät tähän tiedostoon URI-tunnuksina. Nämä URI:t tunnistavat kunkin avainosan ja paketin suhteen tyypin. Tämä sisältää suhteen ensisijaiseen Office-asiakirjaan, joka sijaitsee ppt/presentation.xml-muodossa, ja muita docPropsin osia ydin- ja laajennettuina ominaisuuksina.
```
<Relationship Id#"rId1" Type#"http:~/~/schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"ppt/presentation.xml"/>.
```
Jokaisella asiakirjan osalla, joka on yhden tai useamman suhteen lähde, on oma suhdeosa, jossa jokainen tällainen suhdeosa löytyy osan \_rels-alikansiosta ja nimetään lisäämällä '.rels' tiedoston nimeen. osa. Pääsisältöosalla (presentation.xml) on oma suhdeosa (presentation.xml.rels). Se sisältää suhteita muihin sisällön osiin, kuten slideMaster1.xml, notesMaster1.xml, handoutMaster1.xml, slide1.xml, presProps.xml, tableStyles.xml, theme1.xml sekä ulkoisten linkkien URI:t.

#### Eksplisiittinen suhde ####

Eksplisiittisessä suhteessa resurssiin viitataan käyttämällä a:n Id-attribuuttia<Relationship> elementti. Toisin sanoen lähteen Id kartoitetaan suoraan suhdealkion tunnukseen, jossa on selkeä viittaus kohteeseen.

Dia voi sisältää esimerkiksi seuraavanlaisen hyperlinkin:
```
<a:hlinkClick r:id#"rId2">
```
R:id#rId2 viittaa seuraavaan suhteeseen dian suhdeosassa (slide1.xml.rels).
```
<Relationship Id#"rId2" Type#"http:~/~/. . ./hyperlink" Target#"http:~/~/www.google.com/" TargetMode#"External"/>
```
#### Implisiittinen suhde ####

Implisiittisessä suhteessa ei ole tällaista suoraa viittausta `<Relationship> Id`. Sen sijaan viittaus ymmärretään.

### ppt-kansio ###

Tämä on pääkansio, joka sisältää kaikki tiedot esityksen sisällöstä. Oletuksena siinä on seuraavat kansiot:

* \_rels

* teema

* diat

* slideLayouts

* slideMasters


ja seuraavat xml-tiedostot:

* esitys.xml

* presProps.xml

* tableStyles.xml

* viewProps.xml


## Viitteet ##

* [OpenXML-esitystiedostomuoto](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


