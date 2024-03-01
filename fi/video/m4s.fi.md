{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4S-tiedosto - Mikä on M4S-tiedosto?",
  "description": "Opi M4S-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata M4S-tiedostoja.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-fis"
}
},
  "lastmod": "2022-07-18"
}

## Mikä on M4S-tiedosto?

M4S-tiedosto on pieni osa videosta, joka suoratoistetaan Internetissä **MPEG-DASH** -suoratoistotekniikalla. Se sisältää videosegmentin binääritietojen muodossa. Vastaanottava sovellus (yleensä verkkoselain tai mediasoittimet) toistaa nämä segmentit saapumisjärjestyksessä. Ensimmäinen M4S-segmentti tunnistetaan sen sisältämien alustustietojen perusteella. **yhteenveto**: M4S-tiedostot ovat pieniä yksittäisiä mediasegmenttejä kokonaisesta tiedostosta.

## M4S tiedostomuoto

M4S-tiedostot perustuvat {{HYPERLINKKI}}. Nämä suuren tiedoston pienet osat voidaan ladata itsenäisesti HTTP:n kautta. Jos sinulla on siis suuri [MP4](/video/mp4/)-elokuvatiedosto, se voidaan suoratoistaa MPEG-DASH-tekniikalla (Dynamic Adaptive Streaming over HTTP) segmentoimalla se M4S-segmenttitiedostoiksi. Jos tämä suuri elokuvatiedosto ladataan levylle M4S-muodossa, useita M4S-tiedostoja ladataan. Jos kaikki nämä .m4s-segmentit ketjutetaan, syntyy täydellinen toistettava tiedosto. Mediasoittimet eivät voi toistaa tiedostoa, ellei ensimmäinen alustussegmentti ole myös saatavilla tiedoston kanssa.

## Tietoja MPEG-DASH-suoratoistosta

MPEG-DASH käyttää mukautuvaa bittinopeusvirtaustekniikkaa, joka mahdollistaa korkealaatuisen mediasisällön suoratoiston Internetin kautta. Tämä tehdään jakamalla sisältö pieniin segmentteihin, jotka suoratoistetaan HTTP:n kautta. Suuret mediatiedostot, kuten elokuvat, podcastit tai urheilutapahtuman suorat lähetykset, voidaan suoratoistaa tällä tavalla. Nämä segmentit koodataan eri bittinopeuksilla. MPEG-DASH-yhteensopivat mediasoittimet valitsevat automaattisesti segmentin, jolla on suurin bittinopeus bittinopeuden sovitusalgoritmin avulla. Tämä välttää tapahtumien pysähtymisen tai uudelleenpuskuroinnin toistossa.

### Open-Source API M4S-tiedostoille

Saatavilla on avoimen lähdekoodin sovellusliittymiä, joita voidaan käyttää M4S-tiedostojen lukemiseen ja muuntamiseen.

 * [libdash](https://github.com/bitmovin/libdash) – .NET-sovellusliittymä M4S-tiedostoille
 * [dash.js](https://github.com/Dash-Industry-Forum/dash.js) – Javascript-asiakasohjelma M4S-tiedostolle
 * [Go Library for Create Dash Files](https://github.com/zencoder/go-dash)

### Avoimen lähdekoodin sovellusliittymä M4S:n muuntamiseksi MP4:ksi

 * [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Viitteet ###

* [ISO Base Media File (ISOBMFF) -muoto](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)

* [Dynaaminen mukautuva suoratoisto HTTP:n kautta - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


