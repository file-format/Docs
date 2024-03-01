{
  "date": "2023-06-08",
  "keywords": [
"crx tiedosto",
"mikä on crx-tiedosto",
"kuinka asentaa crx-tiedosto google chromeen",
"kuinka avata crx-tiedosto",
"mitä crx-tiedosto sisältää",
"mikä on crx-tiedoston muoto",
"tiedosto",
"crx tiedostopääte",
"laajennus"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CRX-tiedostomuoto - Google Chrome -laajennus",
  "description": "Opi CRX-muodosta ja sovellusliittymistä, jotka voivat luoda ja avata CRX-tiedostoja.",
  "linktitle": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx-fi",
      "parent": "misc"
}
},
  "lastmod": "2023-06-08"
}

## Mikä on CRX-tiedosto?

CRX-tiedostomuoto on liitetty Google Chrome -selainlaajennuksiin. CRX-tiedosto on pohjimmiltaan pakattu paketti, joka sisältää tarvittavat tiedostot ja metatiedot laajennuksen asentamista ja käyttöä varten Google Chromessa. Se parantaa verkkoselaimen toimivuutta tai ulkonäköä tarjoamalla lisäominaisuuden tai teeman.

Kun CRX-tiedosto ladataan ja asennetaan Google Chromeen, selain varmistaa laajennuksen eheyden käyttämällä julkista avainta ja allekirjoitusta. Jos vahvistus onnistuu, Chrome purkaa CRX-tiedoston sisällön ja asentaa laajennuksen, jolloin se on käytettävissä. Käyttäjät voivat hallita laajennuksiaan Chrome-laajennukset-sivun kautta, jolla voidaan ottaa käyttöön, poistaa käytöstä tai poistaa asennettuja laajennuksia.

## Kuinka asentaa CRX-tiedosto Google Chromeen?

Voit asentaa CRX-tiedoston Google Chromeen seuraavasti:

1. Avaa Chrome-selain.
2. Kirjoita osoitepalkkiin chrome://extensions ja paina Enter.
3. Ota käyttöön Kehittäjätilan vaihtokytkin, joka sijaitsee Laajennukset-sivun oikeassa yläkulmassa.
4. Napsauta Lataa pakattu -painiketta.
5. Etsi ja valitse kansio, joka sisältää puretun CRX-tiedoston sisällön (tai valitse yksinkertaisesti itse CRX-tiedosto).
6. Napsauta Avaa asentaaksesi laajennuksen.

## Mitä CRX-tiedosto sisältää?

CRX-tiedosto sisältää tarvittavat tiedostot ja metatiedot, joita tarvitaan Google Chrome -laajennukseen. Tässä on erittely tyypillisestä CRX-tiedoston sisällöstä:

- **Manifest file (manifest.json):** This file is a JSON-formatted file that includes information about extension such as its name, version, description, permissions and background scripts. It defines the structure and behavior of extension.
- **JavaScript-tiedostot:** Nämä tiedostot sisältävät koodin, joka määrittää laajennuksen toiminnallisuuden. Ne voivat sisältää komentosarjoja tapahtumien käsittelyyn, verkkosivujen muokkaamiseen tai vuorovaikutukseen Chromen sovellusliittymien kanssa.
- **HTML-, CSS- ja kuvatiedostot:** Laajennukset sisältävät usein käyttöliittymäelementtejä, kuten ponnahdusikkunoita tai asetussivuja. HTML-tiedostot määrittävät näiden rajapintojen rakenteen, kun taas CSS-tiedostot hallitsevat niiden ulkonäköä. Kuvatiedostoja käytetään kuvakkeisiin tai muihin graafisiin resursseihin.
- **Valinnaiset resurssitiedostot:** Laajennukset voivat sisältää lisäresursseja, kuten lokalisointitiedostoja useiden kielten tukemiseksi. Nämä tiedostot sisältävät käännöksiä laajennuksen käyttöliittymässä käytetystä tekstistä.
- **Taustaskriptit:** Jos laajennuksessa on taustaprosesseja tai komentosarjoja, jotka toimivat aktiivisesta verkkosivusta riippumatta, nämä komentosarjat sisällytetään CRX-tiedostoon.
- **Sisältöskriptit:** Sisältöskriptit ovat skriptejä, jotka voidaan lisätä verkkosivuille niiden käyttäytymisen muokkaamiseksi tai vuorovaikutuksessa niiden sisällön kanssa. Jos laajennus käyttää sisältöskriptejä, tarvittavat tiedostot kyseisille skripteille ovat CRX-tiedostossa.
- **Muu sisältö:** Tietyistä laajennusvaatimuksista riippuen voidaan sisällyttää lisätiedostoja, kuten ääni- tai videotiedostoja, fontteja tai datatiedostoja.

CRX-tiedostomuoto on pohjimmiltaan pakattu paketti, joka sisältää kaikki nämä tiedostot ja kansiot jäsennellyllä tavalla. Kun CRX-tiedosto asennetaan Google Chromeen, selain purkaa sisällön ja sijoittaa ne sopiviin paikkoihin, jolloin laajennus voidaan ladata ja suorittaa selaimessa.

## Mikä on CRX-tiedoston muoto?

CRX-tiedostomuoto on erityinen muoto Google Chrome -laajennusten pakkaamiseen ja jakeluun. Se on pohjimmiltaan pakattu ZIP-arkisto eri tiedostotunnisteilla. CRX-tiedoston perusrakenne on seuraava:

- **Tiedoston allekirjoitus:** Tiedoston ensimmäiset 4 tavua sisältävät maagisen numeron Cr24 (heksadesimaali: 43 72 32 34), joka toimii allekirjoituksena tiedoston tunnistamiseksi CRX-tiedostoksi.
- **Versionumero:** Seuraavat 4 tavua edustavat CRX-muodon versionumeroa.
- **Julkisen avaimen pituus:** Seuraavat 4 tavua osoittavat laajennuksen allekirjoituksen tarkistamiseen käytetyn koodatun julkisen avaimen pituuden.
- **Allekirjoituksen pituus:** Seuraavat 4 tavua määrittävät laajennuksen allekirjoituksen pituuden.
- **Julkinen avain:** Tämä osio sisältää koodatun julkisen avaimen, jota käytetään laajennuksen eheyden tarkistamiseen.
- **Allekirjoitus:** Tämä osio sisältää laajennuksen allekirjoituksen, joka luodaan allekirjoittamalla laajennuksen sisältö yllä mainittua julkista avainta vastaavalla yksityisellä avaimella.
- **ZIP-arkisto:** CRX-tiedoston loput tavut sisältävät pakatun ZIP-arkiston. Tämä arkisto sisältää kaikki tarvittavat tiedostot ja kansiot laajennuksilla, mukaan lukien luettelotiedostot, JavaScript-tiedostot, HTML-tiedostot, CSS-tiedostot, kuvat ja kaikki muut resurssit.

## Viitteet
* [CRX-muodon erittely](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)


