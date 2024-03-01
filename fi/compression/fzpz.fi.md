{
  "date": "2022-06-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FZPZ-tiedostomuoto - Fritzing-osatiedosto",
  "description": "Opi, mikä on FZPZ-tiedosto ja API:t, jotka voivat luoda ja avata FZPZ-tiedostoja.",
  "linktitle": "FZPZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-fzp-fiz"
}
},
  "lastmod": "2022-06-20"
}

## Mikä on FZPZ-tiedosto?

An FZPZ file is a component/part used in an electronic circuit design created with the circuit prototyping and design application **Fritzing**. It is a compressed archive that contains an [FZP](/cad/fzp/) file and four [SVG](/page-description-language/svg/) images describing the overall part in Fritzing. The advantage of using these files is that users can share their FZPZ files with each from reusability point of view. The sharing of FZPZ parts help in integrating circuit parts to create larger PCB designs in a quick manner.

## FZPZ-tiedostomuoto - lisätietoja

FZPZ-tiedostot tallennetaan levylle pakattujen [ZIP](/compression/zip/)-arkistojen muodossa. Voit nimetä laajennuksen uudelleen .fzpz:stä .zip:ksi ja käyttää mitä tahansa tavallista purkuapuohjelmaa, kuten WinZIP:tä, tiedostojen purkamiseen arkistosta.

### FZPZ-tiedostorakenteen tiedot

Kuten mainittiin, FZPZ-tiedosto on arkistotiedosto, joka sisältää useita tiedostoja painetussa piirilevyssä käytetyn osan esittämiseksi. FZPZ sisältää seuraavat tiedostot:

 * Neljä SVG-tiedostoa - jotka edustavat osan koeppilevyä, kaaviota, PCB- ja kuvakekuvia
 * FZP-tiedosto - XML-tiedosto, joka sisältää tietoja osan ominaisuuksista, liittimistä ja väylistä

Tiedostot nimetään yleensä seuraavasti.

 * part.file.fzp
 * svg.breadboard.file.svg
 * svg.icon.file.svg
 * svg.pbc.file.svg
 * svg.schematic.file.svg

## Viitteet ##

* [Uudet osat fzpz-laajennuksella](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)


