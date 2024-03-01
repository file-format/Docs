{
  "date": "2019-10-11",
  "keywords": [
"arsc",
".arsc",
"mikä on arsc-tiedosto",
"kuinka avata arsc-tiedosto",
"laajennus",
"tiedosto",
"arsc tiedosto",
"arsc-tiedostomuoto",
"arsc tiedostopääte",
"arsc-tiedosto esimerkki"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARSC - Android-paketin resurssitaulukkotiedosto ",
  "description": "Opi ARSC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ARSC-tiedoston.",
  "linktitle": "ARSC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ars-fic"
}
},
  "lastmod": "2021-06-22"
}

## Mikä on ARSC-tiedosto?

ARSC-tiedosto on Android-resurssitaulukkotiedosto, joka sisältää sovelluksen resurssiluettelon taulukkomuodossa. Tämä sisältää tietoja, kuten resurssien nimet, ominaisuudet ja tunnukset. ARSC-tiedostot ovat osa APK-paketteja, joita käytetään näiden Android-sovellusten asentamiseen. Kaikki resurssit, kuten kuvat, asettelut, tyylit ja merkkijonot, Android-sovelluksessa muunnetaan binääritiedostoiksi, kun APK-tiedosto luodaan. Samalla luodaan myös ARSC-tiedosto, joka sisältää luettelon kaikista ohjelman käännetyistä resursseista ja niiden tunnuksista.

## ARSC-tiedostomuoto

.arsc-tunnistetiedostot ovat binääritiedostoja, jotka luodaan sen jälkeen, kun kääntäjä, kuten ANT (Eclipse) tai Gradle (AS), on kääntänyt Android-sovelluskoodin [APK](/compression/apk/)-tiedoston tuottamiseksi. Voit purkaa APK-tiedoston millä tahansa arkistointityökalulla, kuten WinZipillä, tarkastellaksesi sen sisältöä, joka on käännetty Java-luokkatiedostoja eli classes.dex. Näiden lisäksi se sisältää myös tämän ARSC-tiedoston, joka sisältää metatietoja:

 * XML-solmut
 * Ominaisuudet
 * Resurssitunnukset

Resurssitunnukset viittaavat APK-tiedoston resursseihin, kun taas attribuutit ratkaistaan arvoksi suorituksen aikana. Android aapt -työkalu kerää kaikki tiedostoissa määritetyt resurssit rakennusvaiheessa ja määrittää niille resurssitunnukset. Kun käännetyille resursseille on määritetty tunnisteet, R.java-tiedosto luodaan lähdekoodista sekä resources.arsc-tiedostosta.

## Viitteet

* [Binary Resource Table Structure](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)


