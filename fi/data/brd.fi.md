{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BRD File - EAGLE Circuit Board File - Mikä on .brd -tiedosto ja kuinka avata se?",
  "description" : "Lisätietoja BRD EAGLE Circuit Board File -tiedostosta ja sen avaamisesta.",
  "linktitle" : "BRD",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-brd-fi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Mikä on BRD-tiedosto?

BRD-tiedostomuotoa käytetään elektronisen suunnittelun automaation (EDA) ohjelmistossa painetun piirilevyn (PCB) suunnittelussa. PCB-suunnitteluohjelmistot, kuten Eagle, KiCad, Altium Designer ja muut, käyttävät tätä tiedostomuotoa painetun piirilevyn asettelun, liitäntöjen ja muiden suunnitteluun liittyvien tietojen tallentamiseen.

BRD-tiedosto on CAD-tiedostotyyppi, joka on digitaalisia tiedostoja, joita insinöörit ja suunnittelijat käyttävät suunnittelun luomiseen, muokkaamiseen ja analysointiin. BRD-tiedosto liittyy Autodesk EAGLE:hen, joka on elektroniikkateollisuudessa yleisesti käytetty ohjelmistosovellus painettujen piirilevyjen (PCB) suunnitteluun. Autodesk EAGLE tarjoaa työkaluja sekä kaavamaiseen sieppaamiseen (piirin visuaalisen esityksen luomiseen) että piirilevyasetteluun (komponenttien järjestämiseen ja yhteyksien reitittämiseen).

BRD-tiedosto luodaan EAGLE Layout Editorilla, joka on osa Autodesk EAGLE -ohjelmistopakettia. Tämän editorin avulla käyttäjät voivat suunnitella piirilevyn asettelua, mukaan lukien komponenttien sijoittamisen, reititysjäljet, suunnittelusääntöjen määrittelyn ja valmistusta varten tarvittavien tiedostojen luomisen.

BRD-tiedostot toimivat malleina tai suunnitelmina elektronisten piirien suunnittelussa PCB:lle. Suunnittelijat käyttävät EAGLE- ja .brd-tiedostoja kääntääkseen kaaviokuvansa fyysisiksi asetteluiksi, jotka voidaan valmistaa.

.BRD-tiedostot voidaan tallentaa Gerber-poratietomuodossa. Gerber-tiedostot ovat vakiomuotoja, joita käytetään piirilevyjen valmistuksessa kuvaamaan kuvioita, kerroksia ja piirilevysuunnittelun ominaisuuksia. .brd-tiedostojen tallentaminen tähän muotoon mahdollistaa niiden käytön tietokoneavusteisissa valmistusohjelmissa (CAM), jotka luovat PCB:n valmistukseen tarvittavia ohjeita.

## BRD-tiedostojen katseluohjelma

.brd-tiedostojen katseluun on saatavilla useita ohjelmistotyökaluja, joiden avulla käyttäjät voivat visualisoida ja tarkastaa Autodesk EAGLEn kaltaisilla ohjelmistoilla luotuja PCB-asetteluja.

1.  **Autodesk EAGLE**: Jos sinulla on Autodesk EAGLEn käyttöoikeus, voit yksinkertaisesti avata .brd-tiedostoja suoraan ohjelmistosta katselu- ja muokkaustarkoituksiin.
    
2.  **KiCad**: KiCad on avoimen lähdekoodin EDA-ohjelmistopaketti, joka sisältää PCB-asettelueditorin. Sillä on mahdollisuus tuoda ja tarkastella Autodesk EAGLElla luotuja .brd-tiedostoja.
    
3.  **ViewPlot**: ViewPlot on erillinen Gerber-katseluohjelma, joka tukee useita PCB-tiedostomuotoja, mukaan lukien .brd. Sen avulla käyttäjät voivat tarkastella piirilevymalleja ilman alkuperäistä suunnitteluohjelmistoa.
    
4.  **GC-Prevue**: GC-Prevue on toinen suosittu Gerber-katseluohjelma, joka pystyy käsittelemään myös .brd-tiedostoja. Se tarjoaa ominaisuuksia piirilevyasettelujen visualisointiin, etäisyyksien mittaamiseen ja suunnittelun yksityiskohtien tarkastamiseen.
    
5.  **Gerbv**: Gerbv on avoimen lähdekoodin Gerber-katseluohjelma, joka tukee Gerber-tiedostojen katselua, jotka voivat sisältää Gerber-muotoon tallennettuja .brd-tiedostoja.
    
6.  **Online-katselutyökalut**: Saatavilla on myös online-työkaluja, joiden avulla voit ladata ja tarkastella .brd-tiedostoja suoraan selaimessasi. Yksi tällainen esimerkki on EasyEDAn Online Gerber Viewer, joka tukee eri PCB-tiedostomuotojen katselua, mukaan lukien Gerber ja .brd.

## Kuinka avata BRD -tiedosto?

Piirilevysuunnittelussa käytettäviä BRD-tiedostoja voidaan avata erilaisissa piirilevysuunnittelusovelluksissa.

- **Autodesk EAGLE**: Tämä on Autodeskin kehittämä monikäyttöinen piirilevysuunnitteluohjelmisto. Se tukee kaavioiden luomista, piirilevyasetteluja ja sähköliitäntöjen reititystä. Käyttäjät voivat avata .brd-tiedostoja suoraan Autodesk EAGLEssa katselua ja lisämuokkausta varten.
    
- **Altium Designer**: Altium Designer on kattava piirilevysuunnitteluohjelmisto ensisijaisesti Windows-käyttöjärjestelmille. Se tarjoaa laajan valikoiman ominaisuuksia kaavamaiseen sieppaukseen, piirilevyasetteluun ja suunnitteluanalyysiin. Altium Designer tukee myös .brd-tiedostojen avaamista, jolloin käyttäjät voivat tuoda muilla ohjelmistoilla luotuja malleja ja käsitellä niitä.
    
- **Open Board Viewer**: Open Board Viewer on PCB-katseluohjelmisto, joka on suunniteltu erityisesti Linux-käyttöjärjestelmille. Se on avoimen lähdekoodin työkalu, jonka avulla käyttäjät voivat visualisoida piirilevyasetteluja, tarkastaa komponentteja ja tarkastella reititystietoja. Open Board Viewer tukee .brd-tiedostojen avaamista, jolloin Linux-käyttöympäristöjen käyttäjät voivat tarkastella ja analysoida muilla ohjelmistoilla luotuja malleja.

Tässä on luettelo ohjelmista, joilla voit avata BRD tiedostoja.

- **Autodesk EAGLE** (ilmainen kokeiluversio) (Windows, Mac, Linux)
- **Altium Designer** (ilmainen kokeiluversio) (Windows, Mac, Linux)
- **Avaa Board Viewer** (ilmainen) Linuxille

## Viitteet
* [EAGLE-ohjelma](https://en.wikipedia.org/wiki/EAGLE_(ohjelma))


