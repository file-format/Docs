{
  "date": "2022-02-16",
  "keywords": [
"obb-tiedosto",
"obb-tiedostomuoto",
"mikä on obb-tiedosto",
"tiedosto",
"obb esimerkki",
"obb tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBB-tiedostomuoto - Android Opaque Binary Blob -tiedosto",
  "description": "Opi OBB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OBB-tiedostoja.",
  "linktitle": "OBB",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ob-fib"
}
},
  "lastmod": "2022-02-16"
}

## Mikä on OBB-tiedosto?

OBB-tiedosto on laajennustiedosto, joka sisältää lisädataa Androidin [APK](/compression/apk/)-tiedoston lisäksi. Google Play Kauppa ei salli Android APK -tiedostoa, jonka koko on yli 100 Mt. Jotkut sovellukset saattavat kuitenkin vaatia teräväpiirtografiikkaa, mediatiedostoja tai muita suuria resursseja isännöimään APK-tiedostojen lisäksi. Siellä OBB-tiedostotyypit tulevat käyttöön. Google Play sallii näiden laajennustiedostojen liittämisen APK-tiedostoon.

## OBB tiedostomuoto

OBB-tiedostot tallennetaan binääritiedostoina APK-tiedostojen mukana. Kun APK on OBB-tiedostojen mukana, Google Play isännöi laajennustiedostoja palvelimellaan, eikä kehittäjältä veloiteta lisäkustannuksia. Nämä lisätiedostot tallennetaan laitteen jaettuun tallennustilaan SD-kortille tai USB-liittimeen asennettavalle osioon, kun sovellus ladataan asennusta varten.

OBB-tiedostot ladataan ja asennetaan latauksen yhteydessä. Mutta joissakin tapauksissa ne ladataan asennusta varten, kun sovellus ajetaan ensimmäisen kerran.

### OBB-tiedoston enimmäiskoko

Google Play Kaupassa voit ladata OBB-laajennustiedostoja, joiden koko on enintään 2 Gt. Suuret tiedostot suositellaan lähetettäväksi pakattujen [ZIP](/compression/zip/)-tiedostojen muodossa tehokkaan latauksen varmistamiseksi Internetin kautta.

Näitä laajennustiedostoja voidaan isännöidä joko **pääasiallisena** ensisijaisena laajennustiedostona sovelluksen tarvitsemia lisäresursseja varten tai valinnaisena korjaustiedoston laajennustiedostona, joka on tarkoitettu päälaajennustiedoston pieniin päivityksiin.

## Viitteet

* [Android-kehittäjät – laajennustiedostot](https://developer.android.com/google/play/expansion-files)


