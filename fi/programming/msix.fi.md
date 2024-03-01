{
  "date": "2021-04-22",
  "keywords": [
"msix-tiedosto",
"laajennus",
"muoto",
"kuinka avata msix-tiedosto",
"msix-tiedostomuoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX - Mikä on MSIX-tiedosto?",
  "description": "Opi MSIX-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata MSIX-tiedostoja.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-fix"
}
},
  "lastmod": "2021-12-16"
}

## Mikä on MSIX-tiedosto?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. Tämä on nykyaikainen pakettitiedostomuoto verrattuna {{HYPERLINKKI1}}- ja MSI-tiedostomuotoihin, jotka lopulta luovutaan uuteen tiedostomuotoon. Sitä voidaan käyttää Win32-, WPF- ja Windows Forms -sovellusten käyttöönotossa. MSIX-tiedostot ovat luotettavia, ja ne tähtäävät verkon ja levytilan optimointiin. Kehittäjät käyttävät näitä ohjelmien jakamiseen loppukäyttäjille Microsoft Storen (aiemmin nimellä Windows Store) kautta.

## MSIX-tiedostomuoto - lisätietoja

MSIX-tiedostot on [ZIP](/compression/zip/)-pakattu, ja kaikki tiedostot sisältyvät pakattuun tiedostoon. Sovelluksiin liittyvien tiedostojen lisäksi MSIX-tiedosto sisältää [.xml](/web/xml/) määritystiedostoa, jotka sisältävät sovelluksen asennukseen liittyviä tietoja.

## Mitä MSIX-paketissa on?

MSIX-paketti koostuu seuraavista tiedostoista.

 * `AppxBlockMap.xml` – Pakettilohkokarttatiedostona tunnettu XML-dokumentti sisältää luettelon sovelluksen tiedostoista indekseillä ja salaustiivisteillä jokaiselle pakettiin tallennetulle tietolohkolle.
 * AppxManifest.xml – XML-dokumentti, joka sisältää MSIX-sovelluksen käyttöönottoon, näyttämiseen ja päivittämiseen tarvittavat tiedot. Nämä tiedot sisältävät paketin identiteetin, paketin riippuvuudet, vaaditut ominaisuudet, visuaaliset elementit ja laajennettavuuskohdat.
 * AppxSignature.p7x - Tiedosto, joka luodaan, kun paketti allekirjoitetaan. Kaikki MSIX-paketit on allekirjoitettava ennen asennusta. AppxBlockmap.xml:n avulla alusta voi asentaa paketin ja olla validoitu.

## Viitteet

 * [MSIX Overview](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Luo APPX-tiedostoja Microsoft Visual Studiolla](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

