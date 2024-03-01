{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH2-tiedosto - iOS SHSH Blob -tiedostomuoto",
  "description":"Lisätietoja siitä, mikä on SHSH2-tiedosto.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2-fi",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Mikä on SHSH2-tiedosto?

SHSH2-tiedosto, joka tunnetaan myös nimellä SHSH blob tai ECID SHSH, on digitaalinen allekirjoitus, jota Apple käyttää iOS-laitteiden, kuten iPhonen, iPadin ja iPodin laiteohjelmistopäivitysten todentamiseen ja tarkistamiseen. Se sisältää laitteelle yksilöllisen tunnisteen, joka tunnetaan nimellä ECID (Exclusive Chip ID). Se sisältää myös tietoja laitteeseen asennetusta laiteohjelmistoversiosta.

## SHSH2-tiedostomuoto – lisätietoja

SHSH2-tiedostot tallennetaan levylle binääritiedostomuodossa, ja tämän tiedostomuodon sisäiset tiedostorakenteen tiedot eivät ole saatavilla julkisesti.

Kun uusi iOS-versio asennetaan Apple-laitteeseen, kuten iPhoneen, iPadiin tai Maciin, SHSH2-tiedosto luodaan. Tämä SHSH2-tiedosto lähetetään Applen palvelimille, jotka lukevat ja vahvistavat tämän digitaalisen allekirjoitustiedoston. Näiden tietojen perusteella palvelin sallii tai estää asennuksen.

Sama tapahtuu, kun päivitystä pyydetään. Kun käyttäjä pyytää laitteensa päivitystä tai palautusta iTunesin tai muun ohjelmiston kautta, Applen palvelimet tarkistavat, että SHSH2-tiedosto vastaa laitteen ECID- ja laiteohjelmistoversiota ennen päivityksen sallimista.

## Viitteet

* [SHSH Blob - Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)

* [TSS Saver](https://tsssaver.1conan.com/v2/)


