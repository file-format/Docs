{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Opi MDS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MDS-tiedostoja.",
  "title" : "MDS-tiedostomuoto - Media Descriptor Sidecar -tiedosto",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-fi",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## Mikä on MDS-tiedosto?

MDS (Media Descriptor Sidecar File) on tiedosto, joka liittyy ohjelmistoihin Alcohol 120% ja Daemon Tools, joita molempia käytetään virtuaalisten CD- ja DVD-asemien luomiseen ja hallintaan. MDS-tiedosto sisältää tietoja levyn tietojen asettelusta, mukaan lukien kaikkien tiedostojen sijainnit ja levyn rakenne. Tämän ansiosta virtuaaliasema voi emuloida fyysisen levyn käyttäytymistä, jotta ohjelmisto voi lukea virtuaalilevyn tiedot ikään kuin se olisi oikea levy.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## Suhde alkoholiin 120 %

Alcohol 120% on suosittu ohjelmisto virtuaalisten CD- ja DVD-asemien luomiseen ja hallintaan, ja se käyttää MDS-tiedostomuotoa levykuvien tallentamiseen ja käyttämiseen. MDS-tiedostomuoto on Alcohol 120%:n oma, ja sen voi avata ja käyttää vain Alcohol 120% -ohjelmistolla tai muulla sitä tukevalla ohjelmistolla.

## Kuinka avata MDS -tiedosto?

Jotta voit avata MDS-tiedoston Alcohol 120% -sovelluksessa, ohjelmiston on oltava asennettuna tietokoneellesi. Kun olet asentanut Alcohol 120%:n, voit avata MDS-tiedoston seuraavasti:

1. Launch Alcohol 120%.
2. Napsauta Tiedosto-valikkoa ja valitse Avaa.
3. Siirry MDS-tiedoston sijaintiin tietokoneellasi ja valitse se.
4. MDS-tiedosto avataan nyt Alcohol 120% -tilassa ja sinua pyydetään valitsemaan vastaava kuvatiedosto (kuten ISO, BIN tai CUE).
5. Kun olet valinnut kuvatiedoston, Alcohol 120% liittää kuvan virtuaaliasemaan.

Vaihtoehtoisesti voit myös avata MDS-tiedoston kaksoisnapsauttamalla sitä, jos Alcohol 120% on asetettu oletusohjelmaksi MDS-tiedostojen avaamiseen. Voit myös käyttää muita ohjelmistoja, jotka tukevat MDS-muotoa, kuten Daemon Tools, Virtual CloneDrive, Virtual Drive Manager ja MagicISO.

## Viitteet
* [Alcohol 120% – CD- ja DVD-polttoohjelmisto](https://www.alcohol-soft.com/)


