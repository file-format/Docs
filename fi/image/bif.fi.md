{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BIF-tiedosto - Ventana koko diakuvamuoto",
  "description":"Opi BIF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata BIF-tiedostoja.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-fi",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## Mikä on BIF-tiedosto?

BIF-tiedosto on rasterikuvatiedosto, joka sisältää dianäytteen kuvan. Se koostuu useista TIFF-kuvista, jotka diojen katselusovellukset yhdistävät yhdeksi yhdistelmäkuvaksi. BIF-tiedostot on luotu Ventana Medical Systemsin digitaalisella diaskannerilla, ja ne ovat täysin yhteensopivia [TIFF](/image/tiff/) v 6.0 -määritelmän BigTIFF-version kanssa.

## BIF-tiedostomuoto

BIF-tiedosto tallennetaan binäärikuvatiedostona, ja se koostuu jopa 200 000 x 200 000 pikselistä. Tämä voi johtaa suuriin tiedostokokoihin, mikä rikkoo TIF-standardin määrittelemien 32-bittisten tiedostoosoittimien asettaman 4 Gt:n kokorajan. 64-bittisten tiedostoosoittimien avulla TIFF-standardin BigTIFF-muunnos voittaa tämän tiedostokoon esteen.

### Kuka käyttää BIF-tiedostoa?

Digitaaliset diaskannerit käyttävät BIF-tiedostoja dianäytteiden skannaukseen ja digitaalisten kopioiden luomiseen. Jos olet patologi, voit avata nämä BIF-tiedostot diakatseluohjelmissa. Suurin yksityiskohtien ja korkearesoluutioisten tietojen ansiosta voit lähentää ja loitontaa diakuvaa nähdäksesi näyteosien enemmän tai vähemmän yksityiskohtia. Näissä tiedostoissa oleva metatietotiedosto [XML](/web/xml/) määrittää, kuinka kuvat yhdistetään ja mitä kuvaa tulee käyttää tiedoston pikkukuvana.

## Kuinka avata BIF-tiedosto?

Voit avata BIF-tiedostoja seuraavilla tavoilla:

 * OpenSlide (alustojen välinen)
 * ImageJ (alustojen välinen)
 * NetScope Viewer (Windows)

## Viitteet ##

 * [Roche Digital Pathology BIF Whitepaper](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

