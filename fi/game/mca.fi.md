{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi MCA-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MCA-tiedostoja.",
  "title": "MCA - Minecraft Anvil Region -tiedostomuoto",
  "linktitle": "MCA",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-fia"
}
},
  "lastmod": "2022-12-13"
}

## Mikä on MCA-tiedosto?

Minecraft Anvil -alueen tiedostomuoto on tiedontallennusmuoto, jota käytetään Minecraft Worldin maastopalojen tallentamiseen suosittuun videopeliin **Minecraft**. Minecraft-maailma koostuu alueista, joissa jokainen alue on jaettu paloiksi. MCA-tiedostomuoto mahdollistaa suurten pelitietojen, kuten lohkojen ja entiteettien sijainnin, tehokkaan tallennuksen tietyssä pelimaailman osassa. MCA-tiedostot on yhdistettävä muihin MCA-tiedostoihin kokonaisen maailman luomiseksi.

Pelitietojen tallentamisen lisäksi Anvil-alueen tiedostomuoto sisältää tuen useille muille tietotyypeille, kuten pelaajadatalle ja metadatalle. Tämä mahdollistaa kaiken tiedon tehokkaan tallentamisen, jota tarvitaan pelimaailman tietyn osan luomiseen, mukaan lukien lohkojen, entiteettien ja muiden peliobjektien sijainti.

## MCA-tiedostomuoto – lisätietoja

Anvil-alueen tiedostomuoto on muunnelma NBT-muodosta (Named Binary Tag), joka on hierarkkinen puumainen rakenne tietojen tallentamiseksi binääritiedostoon. Tämä mahdollistaa monimutkaisten tietorakenteiden tehokkaan tallennuksen kompaktissa ja helposti luettavassa muodossa.

### Palat MCA-tiedostossa

Minecraftissa pala on pelimaailman 16x16x16 lohkoalue, joka ladataan muistiin ja esitetään pelaajan näytöllä. Anvil-alueen tiedostomuoto tallentaa kaikki tietyn osan tiedot yhteen tiedostoon, joka voidaan sitten ladata nopeasti muistiin tarvittaessa. Tämä mahdollistaa tehokkaan tallennuksen ja nopean pääsyn pelitietoihin, mikä on tärkeää sujuvan ja saumattoman pelikokemuksen takaamiseksi.

### Pieni MCA-tiedoston koko

Yksi Anvil-alueen tiedostomuodon tärkeimmistä ominaisuuksista on sen pakkausten käyttö. Tämä mahdollistaa suurten tietomäärien tehokkaan tallennuksen tinkimättä tiedon laadusta tai nopeudesta, jolla niitä voidaan käyttää. Tämä saavutetaan useilla eri tekniikoilla, kuten gzip-pakkauksella ja lohkotiedon pakkaamisella.

MCA-tiedostojen pakattu tiedostomuoto tekee siitä tärkeän osan pelin tietojen tallennus- ja hallintajärjestelmää. Sen tehokas pakkaus ja tuki eri tietotyypeille mahdollistaa tehokkaan tallennuksen ja nopean pääsyn pelitietoihin, mikä takaa pelaajille sujuvan ja saumattoman pelikokemuksen.

## MCA-tiedostomuodon rakenne

MCA-tiedostojen sisäinen tiedostomuotorakenne koostuu:
 * Otsikko ja a
 * Hyötykuorma

### MCA-otsikko

MCA-aluetiedoston otsikko alkaa 8KiB:n otsikolla, joka on jaettu kahteen 4KiB:n taulukkoon. Ensimmäinen taulukko sisältää itse aluetiedoston osien siirtymät, kun taas toisessa taulukossa on näiden osien viimeisten päivitysten aikaleimat.

### MCA-hyötykuorma

MCA-hyötykuorma koostuu paloista, joissa jokainen osatieto alkaa (big-endian) neljän tavun pituisella kentällä. Tämä kenttä ilmaisee jäljellä olevan osadatan tarkan pituuden tavuina. Viimeisen osan tiedot on pehmustettu pituudeltaan 4096B:n kerrannaiseksi. Minecraft ei hyväksy tiedostoja, joissa viimeistä osaa ei ole täytetty.

## Kuinka avata MCA-tiedostoja

Voit avata ja muokata MCA-tiedostoja MCEdit-ohjelmalla, joka on ilmainen avoimen lähdekoodin editori Minecraftille. Voit [download MCEdit](https://www.mcedit.net/) avata ja tarkastella Anvil-aluetiedostosi sisältöä viralliselta verkkosivustolta.

Kun olet asentanut MCEditin, voit avata Anvil-aluetiedoston seuraavasti:

 1. Käynnistä MCEdit ja napsauta Avaa-painiketta ikkunan vasemmassa yläkulmassa.

 1. Siirry Avoin maailma -valintaikkunassa Anvil-alueen tiedostosi sijaintiin ja valitse se.

 1. Napsauta Avaa-painiketta avataksesi tiedoston MCEditissä.

 1. MCEdit lataa tiedoston ja näyttää sen sisällön pääikkunassa. Tämän jälkeen voit käyttää MCEditin työkaluja ja ominaisuuksia tarkastellaksesi, muokataksesi ja poimiaksesi tietoja Anvil-aluetiedostosta.

## Viitteet

* [Minecraftin maailmaneditori](https://www.mcedit.net/)

* [Tietoja Minecraftista](https://www.minecraft.net/)

* [Alueen tiedostomuoto](https://minecraft.fandom.com/wiki/Region_file_format)


