{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMV tiedostomuoto",
  "description": "Opi WMV-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WMV-tiedostoja.",
  "linktitle": "WMV",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-wm-fiv"
}
},
  "lastmod": "2019-09-16"
}

## Mikä on WMV-tiedosto?

Advanced Systems Format (ASF) on digitaalinen multimediasäiliö, joka on suunniteltu ensisijaisesti mediavirtojen tallentamiseen ja lähettämiseen. Microsoft Windows Media Video (WMV) on pakattu videomuoto ja Microsoft Windows Media Audio (WMA) on pakattu äänimuoto sekä lisämetatiedot Microsoftin kehittämässä ASF-säiliössä. Kun WMV- tai WMA-tiedostot on koodattu Windows Media Video- ja Windows Media Audio -koodekeilla, ne esitetään .asf-tunnisteella. WMV pakkaa suuret tiedostot paremman siirtonopeuden saavuttamiseksi verkossa säilyttäen samalla videon laadun. WMV on erityisesti suunniteltu toimimaan kaikissa Windows-laitteissa. Society of Motion Picture and Television Engineers (SMPTE) standardoinnin jälkeen WMV:tä pidetään nyt avoimena standardimuotona.

## Historia ##

With the help of Microsoft proprietary codecs new compressed video format was developed in 1999 known as WMV7 which was based on MPEG-4 Part 2. Parannuksia lisättiin kahteen muuhun versioon, eli WMV8:aan ja 9:ään. Microsoft toimitti 9^^th^^-version WMV:stä SMPTE:lle standardointia varten vuonna 2003, joka lopulta standardoitiin vuonna 2006 nimellä SMPTE 421M, joka tunnetaan myös nimellä VC-1. WMV:n ideana oli kehittää mediamuoto, jota kaikki Microsoftin tukemat laitteistot ja ohjelmistot voisivat tukea. Lisäksi toinen tärkeä tarkoitus oli siirtää videovirtoja Internetin kautta optimaalisessa tilanteessa. SMPTE:n standardoinnin jälkeen WMV:stä tuli myös Blu-ray-levyjen videoformaatti.

## Tiedostomuodon tekniset tiedot

### Säiliö

Yleensä WMV pakataan ASF-säiliöön, mutta lisäksi Matroska tai AVI-säiliö voi tukea sitä myös .mkv- ja .avi-laajennuksilla.

### Windows Media Video 9

Vaikka Windows Media Video 9 -sarjassa on saatavilla useita ääni- ja videokoodekkeja digitaalisen median luomiseen ja toistoon, WMV-9-koodekki on uusin ja paras videokoodekki, sillä se voi saavuttaa optimaalisen pakkauksen erittäin alhaisilla bittinopeuksilla eli 160 x 120 nopeudella 10 Kb/s – 1920 x 1080 nopeudella 4–8 Mb/s erilaisille HD-videoille.

### Codecin rakenne

WMV-9:ssä on 8-bittinen 4:2:0 sisäinen värimuoto. Kuten kaikki muutkin suositut videopakkausstandardit MPEG-1 ja H.261, WMV-9 käyttää lohkopohjaista liikkeen kompensointia ja tilamuunnosjärjestelmää. Yleisesti voidaan sanoa, että nämä standardit suorittavat lohko-lohkolta liikkeen kompensoinnin edellisestä rekonstruoidusta kehyksestä liikevektoriksi (MV) kutsutun 2-D-suureen avulla tilasiirtymän signaloimiseksi. Nykyinen lohko muodostetaan ennustamalla arvot samankokoisesta edellisestä rekonstruoidusta kehyksestä, jota liikevektori siirtää nykyisestä sijainnista. Lopulta jäännösvirhe lasketaan liikekompensoidun ennustetun lohkon ja todellisen lohkon välisenä erona. Tämä jäännösvirhe muunnetaan käyttämällä lineaarista energiaa tiivistävää muunnosta, sitten kvantisoidaan ja entropiakoodataan.

Quantized transform coefficients are entropy decoded, de-quantized, and inverse transformed to produce an approximation of the residual error on the decoder side, which is then added to the motion-compensated prediction to generate the reconstruction. The high-level description of the codec is shown in the following image.

Jakson loppuosassa käsitellään WMV-9:n uusia parannuksia, jotka erottavat sen muista videokoodausratkaisuista, kuten MPEG-standardeista. WMV-9:llä on sisäiset (I), ennustetut (P) ja kaksisuuntaisesti ennustetut (B) kehykset. Sisäiset kehykset ovat niitä, jotka koodataan itsenäisesti ja jotka eivät ole riippuvaisia muista kehyksistä. Ennustetut kehykset ovat kehyksiä, jotka riippuvat yhdestä menneisyydestä. Ennustetun kehyksen dekoodaus voi tapahtua vasta sen jälkeen, kun kaikki viitekehykset ennen nykyistä kehystä viimeisimmästä (I) kehyksestä alkaen on dekoodattu. B-kehykset ovat kehyksiä, joilla on kaksi viittausta – yksi ajalliseen menneisyyteen ja toinen ajalliseen tulevaisuuteen. B-kehykset lähetetään niiden viittausten jälkeen, mikä tarkoittaa, että B-kehykset lähetetään epäjärjestyksessä sen varmistamiseksi, että niiden viitteet ovat saatavilla dekoodauksen aikana. WMV-9:n B-kehyksiä ei käytetä viitteenä seuraaville kehyksille. Tämä asettaa B-kehykset dekoodaussilmukan ulkopuolelle, jolloin B-kehysten dekoodauksen aikana voidaan ottaa pikakuvakkeita ilman ajautumista tai pitkäaikaisia visuaalisia artefakteja. Yllä oleva I-, P- ja B-kehysten määritelmä pätee sekä progressiivisille että lomitetuille sekvensseille.

Videokoodekkien suorituskykyä verrataan niiden nopeusvääristymän (RD) kuvaajaan. Se on 2-D-käyrä, joka näyttää pakkaamisen aiheuttaman vääristymän tietyllä bittinopeudella.

WMV-9 on ratkaissut tämän ongelman ottamalla käyttöön useita alla lueteltuja tekniikoita:

1. Mukautuva lohkokoon muunnos

2. Rajoitettu tarkkuus muunnossarja

3. Liikekompensointi

4. Kvantisointi ja dekvantisointi

5. Kehittynyt entropiakoodaus

6. Silmukkasuodatus

7. Edistynyt B-kehyskoodaus

8. Lomitettu koodaus

9. Limityksen tasoitus

10. Halvat työkalut

11. Häipymisen kompensointi

## Viitteet

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html )

* [https://en.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


