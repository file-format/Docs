{
  "date": "2019-12-12",
  "keywords": [
"JT",
"tiedosto",
"laajennus",
"muoto",
"3D fbx",
""
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi JT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata JT-tiedostoja.",
  "title": "JT - Jupiter Tesselation -tiedostomuoto",
  "linktitle": "JT",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-j-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on JT-tiedosto?

**JT** (Jupiter Tessellation) on Siemens PLM Softwaren kehittämä tehokas, teollisuuskeskeinen ja joustava ISO-standardoitu 3D-tietomuoto. Ilmailun, autoteollisuuden ja raskaan kaluston mekaaniset CAD-alueet käyttävät JT:tä johtavana 3D-visualisointimuotonaan.

JT-muoto on kohtauskaavio, joka tukee CAD-kohtaisia määritteitä ja solmuja. Kehittyneitä pakkaustekniikoita käytetään fasettitietojen (kolmioiden) tallentamiseen. Tämä muoto on rakennettu tukemaan visuaalisia määritteitä, tuote- ja valmistustietoja (PMI) ja metatietoja. Sisällön asynkroniselle suoratoistolle on hyvä tuki. Raskaan mekaniikkateollisuuden ammattilaiset käyttävät JT-tiedostoa CAD-ratkaisuissaan ja tuotteen elinkaarihallintaohjelmistoissa (PLM) monimutkaisten tavaroiden geometrian tutkimiseen.

As JT supports nearly all important 3D CAD formats its assembly can deal with a variety of combination which is known as "multi-CAD". This multi-CAD assembly is always well managed and up-to-date because synchronization among native CAD product description files with their associated JT files takes place automatically. JT files are originally lightweight, so considered to be suitable for internet collaborations. Companies Collaborate through sending 3D visualizations over the media much more easily as compared to “heavy" original CAD files. In addition, JT files ensures many security feature that make intellectual property sharing more secure.

## JT-tiedostomuodon lyhyt historia

Engineering Animation, Inc. ja Hewlett Packard olivat JT:n alkuperäisiä suunnittelijoita, jotka kehittivät tämän muodon Direct Model Toolkitiksi. Kun UGS Corp osti EAI:n, JT:stä tuli osa UGS:n sviittiä. Vuoden 2007 alussa UGS julkisti JT:n master-3D-formaatiksi. Samana vuonna Siemens AG osti UGS:n ja osoittautui Siemens PLM Softwareksi. Siemens käyttää JT:tä yhteisenä yhteentoimivuusmuotona ja tiedonarkistointimuotona. Vuonna 2009 ISO hyväksyi JT-spesifikaation julkaistavaksi ISO Publicly Available -määrityksenä (PAS). Vuoden 2010 puolivälissä ProSTEP iViP ilmoitti, että teollisella tasolla JT:tä ja STEP AP 242 XML:ää voidaan käyttää yhdessä maksimaalisen dataedun saavuttamiseksi. vaihtaa skenaarioita. Vuonna 2012 JT on virallisesti julistettu ISO-standardoiduksi (ISO 14306:2012 (ISO JT V1)) 3D-visualisointiformaatiksi.

## JT-tiedostomuoto ##

Kaikki JT-muodossa olevat objektit esitetään objektitunnisteen kautta ja objektien väliset viittaukset käsitellään viitatun objektin tunnisteen kautta. Näiden objektiviittausten eheys voidaan ylläpitää osoittimien unswizzling/swizzling avulla.

JT-tiedosto on järjestetty sarjaksi lohkoja ja otsikkolohko on aina tiedoston ensimmäinen tietolohko. Tietosegmenttien sarja ja TOC-segmentti seuraavat välittömästi otsikkolohkoa. Yhdellä datasegmentillä (6 LSG-segmenttiä) on viiteyhteensopiva JT-tiedosto aina olemassa. TOC-segmentti sisältää kaikkien muiden kyseisen tiedoston tietosegmenttien sijaintitiedot.

{{< figure src="../JT-1.png" alt="JT tiedostomuoto" >}}

### Tiedoston otsikko ###

Tiedoston otsikko on ensimmäinen lohko JT-tiedoston tietohierarkiassa. Versiotiedot ja TOC-sijaintitiedot on suljettu otsikon sisään, mikä helpottaa lataajia tiedostojen lukemisessa. Tiedoston otsikon sisältö on järjestetty seuraavasti.

### TOC-segmentti ###

TOC-segmentin on oltava tiedostossa, ja se sisältää kaikkien muiden datasegmenttien tunniste- ja sijaintitiedot. TOC-segmentin todellinen sijainti määritetään tiedoston otsikon TOC Offset -kentässä. Jokainen yksilöllisesti osoitettava tietosegmentti esitetään TOC-segmentissä olevalla TOC-merkinnällä.

### Tietosegmentti ###

JT-tiedosto määrittää kaikki datasegmentissä tallennetut tiedot. Jotkin datasegmentit voivat pakata kaikki segmentissä jäljellä olevat datatavut. Datasegmenteillä on seuraava rakenne:

!{{HYPERLINKKI1}}

Seuraava taulukko kuvaa erityyppisiä tietosegmenttejä:

|Nimi|Kuvaus
---|---|
|LSG-segmentti|Kattaa kokoelman objekteja, jotka on linkitetty ohjattujen viittausten kautta muodostamaan LSG:n (suunnattu asyklinen graafirakenne)
|Shape LOD -segmentti|sisältää geometristen muotojen määrittelytiedot (esim. kärjet, normaalit, polygonit jne.)
|JT B-Rep -segmentti|Sisältää elementin tiedoille, jotka edustavat yksittäisen osan tarkan geometrisen rajan JT B-Rep -muodossa.
|XT B-Rep -segmentti|Sisältää elementin tiedoille, jotka edustavat yksittäisen osan tarkan geometrisen rajan rajaesitysmuodossa
|Wireframe-segmentti|Tiedot edustavat tarkkaa 3D-langasta kehystä tietylle osalle määritellään tähän segmenttiin sisältyvällä elementillä.
|Metatietosegmentti|Mahdollistaa metatietojen tallentamisen erillisiin osoitettaviin segmentteihin.
|JT ULP -segmentti|Sisältää elementin tiedoille, jotka edustavat yksittäisen osan puolitarkkoja geometrisia rajaa JT ULP -muodossa.
|JT LWPA -segmentti|Sisältää elementin, joka määrittää tietyn osan analyyttiset tiedot. LWPA sulkee analyyttisten pintojen kokoelman osan b-rep määritelmään.

## Pakkaus ##

3D-mallien lähetys- ja tallennusvaatimukset ovat vaativampia, joten JT-tiedostot voivat hyödyntää pakkausta. JT-tietomalli voi koostua erilaisista tiedostoista, jotka käyttävät eri pakkaustekniikkaa, mutta pakkausprosessi on läpinäkyvä JT-datan käyttäjälle.

Toistaiseksi JT Open Toolkit (vakio) ja edistynyt pakkaus ovat kaksi JT-tiedostojen käyttämää pakkaustekniikkaa. JT Open Toolkit käyttää helppoa, häviötöntä pakkausalgoritmia, kun taas edistynyt pakkaus käyttää hienostuneempaa, toimialuekohtaista pakkaustekniikkaa, joka johtaa häviölliseen geometrian pakkaamiseen. Asiakassovellukset suosivat kehittynyttä pakkausta tavallisen pakkauksen sijaan, koska kehittynyt pakkaus tuottaa melko korkeat pakkaussuhteet. Taaksepäin yhteensopivuus tavallisten JT-tiedostojen katselusovellusten kanssa säilyy vakiopakkauksella. Pakkauslomakkeen on oltava yhteensopiva JT-tiedostomuotoversion kanssa, joka näkyy, kun JT-tiedosto avautuu tekstieditorilla ja joka on liitetty ASCII-otsikkotietoihin.

## Viitteet ##

* [JT-tiedostomuodon viite](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)

* [JT (visualisointimuoto)](https://en.wikipedia.org/wiki/JT_(visualization_format)#Data_model)


