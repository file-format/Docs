{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "NPK tiedostomuoto",
  "description":"Opi NPK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NPK-tiedostoja.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk-fi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Mikä on NPK-tiedosto?

NPK-tiedosto on ohjelmistopäivityspaketti, jota **MikroTik**-reitittimet käyttävät reitittimen käyttöjärjestelmän päivittämiseen. Se toimitetaan pakattuna binaariarkistona, joka ladataan reitittimeen ohjelmistopäivitysten asentamista varten. NPK-tiedostojen sisältämiä tietoja ovat verkkotiedot, kuten IP-osoite ja IP-palvelu, liitintiedot (ethernet-liitännät ja sarjaportti), sähköpostin asetukset, siltamääritykset ja paikallinen käyttäjien hallinta.

## NPK tiedostomuoto

NPK-tiedostot tallennetaan pakattuna binaariarkistona. Se on suljettu tiedostomuoto, jota vain MikroTik itse käyttävät. Sitä ei ole tarkoitettu luomaan RouterOS-lisäosia kolmansien osapuolien kautta. NPK-tiedostoja ylläpitää MikroTik itse, ja niiden päivitetyt versiot voidaan ladata [MikroTik](https://mikrotik.com/download)-verkkosivuston latausosioista.

Kun NPK-tiedosto ladataan reitittimeen, reitittimen käyttöjärjestelmä ei tule voimaan, ellei sitä käynnistetä uudelleen. Siksi reitittimen käyttöjärjestelmä on käynnistettävä uudelleen, jotta se voidaan päivittää.

## Viitteet

* [MikroTik – reitittimen käyttöjärjestelmän päivitys](https://mikrotik.com/download)

* [NPK-tiedostojen luominen](https://forum.mikrotik.com/viewtopic.php?t=87126)


