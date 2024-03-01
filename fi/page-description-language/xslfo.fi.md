{
  "date": "2019-10-11",
  "keywords": [
"XSLFO",
"XSL-muotoiluobjektit",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Laajennettavissa oleva tyylitaulukkokieli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XSLFO",
  "description": "Opi XSLFO-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XSLFO-tiedostoja.",
  "linktitle": "XSLFO",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-xslf-fio"
}
},
  "lastmod": "2021-04-23"
}

## Mikä on XSL-FO-tiedosto? ##

XSL-FO (XSL Formatting Objects) on tehokas tyylitaulukkokieli XML-dokumenttien muotoiluun. Paperin ja printin rajatun muodon semantiikka ilmaistaan XSL-FO:lla, kun mitat ovat kiinteät. Toisin kuin HTML, joka edustaa selainikkunan rajoittamattoman muodon semantiikkaa muuttuvilla mitoilla. XSL-FO:lla muotoiltuja XML-dokumentteja käytetään enimmäkseen PDF-tiedostojen luomiseen. XSL (Extensible Stylesheet Language) on joukko ominaisuuksiltaan täydellisiä W3C-tekniikoita, jotka on tarkoitettu XML-dokumenttien ja tämän kielen XSL-FO-osan muotoiluun ja vaihtamiseen. XSLT ja XPath ovat myös muita XSL:n osia.

Ehdotetaan, että XML-dokumentit muunnetaan ensin XSL-FO:ksi, PDF on esimerkki tästä kriteeristä. PDF:ssä tulokset renderöidään käyttämällä XSLTfirstiä ja sitten XSL-FO-muotoilua. Tällä tavalla XML-dokumentit voidaan muotoilla satunnaisesti. Vaikka XSL-FO hyödyntää CSS (Cascading Style Sheet) -ominaisuuksien käyttöä ja laajentaa niitä aina, kun se on tarpeen todellista muotoa varten, se sisältää sivupohjat, joita kutsutaan sivupohjaksi XSL-FO:n terminologiassa. XSL-FO tarjoaa myös muotoilun melko kehittyneille asiakirjoille ja tukee indeksien luomista.

## Historia ja peruskäsitteet ##

Tammikuussa 2012 XSL-FO:n työluonnos päivitettiin viimeksi ja marraskuussa 2013 sen työryhmä oli suljettu. XSL-tyylitaulukko määrittää XML-dokumenttien luokan esityksen kuvaamalla, kuinka luokan esiintymä muunnetaan muotoilusanastoa käyttäväksi XML-dokumentiksi. XSL-FO on integroitu esityskieli, eikä siinä ole HTML:ssä käytettyjä semanttisia merkintöjä. Lisäksi tämä kieli tallentaa kaikki asiakirjan tiedot itsessään, toisin kuin CSS, joka muuttaa ulkoisen HTML- tai XML-dokumentin oletusasetuksia.

XSL-FO:n käytön yleinen kriteeri on, että käyttäjä kirjoittaa dokumentin XML-kielellä sen sijaan, että kirjoittaisi FO-kielellä. Sen jälkeen tapahtuu XSLT-muunnos. Tämä XSLT-muunnos vastaa XML:n muuntamisesta XSL-FO:ksi. Heti kun XSL-FO-dokumentti on luotu, se luovutetaan sitten FO-prosessoriksi kutsuttuun sovellukseen. FO-prosessorit ovat vastuussa tämän asiakirjan muuttamisesta luettavaksi sekä tulostettavaksi asiakirjaksi. PDF-tiedostot tai PS ovat esimerkkejä XSL-FO:n yleisimmistä tulosteista. Mutta se ei tarkoita, että FO-prosessori voi tuottaa vain nämä kaksi muotoa tulosteena. Jotkut FO-prosessorit voivat tulostaa RTF-tiedostoja tai jopa ikkuna voi ilmestyä käyttäjän graafiseen käyttöliittymään, tämä ikkuna näyttää sivun järjestyksen ja niiden sisällön.

XSL-FO-dokumentti eroaa PDF- tai PS-tiedostosta siinä mielessä, että se ei lopulta määrittele tekstin asettelua eri sivuilla. Ehkä se tyylittelee sivuja ja määrittää sisällön näyttämispaikat. Lisäksi FO-prosessori järjestää tekstin FO-dokumentin määrittämien rajojen sisällä. Tämä spesifikaatio jopa sallii eri FO-prosessorien käyttäytyä tuloksena luotujen sivujen mukaisesti. Esimerkki tällaisesta käyttäytymisestä on tavutus, harvat FO-prosessorit voivat tavuttaa sanoja tilan säästämiseksi rivin katketessa, kun taas jotkut prosessorit eivät valitse tätä vaihtoehtoa. Se riippuu prosessoreista valita erilaisia tavutusalgoritmeja, jotka vastaavat heidän vaatimuksiaan. Nämä tavutusalgoritmit voivat olla hyvin yksinkertaisia tai ehkä monimutkaisempia. Joissakin tilanteissa XSL-FO-spesifikaatio rajoittaa nimenomaisesti FO-prosessoreja, jonkinasteista valintaa asettelun yhteydessä.

Tämä vaihtelu FO-prosessorien välillä tuottaa vaihtelevia tuloksia, joista prosessorit eivät useinkaan välitä. Koska XSL-FO:n pääpaino on sivuttujen/tulostettujen asiakirjojen tuottamisessa. XSL-FO-asiakirjat itsessään toimivat tyypillisesti välittäjinä, joiden päätehtävänä on tuottaa joko PDF-tiedostoja tai tulostettavissa oleva dokumentti jaettavaksi. HTML/CSS:ssä tai XSL-FO:ssa PDF-tiedoston jakaminen lopputuloksena muotoilukielen syöttämisen sijaan osoittaa, että vastaanottimiin ei vaikuta tuloksena oleva monipuolisuus, joka syntyy muotoilukielen tulkkien eroista johtuen. Toisaalta on selvää, ettei ole helppoa tapaa, että asiakirja voi täyttää vastaanottajien erilaiset tarpeet, esim. muuttuva sivukoko tai haluttu fonttikoko tai räätälöinti sivulle tai painolle.

## XSLFO-tiedostomuoto ##

SL-FO-dokumentit ovat pohjimmiltaan XML-dokumentteja, mutta ne eivät noudata mitään skeemaa. Sen sijaan SL-FO-dokumentit noudattavat oman kielensä määrittelyssä määriteltyä syntaksia. Jokaisessa XSL-FO-asiakirjassa vaaditaan kaksi osaa:

1. Osio, joka määrittää luettelon merkittyjä sivuasetteluja.
1. Osio, jossa on kaikki asiakirjan tietojen yksityiskohdat ja merkinnät, joka määrittää sisällön näyttämisen eri sivuilla eri sivuasettelujen kautta.

Sivun ominaisuudet mainitaan sivuasetteluissa, jotka voivat määrittää tekstin organisaation tietyn kielen käytäntöjen mukaiseksi. Lisäksi sivun koko, niiden marginaalit ja sivusarjat (joka määrää eri ominaisuudet parittomille ja parillisille sivuille) määräytyvät myös sivuasetteluissa.

Asiakirjan tieto-osa on jaettu sarjaan vuotoja, joissa jokainen kulku on yhdistetty sivuasetteluun. Virrat sisältävät luettelon lohkoista. Tämä lohkoluettelo voi sisältää upotettuja merkintäominaisuuksia tai luettelon tekstidatasta tai ehkä molempia samanaikaisesti. Asiakirjan marginaalit voivat myös näyttää sivunumerot tai lukujen otsikot. Sekä lohkojen että sisäisten elementtien toiminnallisuus säilyy samoina kuin CSS:ssä, mutta jotkin täyte- ja marginaalisäännöt ovat erilaisia FO:n ja CSS:n välillä.

The page orientation direction is entirely specified for the extension of blocks and inlines, thus making FO documents perform under the languages different from English. The language of the FO specification uses the words start and end rather than left and right for directions description. XSL-FO's basic content markup and cascading rules are taken from CSS. XSL-FO's language agrees to the following specifications.

## Useita sarakkeita ##

Sivulla voi olla useita sarakkeita ja lohkoja, ja se voi ulottua oletuksena sarakkeesta toiseen. Useilla sivuilla saa olla eri leveyksiä ja sarakkeiden lukumäärä. Kaikki FO-ominaisuudet noudattavat monisarakkeisen sivun rajoja.

### Listat ###

XSL-FO-luettelo muodostuu kahdesta lohkosarjasta, jotka on järjestetty posken päähän. Käsitteellisesti luettelossa vasemmalla oleva lohko osoittaa numeron, luettelomerkin tai tekstijonon, kun taas oikeanpuoleinen lohko voi toimia odotetulla tavalla. XSL-FO-luetteloiden numerointi tehdään yleensä XSLT:llä.

### Taulukot ###

FO-taulukko on samanlainen kuin HTML/CSS-taulukko. Käyttäjä voi valita tietorivit, tyylitiedot ja taustavärin jokaiselle yksittäiselle solulle. Käyttämällä erillisiä tyylitietoja käyttäjällä on oikeus valita ensimmäinen rivi taulukon otsikkoriviksi. FO-prosessorille voidaan tiedottaa erikseen kunkin sarakkeen tilamäärityksestä tai sovittaa teksti automaattisesti taulukkoon.

### Indeksointi ###

XSL-FO 1.1:ssä on ominaisuuksia, jotka auttavat luomaan indeksin viittaamalla oikein merkittyihin elementteihin.

### Edut ###

* Soveltuu sisältöpohjaiseen julkaisuun

* Helppokäyttöisyys

* Halpa


## Viitteet ##

* [Mikä on XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)

* [XSL-muotoiluobjektit](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)


