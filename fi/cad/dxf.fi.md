{
  "date": "2020-03-16",
  "keywords": [
"DXF tiedosto",
"Tiedosto muoto",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi DXF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DXF-tiedostoja.",
  "title": "DXF tiedostomuoto",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dx-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DXF-tiedosto?

DXF, Drawing Interchange Format tai Drawing Exchange Format, on merkitty tietoesitys AutoCAD-piirustustiedostosta. Jokaisella tiedoston elementillä on etuliite kokonaisluku, jota kutsutaan ryhmäkoodiksi. Tämä ryhmäkoodi edustaa itse asiassa seuraavaa elementtiä ja osoittaa tietoelementin merkityksen tietylle objektityypille. DXF mahdollistaa lähes kaikkien käyttäjän määrittämien tietojen esittämisen piirustustiedostossa.

Autodesk on kehittänyt DXF-tiedostomuodon CAD-tietotiedostomuodoksi tietojen yhteentoimivuutta varten AutoCADin ja muiden sovellusten välillä. Siten tietoja voidaan tuoda muista muodoista DXF:ään AutoCADiin DXF-tiedostomuotojen yhteentoimivuusmääritelmien mukaisesti.

## Lyhyt historia ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. AutoCADin alkuperäiset versiot tukevat vain DXF:n ASCII-tiedostomuotoa. AutoCADin (ja uudempi) julkaisun 10. julkaisun myötä vuonna 1988 AutoCADissa otettiin käyttöön tuki sekä ASCII- että binääriselle DXF-tiedostomuodolle. Aiemmissa vaiheissa Autodesk ei jakanut tiedostomuotomäärityksiä, joten DXF-tiedostojen oikea tuonti ei ollut helppoa. Autodesk julkaisee kuitenkin nyt DXF-spesifikaatiot suuren yleisön saataville.

## Tiedostomuodon tiedot ##

DXF-tiedostomuoto käyttää ryhmäkoodi- ja arvopareja sisällön järjestämiseen osioihin. Jokainen osa koostuu tietueista, joissa jokainen tietue koostuu ryhmäkoodista ja tietoelementistä. Jokainen ryhmäkoodi ja arvo ovat omalla rivillään DXF-tiedostossa. Jokainen osa alkaa ryhmäkoodilla 0, jota seuraa merkkijono SECTION. Tätä seuraa ryhmäkoodi 2 ja merkkijono, joka ilmaisee osion nimen (esimerkiksi SECTION1). Jokainen osa koostuu ryhmäkoodeista ja arvoista, jotka määrittelevät sen elementit. Osio päättyy nollaan, jota seuraa merkkijono ENDSEC.

DXF-tiedostomuoto huomioi objektit, jotka ovat erilaisia kuin entiteetit. Objekteilla ei ole tässä graafista esitystä, mutta entiteeteillä on se. Siten DXF:n merkintöjä kutsutaan graafisiksi objekteiksi, kun taas objektiobjekteja kutsutaan ei-graafisiksi objekteiksi. DXF-tiedoston BLOCK- ja ENTITIES-osat sisältävät entiteettejä ja ryhmäkoodien käyttö näissä kahdessa osiossa on identtinen. Entiteetin loppua ilmaisee seuraava 0-ryhmä, joka aloittaa seuraavan entiteetin tai osoittaa osion loppua.

### Tiedostorakenne ###

DXF-tiedoston osiot on järjestetty seuraavassa järjestyksessä:

|Section|Basic description
---|---|
|Otsikko|Tämä osio sisältää yleistä tietoa piirroksesta. Se on kuin puhelimen Asetukset-toiminto, joka sisältää piirustukseen liittyvät erilaiset muuttujat ja siihen liittyvät arvot. Esimerkiksi Otsikko-osio määrittää, mitä AutoCAD-versiota DXF-tiedosto käyttää (muuttuja $ACADVER) tai yksikön, jota käytetään tiedoston kulmien mittaamiseen (muuttuja $AUNITS).
|Luokat|LUOKAT-osiossa on tiedot sovelluskohtaisista luokista, joiden esiintymät näkyvät tietokannan LOHKOT-, ENTITIES- ja OBJEKTI-osissa.
|Tables|Tämä osio sisältää määritelmiä useille eri taulukoille, joista jokainen sisältää useita eri symbolimerkintöjä. Esimerkiksi taulukko [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) (LTYPE) määrittää DXF-tiedoston viivojen, pisteiden, tekstin ja symbolien kuvion ja niiden skaalauksen. Tässä on täydellinen luettelo tästä osiosta löytyvistä taulukoista:<ul><li> Sovellustunnus (APPID) -taulukko</li><li> Block Record (BLOCK_RECORD) -taulukko</li><li> Dimension Style (DIMSTYPE) -taulukko</li><li> Layer (LAYER) -taulukko</li><li> Linetype (LTYPE) -taulukko</li><li> Tekstityyli (STYLE) -taulukko</li><li> User Coordinate System (UCS) -taulukko</li><li> Näytä (VIEW) taulukko</li><li> Viewport-määritystaulukko (VPORT).</li></ul>
|Blocks|Tämä osio sisältää graafiset objektit ja piirustuskokonaisuudet, jotka muodostavat kunkin piirustuksen lohkoviittauksen.
|Entiteetit|Tämä osio sisältää piirustuksen todelliset objektitiedot ja graafiset kokonaisuudet. Tämä voi sisältää raakadataa – esimerkiksi ympyräkokonaisuuden määrittää sen paksuus, keskipiste, säde ja pursotussuunta.
|Objektit|Täältä löydät piirustuksen ei-graafiset osat. Esimerkiksi AutoCAD-sanakirjat on tallennettu tähän.

## Viitteet ##

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [AutoCAD DXF by Wikipedia](https://en.wikipedia.org/wiki/AutoCAD_DXF)


