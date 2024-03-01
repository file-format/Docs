{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/X-tiedostomuoto",
  "description": "Opi PDF/X-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata PDF/X-tiedostoja.",
  "linktitle": "PDF/X",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf--fix"
}
},
  "lastmod": "2019-09-10"
}

# Mikä on PDF/X-tiedosto? #

PDF/X on ISO 15930 -standardi, joka julkaistiin vuonna 2001, ja siinä on osa PDF-toimintoja. Standardi laadittiin ja julkaistiin paino- ja kustannusteollisuuden erityisvaatimusten perusteella. Tämän standardin vaatimukset on kaikki laadittu paino- ja kustannusteollisuuden erilaisten tarpeiden mukaan. PDF/X edellyttää vaatimusten mukaisten tiedostojen olevan täydellisiä eli itsenäisiä. Tämä edellyttää, että sivulla käytettyjen elementtien, kuten fonttien, tulee olla osa asiakirjaa. Sisältö, kuten 3D tai video, ei voi olla osa PDF/X-dokumenttia. PDF/X-dokumentin sisältämien tietojen on oltava tarkkoja.

## PDF/X-standardit ja -versiot ##

PDF/X-standardiperhe koostuu useista versioista, joista jokainen on suunniteltu erikoistulokseen. Näiden standardien kehittämisellä pyrittiin vastaamaan paino- ja kustannusteollisuuden moniin erilaisiin tarpeisiin.

* `PDF/X-1a` - Tunnetaan myös PDF/X-perheen ensimmäisenä standardina. PDF/X-1a edellyttää, että kaikki sisältö on osa PDF-dokumenttia, jotta se voidaan tulostaa. Asiakirjan elementit, kuten kirjasimet, lomakkeet, salasanasuojaus ja näkyvät huomautukset, eivät ole sallittuja. PDF/X-1a:lla on omat erityisvaatimukset, kuten myös läpinäkyvyyttä ja tasoja koskevat vaatimukset ovat sallittuja. Ne edellyttävät myös, että tulostuselementit käyttävät vain CMYK-, harmaasävy- tai spottivärejä, jolloin RGB- tai laiteriippumattomia väriavaruuksia ei käytetä. on tarkoitettu vaihtoon, jossa kaikki tiedostot on toimitettava CMYK-väreissä (ja/tai spottiväreissä) ilman RGB- tai värihallittua dataa. PDF/X-1a:sta käytetään myös nimitystä Complete Exchange, koska sen edellyttämät tiedot ovat täydellisiä

* `PDF/X-3` - otettiin käyttöön vuonna 2002 ja poisti monet PDF/X-1a:n rajoitukset. Tämä mahdollisti grafiikan PDF/X-3:ssa käyttämään CMYK-, grescale-, RGB-, Lab- ja ICC-pohjaisia väriavaruuksia. Se perustuu itse asiassa PDF-standardeihin 1.3 ja [ICC-profiili](https://en.wikipedia.org/wiki/ICC_Profile). Sitä kutsutaan myös värinhallintaksi sen joustavuuden ja sääntöjen vuoksi, jotka liittyvät PDF-dokumenttiin sisältyviin väreihin.

* `PDF/X-4` - tukee piirtoheitinkalvoja, joten PDF-X/4 sisältää kaikki tiedot, joita tarvitaan tulostukseen ilman litistystä.

* `PDF/X-5` - perustuu PDF/X-4:ään, ja se lisää tuen ulkoiselle grafiikalle viite-XObject-objektien kautta sekä ulkoisia n-väriprofiileja renderöintitarkoituksessa. Käytä sitä osittaiseen tulostustietojen vaihtoon PDF-versiolla 1.6


## Viitteet ##

* [PDF/X - Wikipedia](https://en.wikipedia.org/wiki/PDF/X)


