{
  "date": "2021-04-22",
  "keywords": [
"appxbundle-tiedosto",
"laajennus",
"muoto",
"kuinka avata appxbundle-tiedosto",
"appxbundle-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "appxbundle - Mikä on APPXBundle-tiedosto?",
  "description": "Opi APPX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata APPX-tiedostoja.",
  "linktitle": "APPXBUNDLE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-appxbundl-fie"
}
},
  "lastmod": "2021-12-19"
}

## Mikä on APPXBUNDLE-tiedosto?

APPXBUNDLE-tiedosto on pakettitiedosto, joka on luotu sovelluksella [Microsoft Visual Studio](https://visualstudio.microsoft.com/), ja sitä käytetään Windows-sovellusten (sekä työpöytä- että UWP) jakeluun sivustolla [Microsoft Store](https://apps.microsoft.com/store/apps). Se sisältää yhden tai useamman sovelluksen version, joka on kohdistettu tiettyyn suoritinarkkitehtuuriin, kuten x86, x64 tai ARM. Näin loppukäyttäjä voi vastaanottaa ja ottaa käyttöön sopivan version sovelluksesta tietokonearkkitehtuuriin perustuen. APPXBUNDLE-tiedostot on ryhmitelty vakiomuotoisella [ZIP](/compression/zip/)-tiedostomuodolla. Microsoft Visual Studion Publish-menetelmää käytetään sovellusten julkaisemiseen pakettina. Yhden paketin sovellukset jaetaan [APPX](/programming/appx/)-tiedostoina.

## APPXBUNDLE-tiedostomuoto

APPXBUNDLE-tiedostot julkaistaan ZIP-tiedostomuodossa. Jos haluat nähdä sovelluspaketin sisällön, voit purkaa sen sisällön purkuapuohjelmilla, kuten [WinZIP](https://www.winzip.com/en/) tai WinRAR.

## Viitteet

 * [Dependency packages for .appx and .appxbundle packages](https://www.ibm.com/docs/en/maas360?topic=catalog-dependency-packages-appx-appxbundle-packages)
 * [Luo APPX-tiedostoja Microsoft Visual Studiolla](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

