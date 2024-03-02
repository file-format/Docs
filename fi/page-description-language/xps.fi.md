{
  "date": "2019-10-11",
  "keywords": [
"XPS",
"XML-paperin tekniset tiedot",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"EMF",
"PDF"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XPS - Sivun asettelutiedostomuoto",
  "description": "Opi XPS-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata XPS-tiedostoja.",
  "linktitle": "XPS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xp-fis"
}
},
  "lastmod": "2021-04-23"
}

## Mikä on XPS-tiedosto?

XPS-tiedosto edustaa sivun asettelutiedostoja, jotka perustuvat Microsoftin luomiin XML-paperimäärityksiin. Se kehitettiin korvaamaan EMF-tiedostomuoto ja on samanlainen kuin [PDF](/pdf/)-tiedostomuoto, mutta käyttää XML:ää asiakirjan asettelussa, ulkoasussa ja tulostustiedoissa. On itse asiassa oikeutetumpaa sanoa, että XPS on yritys PDF-tiedostoon, mutta se ei saanut tarpeeksi suosiota PDF:n omistamana monista syistä. Microsoft tarjoaa XPS Document Writerin oletuksena Windows 7:stä alkaen XPS-tiedostojen luomiseen. XPS-tiedostoja voidaan luoda valitsemalla tulostimeksi Microsoft XPS Document Writer asiakirjaa tulostettaessa.

XPS-katselulaitteet toimitetaan osana Windows Vistaa, Windows 7:ää, Windows 8:aa ja Internet Explorer 6:ta tai uudempaa. XPS-tiedostoista tulee vain luku -muotoisia, kun ne on luotu. Tämä lisää käyttäjän luottamusta XPS-muodossa lähetettyihin vastaanotettuihin asiakirjoihin asiakirjan aitouden vuoksi. XPS-asiakirja voi sisältää yhden tai useamman sivun alkuperäisestä asiakirjasta muunnettuina.

## Lyhyt historia ##

Microsoft toimitti XPS-eritelmän Ecma Internationalille. Kesäkuussa 2007 perustettiin Ecma Technical Committee 46 (TC46) kehittämään OpenXPS-paperispesifikaatioihin perustuva standardi. Ecma International hyväksyi Ecma-standardin (ECMA-388) [XPS specifications](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) kesäkuussa 2009 97. yleiskokouksessa.

## XPS-tiedostomuoto ##

XPS-muoto koostuu XML-merkinnöistä, jotka määrittelevät asiakirjan koostumuksen ja kunkin sivun visuaalisen ulkoasun sekä asiakirjan näyttämistä tai tulostamista koskevat renderöintisäännöt. Se säilyttää kaikki tiedot asiakirjan luomiseksi uudelleen missä tahansa järjestelmässä, mikä tekee siitä riippumattoman kyseisessä järjestelmässä käytettävissä olevista resursseista. Muoto on pohjimmiltaan ZIP-arkisto, ja jos nimeät tiedostotunnisteen uudelleen ZIP:ksi, näet tiedostot, jotka sisältävät asiakirjan tiedot. Näitä asiakirjoja ovat:

* Asiakirjan sivutiedostot (.fpage) - Sisältää asiakirjan sisällön ja asiakirjan muotoasetukset. Jokaisella XPS-asiakirjan sivulla on yksi FPAGE-tiedosto.

* Asiakirjan asetustiedosto (.fdoc) - Tallentaa XPS-arkistoon sisältyvät asetukset.

* Asiakirjan fragmenttitiedostot (.frag) - Määrittää todellisen XPS-tiedoston asetukset ja jokaisella asiakirjan sivulla on oma .frag-tiedosto.


{{< figure src="../XPS-1.png" alt="XPS tiedostomuoto" >}}

Nämä tiedostot säilyttävät asiakirjan sisällön siten, että jos esimerkiksi jollain ei ole samoja fontteja asennettuna koneelleen, XPS-katseluohjelma hahmontaa silti alkuperäiset kirjasimet. Tämä edellyttää XML-merkintätiedoston sisällyttämistä jokaiseen:

* Sivu

* Teksti

* Upotetut fontit

* Rasterikuvia

* 2D-vektorigrafiikka

* Digitaalinen oikeuksien hallinta


XPS-dokumenttimuoto sisältää hyvin määritellyn joukon osia ja suhteita, joista jokainen täyttää asiakirjassa tietyn tarkoituksen. Muoto laajentaa myös paketin ominaisuuksia, mukaan lukien digitaaliset allekirjoitukset, pikkukuvat ja lomitus.

Tyypillinen XPS-asiakirja näyttää seuraavalta, ja sitä voidaan analysoida XPS-tiedostomuodon specifications valossa.

{{< figure src="../XPS-2.png" alt="XPS tiedostomuoto" >}}


## Viitteet ##

* [XPS-tiedostomuodon tekniset tiedot](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)

* [XPS - Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)


