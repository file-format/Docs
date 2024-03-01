{
  "date": "2021-01-21",
  "keywords": [
"ai tiedosto",
"ai-tiedostomuoto",
"mikä on ai-tiedosto",
"tiedosto",
"ai esimerkki",
"ai tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "AI - Adobe Illustratorin kuvitustiedosto",
  "description": "Opi AI-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata tekoälytiedostoja.",
  "linktitle": "AI",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-a-fii"
}
},
  "lastmod": "2021-01-21"
}

## Mikä on AI-tiedosto?

A file with an .ai extension is an Adobe Illustrator Artwork file that contains vector graphics in a single page. it uses points to create paths for displaying the image data, thus making it safe from losing image quality if it is enlarged. AI file format is base don the PGF file format which are similar to AI files. AI format finds its major usage for logos and print media, and its initial versions were considered similar to that of [EPS](/page-description-language/eps/) files. AI files can be opened with Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro, and CorelDraw Graphics tools.

## AI tiedostomuoto

Tekoäly on Adobe Illustratorin oma tiedostomuoto, ja se käyttää PGF:n kaltaista kaksoispolkua EPS-yhteensopivien tiedostojen tallentamiseen. [Adobe Illustrator File Format specifications](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) tarjoaa yksityiskohtaisen kehittäjän viitteen tämän tiedostomuodon sisäisistä tiedoista. Kaikki Adobe Illustratorin luomat asiakirjat (tiedostot) ovat PostScript-kielisiä asiakirjoja, ja niissä on kaksi pääosaa, jotka noudattavat asiakirjan strukturointikäytäntöjä: prolog ja skripti.

### Prolog

Prolog-osio sisältää tiedoston tulkitsemiseen tarvittavat tiedot. Esimerkki olisi rajauslaatikko, joka sisältää kaikki sivulla olevat merkit. Se sisältää myös resurssitietoja, kuten kirjasimia ja toimintomääritelmiä. Nämä resurssit on loogisesti ryhmitelty sarjoiksi, joita kutsutaan procsetiksi, ja ne sisältävät eksplisiittisiä menetelmiä proseduurien alustamiseksi ja lopettamiseksi.

### Käsikirjoitus

Sivun graafiset elementit kuvataan käsikirjoituksella. Skripti sisältää viittauksia prologin operaattoreihin ja proseduureihin sekä operandit ja tiedot. Skriptin kolme loogista osaa sisältävät:

 * Setup Sequence - joka alustaa ja aktivoi prologissa määritellyt resurssit
 * Kuvaavien operaattoreiden sekvenssi
 * Traileri, joka poistaa resurssit käytöstä

Skriptin operaattorit ovat graafisten elementtien sarjoja, jotka on kirjoitettu prologin procsettien määrittelemällä kielellä. Nämä sekvenssit koostuvat tietoelementtien kokoelmista, graafisista attribuuttien määritelmistä ja prosessisarjoissa määriteltyjen proseduurien kutsuista.

### Objektitunnisteet

Objektitunnisteita käytetään mukautetun tiedon liittämiseen Adobe Illustrator -taideobjektiin. Tunnisteet koostuvat seuraavista:

 * Tunnisteen tunniste
 * Tunnisteen tyyppi
 * Data

## Viitteet
* [Adobe Illustrator -tiedostomuodon tekniset tiedot](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)

* [PaintShopPron AI-tiedostomuoto](https://www.paintshoppro.com/en/pages/ai-file/)


