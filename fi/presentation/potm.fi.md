{
  "date": "2019-10-11",
  "keywords": [
"potm tiedosto",
"potm-tiedostomuoto",
"mikä on potm-tiedosto",
"tiedosto",
"potm esimerkki",
"potm tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "POTM - Microsoft PowerPoint -mallitiedosto makroilla",
  "description": "Opi POTM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata POTM-tiedostoja.",
  "linktitle": "POTM",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pot-fim"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on POTM-tiedosto?

POTM-laajennuksella varustetut tiedostot ovat Microsoft PowerPoint -mallitiedostoja, jotka tukevat makroja. POTM-tiedostot luodaan PowerPoint 2007:llä tai uudemmalla, ja ne sisältävät oletusasetukset, joita voidaan käyttää lisäesitystiedostojen luomiseen. Nämä asetukset voivat sisältää tyylejä, taustoja, väripalettia, fontteja ja oletusasetuksia sekä makroja, jotka koostuvat mukautetuista toiminnoista tietyn tehtävän suorittamista varten. Ne voidaan avata myös PowerPointin aiemmalla versiolla, johon on asennettu Open XML -dokumenttituki. POTM-tiedostot voidaan avata Microsoft PowerPointissa muokkausta varten kuten mikä tahansa muu PowerPoint-tiedosto.

## Tiedostomuodon tiedot ##

POTM-tiedostomuoto perustuu Office OpenXML-spesifikaatioihin ja muistuttaa rakennetta [PPTX](/presentation/pptx/)-tiedostosta, joka on pakattu [ZIP](/compression/zip/)-arkisto.

POTM-tiedoston sisällä olevat diot voivat sisältää tekstiä, kuvia, videoita, grafiikkaa ja muita objekteja, jotka voidaan järjestää vapaasti sivulla. POTM-malleja käytetään sitten useiden tiedostojen luomiseen, jotka perivät kaikki tiedoston muotoiluasetukset. POTM-tiedoston sisältämät makrot periytyvät siis myös muilta esityksiltä. Niiden upottaminen asiakirjan rakenteeseen tapahtuu MS Officen Macro Recorderin avulla, joka voi tallentaa komentosarjoja ja luoda makroja kopioidakseen ne automaattisesti.

Office Open XML -tiedostomuodolla luodut tiedostot on kokoelma XML-tiedostoja sekä muita tiedostoja, jotka tarjoavat linkit kaikkien osatiedostojen välillä. Tämä kokoelma on itse asiassa pakattu arkisto, joka voidaan purkaa ja tarkastella sen sisältöä. Voit tehdä tämän nimeämällä POTM-tiedostotunnisteen uudelleen zip:llä ja purkamalla sen sisällön tarkkailemista varten.

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

* [[MS-PPTX] - PPTX-tiedostomuoto](https://msdn.microsoft.com/en-us/library/dd926741(v#office.12).aspx)

* [Open Office XML](http://officeopenxml.com/anatomyofOOXML-pptx.php)


