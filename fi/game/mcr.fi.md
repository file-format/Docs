{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MCR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MCR-tiedostoja.",
  "title": "MCR - Minecraft-alueen tiedostomuoto",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-fir"
}
},
  "lastmod": "2022-12-14"
}

## Mikä on MCR-tiedosto?

Minecraft MCR -tiedostomuoto on tietomuoto, jota Minecraft käyttää Minecraft Worldin maastopalojen tallentamiseen. Se perustuu NBT (Named Binary Tag) -muotoon, jonka ovat kehittäneet suositun avoimen lähdekoodin pelimoottorin, Minecraft Forgen, kehittäjät. MCR-tiedostotyyppi otettiin käyttöön heti alussa ja korvattiin myöhemmin {{HYPERLINKKI}}:lla.

## MCR tiedostomuoto

MCR-tiedostomuoto on rakennettu sarjaksi nimettyjä binääritunnisteita, joista jokainen sisältää tietyntyyppistä dataa. Ylimmän tason tagi on Level-tunniste, joka sisältää kaikki tiedot yhdeltä pelitasolta. Level-tunnisteen sisällä on useita muita nimettyjä tunnisteita, jotka tallentavat erityyppisiä tietoja, kuten Data-tunniste, joka tallentaa tietoa pelimaailmasta, ja Entities- ja TileEntities-tagit, jotka tallentavat tietoja pelimaailmasta. peliobjekteja ja laattakokonaisuuksia maailmassa.

## Mitä MCR-tiedostomuodon sisällä on?

Minecraft MCR -tiedostomuodossa alue on pelimaailman 32x32 lohkoalue. MCR-muoto jakaa pelimaailman alueisiin, jotta dataa voidaan hallita tehokkaammin ja mahdollistaa pelitasojen nopeamman lataamisen ja tallentamisen. Jokainen alue on tallennettu erilliseen tiedostoon, ja MCR-tiedostomuoto käyttää koordinaattijärjestelmää tunnistaakseen kunkin alueen sijainnin pelimaailmassa. Alueen koordinaatit määritetään alueen vasemman alakulman lohkokoordinaateilla. Esimerkiksi alue, jolla on koordinaatit (-1,0), sijaitsisi yhden alueen vasemmalla ja nolla aluetta alaspäin pelimaailman alkuperästä.

## MCR-tiedostomuodon tekniset tiedot

MCR-tiedostomuodon tekniset tiedot ovat julkisesti saatavilla. NBT-muodon tekniset tiedot, joihin MCR-muoto perustuu, ovat saatavilla Minecraft Forgen verkkosivustolla. Lisäksi [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) sisältää yksityiskohtaisia tietoja MCR-tiedostomuodosta, mukaan lukien sen rakenteesta ja sen tukemista eri tietotyypeistä.

### Pakatut tiedot MCR-tiedostoissa

Minecraft MCR -tiedostomuoto tukee pakkausta. MCR-tiedostomuoto perustuu The [NBT format](https://minecraft.fandom.com/wiki/NBT_format) -tiedostoon, joka mahdollistaa tietojen tallentamisen pakatussa muodossa. Tämä auttaa pienentämään MCR-tiedostojen kokoa ja tehostamaan niiden siirtämistä ja tallentamista. Tämä on tärkeä ominaisuus MCR-tiedostomuodossa, koska sen avulla pelaajat voivat jakaa suuria Minecraft World -maastotietoja muiden kanssa.

## Viitteet

* [Minecraftin maailmaneditori](https://www.mcedit.net/)

* [Tietoja Minecraftista](https://www.minecraft.net/)

* [Alueen tiedostomuoto](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT-muoto](https://minecraft.fandom.com/wiki/NBT_format)


