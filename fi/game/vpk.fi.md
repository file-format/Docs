{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Opi Unreal Static Meshes VPK -tiedostomuodosta ja API:ista, jotka voivat luoda ja avata VPK-tiedostoja.",
  "title" : "VPK-tiedosto - Epätodellinen staattinen verkkotiedosto",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-fi",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Mikä on VPK-tiedosto?

.vpk-tiedosto on tiedostomuoto, jota käyttää **Source Engine**, Valve Corporationin kehittämä pelimoottori. VPK-tiedostoja käytetään pelisisällön, kuten mallien, tekstuurien ja äänien, pakkaamiseen, ja niitä käytetään yleisesti peleissä, kuten Team Fortress 2, Left 4 Dead ja Counter-Strike: Global Offensive. Tiedostot voidaan avata ja purkaa useilla työkaluilla, kuten GCFScape ja VPK Tool.

## VPK-tiedostomuoto - lisätietoja

VPK-tiedostot tallennetaan levylle binääritiedostoina. Yksi vpk-tiedosto voi olla osa VPK-pakettia tai se voi toimia itsenäisenä raaka-VPK-tiedostona. VPK-tiedostoon tallennettavia tietoja ovat karttoja, materiaaleja, pelisisältöä ja koreografiakohtauksia.

### Kuinka luodaan VPK-tiedosto?

On olemassa useita tapoja luoda .vpk-tiedosto käytettävissä olevista työkaluista riippuen.

1. `VPK-työkalun käyttäminen:` Tämä on komentorivityökalu, jota voidaan käyttää VPK-tiedostojen luomiseen ja purkamiseen. VPK-tiedosto voidaan luoda seuraavalla komennolla:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Tämä luo VPK-tiedoston määritetystä hakemistosta ja tallentaa sen määritettynä tulostustiedostona.

1. `Hammer Editorin käyttäminen:` Hammer Editor on Source SDK:n mukana tuleva työkalu, jota voidaan käyttää tasojen luomiseen ja muokkaamiseen lähdemoottoria käyttäville peleille. Se sisältää myös mahdollisuuden luoda VPK-tiedostoja napsauttamalla hiiren kakkospainikkeella kansiota Tiedostojärjestelmä-välilehdessä ja valitsemalla Luo VPK.

1. `Käyttäen Valven VPK:n luojaa:` Tämä on Valven kehittämä työkalu, jota käytetään pelisisällön pakkaamiseen ja jakeluun. Tätä työkalua voidaan käyttää VPK-tiedostojen luomiseen, ja se on myös virallinen työkalu VPK-tiedostojen luomiseen.

## Viitteet

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK Developer's Resources](https://developer.valvesoftware.com/wiki/GCF)

