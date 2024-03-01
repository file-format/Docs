{
  "date": "2021-03-12",
  "keywords": [
"VP9",
"Tiedosto",
"Laajennus",
"Tiedosto muoto",
"Videon muoto",
"TrueMotion-video",
"VPX",
"On2 Technologies"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "VP9 - TrueMotion-videotiedosto",
  "description": "Opi VP9-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VP9-tiedostoja.",
  "linktitle": "VP9",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-vp-fi9"
}
},
  "lastmod": "2021-03-27"
}

## Mikä on VP9-tiedosto?

Google has developed the VP9 codec as a royalty-free, open-source video coding standard as the successor to VP8. Se oli alun perin suunniteltu pakkaamaan ultra-HD-sisältöä YouTubessa, koska se laajentaa ja parantaa edeltäjänsä koodaustehokkuutta. Jos puhumme alkuperäisistä VPX-koodekeista, ne tulivat On2 Technologiesilta, jonka Google omaksui vuonna 2010. Myöhemmin Google osoitti koodekin avoimen lähdekoodin. Molemmat VP8- ja VP9-muodot ovat saatavilla ilmaisella BSD-lisenssillä, jonka avulla operaattorit voivat järjestää koodauksen tai purkaa taitojaan sekä yksinoikeudessa että avoimen lähdekoodin ohjelmistoissa paljastamatta lähdekoodiaan.

## VP9:n tekniset ominaisuudet

* VP9:n maksimiresoluutio on 8192x4352 jopa 120 fps ja useita väriavaruuksia Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 ja sRGB kanssa
* Tämä muoto tukee täysin kaikkia verkko- ja mobiilikäyttötapauksia alhaisen bittinopeuden pakkauksesta korkealaatuiseen ultra-HD:hen, lisätuella 10/12-bittiselle koodaukselle ja HDR:lle.
* Se voi vähentää videon bittinopeutta jopa 50 % muihin verrattuna
* Se on valmistettu adaptiiviseen suoratoistoon, ja sitä käyttävät YouTube ja muut tunnetut verkkovideopalveluntarjoajat
* Chrome-, Opera-, Edge-, Firefox- ja Android-laitteet sekä miljoonat älytelevisiot tukevat tämän koodekin purkamista
* Yli 1080p:n videoresoluutiota muutetaan VP9:n kautta ja ne mahdollistavat häviöttömän pakkauksen
* Eri väriavaruudet, kuten Rec. 601, Rec. 709, Rec. VP9 tukee 2020, SMPTE-170, SMPTE-240 ja sRGB
* VP9 voi myös tukea HDR-videota, joka käyttää Hybrid Log-Gammaa ja Perceptual Quantizeria


## Lyhyt historia

 *  VP9-videokoodekkien kehitys on aloitettu vuonna 2011, ja sen dekooderi lisättiin Chromium-verkkoselaimeen joulukuussa 2012
 *  Sen ensimmäinen Google Chrome -selainversio julkaistiin helmikuussa 2013 ja julkaisi dekoodauksen tuolloin
 *  Google julkaisi elokuussa 2013 Chrome 29.0.1547 VP9:n lopullisella tuella
 *  Lokakuussa 2013 FFmpegiin lisättiin vaistomainen VP9-dekooderi
 *  Mozilla on lisännyt VP9-apuohjelman Firefoxiin joulukuussa 2013 versioon 2, joka julkaistiin sitten 18. maaliskuuta 2014.
 
## VP9:n toiminta

Yleensä 4K-video parantaa kuvanlaatua pienentämällä tiettyjä pikseleitä, VP9-koodekki ja HEVC tekevät niistä suurempia bittinopeuden ja tiedostokoon pienentämiseksi. Vaikka tämä saattaa tuntua ristiriitaiselta, koodauskone ottaa suuremmat pikselit ja muuttaa ne paremmaksi resoluution tuottavuudeksi. Lähdevideo, joka sisältää videokehyksiä, koodataan tai pakataan pakatuksi videobittivirraksi. Jokainen erillinen kehys jaetaan ensin pikselilohkoihin. Lohkot tutkitaan sitten kolmiulotteisten hylkäysten varalta ja kehysten väliset peräkkäiset yhteydet arvioidaan hyödyntämään alueita, joita ei voida muuttaa. Nämä koodataan liikevektoreilla, jotka varmistavat tietyn lohkon ominaisuudet seuraavassa kehyksessä. Jäännöstiedot koodataan käyttämällä tehokasta binääripakkausta.

## Viitteet

 * [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
 * [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
 * [Coconut](https://www.coconut.co/)

