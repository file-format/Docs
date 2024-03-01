{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDF/UA-tiedostomuoto",
  "description": "Opi PDF/UA-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata PDF/UA-tiedostoja.",
  "linktitle": "PDF/UA",
  "menu": {
    "docs": {
      "parent": "pdf",
      "identifier": "pdf-u-fia"
}
},
  "lastmod": "2019-09-10"
}

# Mikä on PDF/UA-tiedosto? #

PDF/UA julkaistiin nimellä [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) elokuussa 2012, ja se on ylivoimaisesti ensimmäinen täydellinen vaatimusjoukon määritelmä yleisesti saatavilla oleville PDF-dokumenteille. Termi yleisesti saatavilla viittaa ymmärrykseen siitä, että [PDF](/pdf/)-asiakirjan sisältämien tietojen tulee olla yhtäläisesti ja itsenäisesti kaikkien yleisesti saatavilla ja erityisesti vammaisten saatavilla. PDF/UA-standardin käyttöönottoa voidaan pitää tärkeänä askeleena työkalujen ja sovellusten luomisessa PDF-sisällön luomiseen ja lukemiseen.

## Tiedostomuotovaatimukset ##

PDF/UA:n perustana on tiettyjä vaatimuksia, jotka toimivat tämän standardin olemuksena. Pohjimmiltaan nämä perustuvat PDF-tiedostojen merkitsemiseen, mikä tarkoittaa, että kaikki PDF/UA-asiakirjat on merkittävä oikein. Se edellyttää myös, että tunnisteet ovat semanttisesti sopivia ja loogisessa järjestyksessä. Tämä varmistaa, että PDF/UA-spesifikaation avulla luotu loppuasiakirja on luotettavampi ja helppopääsyisempi. Tämä saattaa herättää PDF-kirjoittajien kysymyksen, tarvitseeko heidän tietää kaiken kaikista tällaisista vaatimuksista? Onneksi asia ei ole näin, koska PDF/UA-yhteensopivuustyökalut ottavat vastuun PDF-tiedoston lisäämisestä ja käytettävyyden säilyttämisestä.

PDF/UA:n tiedostomuotovaatimukset ovat seuraavat.

* Sisältö luokitellaan kahdella tavalla: merkityksellinen sisältö ja artefaktit, kuten koristeelliset sivuelementit. Kaikki merkityksellinen sisältö on merkittävä ja integroitava asiakirjan kaikkien tunnisteiden rakennepuuhun. Artefaktit sen sijaan tarvitsee vain merkitä sellaisiksi.

* Merkittävä sisältö tulee merkitä tunnisteilla ja luoda yhdessä muiden dokumentin tunnisteiden kanssa täydellinen rakennepuu.

* Merkittävä sisältö on merkittävä asianmukaisilla semanttisilla tunnisteilla.

* Dokumenttitunnisteiden luoman rakennepuun on vastattava dokumentin loogista lukujärjestystä.

* Vain PDF 1.7:ssä määriteltyjä vakiotunnisteita saa käyttää; Jos käytetään muita tunnisteita, roolimäärityksen merkinnän on kirjattava, mitä vakiotunnistetta kukin edustaa.

* Tietoja ei saa välittää pelkästään visuaalisilla keinoilla (esim. kontrasti, väri tai sijainti sivulla).

* Välkkyvä, vilkkuva tai vilkkuva sisältö ei ole sallittu JavaScriptin ohjaamana tehosteina tai osana PDF-tiedostoon upotettuja videoita.

* Asiakirjan otsikko on annettava ja asiakirja on asetettava niin, että otsikko (eikä tiedostonimi) näkyy ikkunan otsikossa.

* Kaiken sisällön kieli on merkittävä muistiin ja kielenmuutokset on merkittävä sellaisiksi.


## PDF/UA-yhteensopivuus ##

PDF/UA-standardi määrittelee sisällön, lukijoiden ja aputekniikan määritykset. Nämä kolme näkökohtaa linkittyvät toisiinsa asiakirjan sisällön perusteella. Kaikkien näiden vaatimustenmukaisuusvaatimukset ovat alla mainitut.

## Vastaavat tiedostot ##

Files conforming to PDF/UA standard should contain features that are valid as per the [PDF 1.7 specifications](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). However, features that are forbidden by PDF/UA specifically should be excluded.

## Sopivat lukijat ##

Vaatimustenmukaisen lukijan on noudatettava PDF 1.7 -määritysten sääntöjä. Erityisesti sen pitäisi tukea:

* kaikki tunnisteet, attribuutit ja avainarvot, jotka on määritetty saavutettavuutta varten. Sen tulisi myös kyetä käsittelemään ja edustamaan digitaalisia allekirjoituksia, huomautuksia ja valinnaista sisältöä.

* käsittelee ja edustaa digitaalisia allekirjoituksia, huomautuksia ja valinnaista sisältöä

* selata asiakirjaa useilla eri tavoilla


## Yhdenmukainen aputekniikka ##

Yhteensopiva aputekniikka tukee PDF/UA-ominaisuuksia. Näitä ovat esimerkiksi sisällön ja lukijan ominaisuudet, ja niiden pitäisi mahdollistaa navigointi sivujen otsikoiden, asiakirjan rakenteen tai ääriviivan mukaan. Sen pitäisi myös antaa käyttäjän ohittaa navigoinnin oletuszoomaus.

## Viitteet ##

* [PDF/UA – Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)

* [PDF/UA pähkinänkuoressa](https://pdfa.org/pdfua-in-a-nutshell/)


