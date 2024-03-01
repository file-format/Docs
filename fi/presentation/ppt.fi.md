{
  "date": "2019-12-13",
  "keywords": [
"ppt tiedosto",
"ppt tiedostomuoto",
"mikä on ppt-tiedosto",
"tiedosto",
"ppt esimerkki",
"ppt tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PPT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PPT-tiedostoja.",
  "title": "PPT - PowerPoint-tiedostomuoto",
  "linktitle": "PPT",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-pp-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PPT-tiedosto?

A file with PPT extension represents PowerPoint file that consists of a collection of slides for displaying as SlideShow. It specifies the Binary File Format used by Microsoft PowerPoint 97-2003. PPT-tiedosto voi sisältää useita erityyppisiä tietoja, kuten tekstiä, luettelomerkkejä, kuvia, multimediaa ja muita upotettuja OLE-objekteja. Microsoft kehitti PowerPointille uudemman tiedostomuodon, joka tunnetaan nimellä [PPTX](/presentation/pptx/), vuodesta 2007 alkaen ja joka perustuu Office OpenXML:ään ja eroaa tästä binääritiedostomuodosta. Useat muut sovellusohjelmat, kuten OpenOffice Impress ja Apple Keynote, voivat myös luoda PPT-tiedostoja.

## Lyhyt historia ##

Microsoft introduced the PPT file format with the release of PowerPoint in 1987. Vakaa binaarimuoto jaettiin oletuksena PowerPoint 97-2003 for Windowsissa. Binääritiedostomuotoa tukevat PowerPointin uusimmat versiot, mukaan lukien PowerPoint 2016, lukemiseen ja kirjoittamiseen.

## Tiedostomuodon tiedot ##

Käyttöönoton jälkeen PPT-tiedostomuoto on käynyt läpi useita päivityksiä uusien ominaisuuksien ja parannusten lisäämiseksi. Uusimmat saatavilla olevat versiot ovat elokuussa 2018 julkaistun version 6.0 tekniset tiedot, joita ei pidä sekoittaa PPT-tiedostomuodon todelliseen tuotenumeroon, koska Microsoft ei enää tarjoa tähän muotoon muutoksia.

### Tiedostomuodon yleiskatsaus ###

Jotkut PPT-tiedostomuodon tärkeimmistä osista ovat seuraavat:

#### Diat ####

Käyttäjätiedot, kuten muodot, teksti, animaatiot ja media, lisätään esitykseen dian sisällä. Esitys voi sisältää yhden tai useamman dian, jotka näytetään diaesityksenä esityksen aikana. Esitys sisältää kantadiat ja otsikon kantadiat, jotka toimivat mallina esityksen diojen yleisille visuaalisille ominaisuuksille. On myös muistiinpanojen kantadia ja monisteen kantadia, jotka palvelevat samanlaista tarkoitusta ja tarjoavat yhteiset visuaaliset ominaisuudet kaikille muistiinpanodioille ja kaikille painetuille monisteille.

#### Muodot ####

Muodot ovat objekteja, joiden avulla käyttäjät voivat lisätä erilaista sisältöä diaan paikkamerkkimuotojen, kuvien ja kaavioiden muodossa. Päädian muodot määrittävät yhteiset tiedot muotoryhmille.

#### Paikkamerkit Muodot ####

Nämä ovat erityisiä paikkamerkkejä, jotka toimivat erilaisten objektien säilytysastioina. Erilaisia paikkamerkkimuotoja voidaan käyttää antamaan vihjeitä tietyntyyppisten muotojen, kuten taulukoiden tai kaavioiden, lisäämiseen. Dian sisällä oleva paikkamerkkimuoto mukautuu päädian, otsikon kantadian tai muistiinpanojen kantadian visuaalisiin ominaisuuksiin.

#### Ulkoiset objektit ####

Ulkoisia objekteja, kuten upotettua ja linkitettyä ääntä, linkitettyä videota, upotettuja ja linkitettyjä OLE-objekteja ja hyperlinkkejä, voidaan upottaa diaan. Näitä objekteja voidaan käyttää linkitettyjen objektien aktivoimiseen ulkoisten resurssien käyttöä varten diaesityksen aikana.

### Tiedostomuotorakenteet ###

PowerPoint-binaaritiedostomuodot koostuvat seuraavista virroista, jotka edustavat asiakirjan yleistä rakennetta ja tietoja.

* Nykyinen käyttäjävirta

* PowerPoint Document Stream

* Kuvat Stream

* Yhteenvetotiedot ja asiakirjan yhteenvetotiedot (valinnainen)


Täydelliset DOC-tiedostomuodon tekniset tiedot löytyvät [Microsoft](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) -tiedostosta, ja niihin tulee tutustua seuraavissa tiedoissa mainituissa osissa.

#### Nykyinen käyttäjävirta ####

Se pitää kirjaa viimeisestä asiakirjan avanneesta käyttäjästä ja sen nimen tulee olla Nykyinen käyttäjä.

#### PowerPoint Document Stream ####

Pitää kirjaa kaikista PowerPoint-esityksen tiedoista ja selittää sen asettelun ja sisällön. Se on pakollinen tietovirta, jonka nimen TÄYTYY olla PowerPoint Document. Tämän virran sisältö määritetään huipputason tietueiden sarjalla. Tietuesekvenssin osittaiset järjestysrajoitukset on määritetty PersistDirectoryAtom- ja UserEditAtom-tietueissa.

Säilötietueina DocumentContainer-, MainMasterContainer- (osio 2.5.3), HandoutContainer- (osio 2.5.8), SlideContainer- (osio 2.5.1) ja NotesContainer-tietueet (osio 2.5.6) ovat kukin säilötietueiden puun juuri. ja atomiennätyksiä. Minkä tahansa säilötietueen sisällä voi olla muita tietueita, joita ei ole nimenomaisesti lueteltu alatietueiksi. Tuntemattomat tietueet tunnistetaan, kun RecordHeader-rakenteen recType-kenttä (osio 2.3.1) sisältää arvon, jota ei ole määritetty RecordType-luettelossa (osio 2.13.24). Nämä tuntemattomat tietueet TÄYTYY jättää huomiotta ja VOI<1> säilyttää. Tuntemattomat tietueet voidaan jättää huomiotta etsimällä recLen-tavuja eteenpäin RecordHeader-rakenteen lopusta.

Joka kerta kun tämä stream kirjoitetaan, olemassa olevaan streamiin voidaan liittää uusia ylimmän tason tietueita, käyttäjän muokkausta, tai koko streamin sisältö voidaan korvata päivitetyllä ylätason tietueiden sarjalla. Jos koko tietovirtaa ei korvata, kaikki aiemmin olemassa olevat ylimmän tason tietueet, jotka sisälsivät minkä tahansa aikaisemman käyttäjän muokkauksen, voidaan tehdä vanhentuneiksi myöhemmin liitetyillä ylätason tietueilla, jotka sisältävät nykyisen käyttäjän muokkauksen.

#### Kuvavirta ####

Tämä on valinnainen tietovirta, joka sisältää tietoja PowerPoint-esityksen sisältämistä kuvista. Sen nimen TÄYTYY olla Kuvat. Tämän virran sisällön määrittää OfficeArtBStoreDelay-tietue [MS-ODRAW]-osiossa 2.2.21 määritetyllä tavalla.

#### Yhteenvetotietovirta ####

Se pitää asiakirjasta tilastoja Microsoft Office -standardin mukaisesti. Yhteenvetotietovirran nimen on oltava \005SummaryInformation, jossa \005 on merkki, jonka arvo on 0x0005, ei merkkijono \005. Tämä stream PITÄÄ jättää pois salatuista asiakirjoista. Tämän virran sisältö on määritelty [MS-OSHARED]-osiossa 2.3.3.2.1.

#### Asiakirjan yhteenvetotietovirta ####

Valinnainen virta, jonka nimen TÄYTYY olla \005DocumentSummaryInformation, jossa \005 on merkki, jonka arvo on 0x0005, ei merkkijono \005. Tämä tietovirta VOI<2> jättää pois salatuista asiakirjoista. Tämän virran sisältö on määritelty [MS-OSHARED]-osiossa 2.3.3.2.2.

#### Salattu yhteenvetotietovirta ####

Valinnainen stream, jonka nimen TÄYTYY olla EncryptedSummary. Tämä tietovirta on olemassa vain salatussa asiakirjassa. Tämän virran sisältö on määritelty [MS-OFFCRYPTO] osiossa 2.3.5.4.

#### Digitaalisen allekirjoituksen tallennus ####

Valinnainen tallennustila, jonka nimen TÄYTYY olla _xmlsignatures. Se VOITTAA jättää pois ja jättää huomiotta. Tämän tallennustilan sisältö on määritelty [MS-OFFCRYPTO] osiossa 2.5.2.

#### Mukautettu XML-tietojen tallennus ####

Valinnainen tallennustila, jonka nimen TÄYTYY olla MsoDataStore. Tallennustilan sisältö on määritelty [MS-OSHARED] osiossa 2.3.6.

#### Allekirjoitusvirta ####

Valinnainen stream, jonka nimen TÄYTYY olla _signatures. Se PITÄÄ jättää pois ja VOITTAA jättää huomiotta. Tämän virran sisältö on määritelty [MS-OFFCRYPTO] osiossa 2.5.1.

## Viitteet ##

* [PPT-tiedostomuodon tiedot](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)

* [[MS-OSHARED]: Officen yleiset tietotyypit ja objektirakenteet](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)

* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)

* [PowerPoint-tiedostomuodot](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)


