{
  "date": "2019-10-11",
  "keywords": [
"potx tiedosto",
"potx tiedostomuoto",
"mikä on potx-tiedosto",
"tiedosto",
"potx esimerkki",
"potx tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "POTX - Microsoft PowerPoint -esitysmalli",
  "description": "Opi POTX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata POTX-tiedostoja.",
  "linktitle": "POTX",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pot-fix"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on POTX-tiedosto?

POTX-laajennuksella varustetut tiedostot edustavat Microsoft PowerPoint -malliesityksiä, jotka on luotu Microsoft PowerPoint 2007:llä tai uudemmalla. Tämä muoto luotiin korvaamaan [POT](/presentation/pot/)-tiedostomuoto, joka perustuu binääritiedostomuotoon ja jota PowerPoint 97-2003 tukee. Luotujen tiedostojen avulla voidaan luoda esityksiä, joilla on sama asettelu ja muut asetukset, joita tarvitaan uusiin tiedostoihin. Nämä asetukset voivat sisältää tyylejä, taustoja, väripalettia, fontteja ja oletusasetuksia. Tällaisia tiedostoja luodaan, jotta voidaan luoda valmiita mallitiedostoja virallista käyttöä varten.

## Lyhyt historia ##

Vuoden 2000 alussa Microsoft päätti tehdä muutoksen mukauttaakseen **Office Open XML -standardin**. Tämän uuden standardin mukaiset erityyppiset asiakirjat tunnistettiin lisäämällä X niiden laajennuksiin, missä X tarkoittaa XML:ää. Vuoteen 2007 mennessä tämä uusi tiedostomuoto tuli osaksi Office 2007:ää, ja sitä käytetään myös Microsoft Officen uusissa versioissa. Uusi tiedostotyyppi on lisännyt etuja: pienet tiedostokoot, vähemmän muutoksia korruptiossa ja hyvin muotoiltujen kuvien esitys.

## Tiedostomuodon tiedot ##

Office Open XML -tiedostomuodolla luodut tiedostot on kokoelma XML-tiedostoja sekä muita tiedostoja, jotka tarjoavat linkit kaikkien osatiedostojen välillä. Tämä kokoelma on itse asiassa pakattu arkisto, joka voidaan purkaa ja tarkastella sen sisältöä. Voit tehdä tämän nimeämällä POTX-tiedostotunnisteen uudelleen zip:llä ja purkamalla sen sisällön tarkkailemista varten.

Seuraavat osiot valaisevat jokaista näistä.

### [Content_Types].xml ###

Tämä on ainoa tiedosto, joka löytyy perustasolta, kun zip-tiedosto puretaan. Siinä luetellaan paketin osien sisältötyypit. Kaikki viittaukset paketissa oleviin XML-tiedostoihin viitataan tässä XML-tiedostossa. Seuraava on diaosan sisältötyyppi:
```
<Override PartName#"/ppt/slides/slide1.xml" ContentType#"application/vnd.openxmlformats-officedocument.presentationml.slide+xml"/>
```
Jos pakettiin on lisättävä uusia osia, se voidaan tehdä lisäämällä uusi osa ja päivittämällä mahdolliset suhteet .rels-tiedostoissa. On pidettävä mielessä, että tällaista muutosta varten Content_Types.xml on myös päivitettävä.

### \_rels (kansio) ###

Muiden osien ja paketin ulkopuolisten resurssien välisiä suhteita ylläpitää suhteet-osa. Relationships-kansio sisältää yhden XML-tiedoston, joka tallentaa pakettitason suhteet. Linkit PPTX-tiedostojen tärkeimpiin osiin sisältyvät tähän tiedostoon URI-tunnuksina. Nämä URI:t tunnistavat kunkin avainosan ja paketin suhteen tyypin. Tämä sisältää suhteen ensisijaiseen Office-asiakirjaan, joka sijaitsee ppt/presentation.xml-muodossa, ja muita docPropsin osia ydin- ja laajennettuina ominaisuuksina.
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


