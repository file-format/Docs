{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "RML - Elixir-raporttimallitiedosto",
  "description":"Opi RML-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata RML-tiedostoja.",
  "linktitle" : "RML",
  "menu" : {
    "docs" : {
      "identifier":"misc-rml-fi",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Mikä on RML-tiedosto?

RML-tiedosto on raporttimallitiedosto, jossa on [Elixir Repertoire](https://elixirtech.com/repertoire-2/)-raporttimoottori. Mallitiedostoa käytetään raporttien luomiseen Elixir FileSystemiin liitetyn tietolähteen kanssa. Tiedot luetaan ja täytetään RML-mallitiedostoon, ja ne voidaan viedä useisiin eri tiedostomuotoihin, kuten [PDF](/pdf/), [RTF](/word-processing/rtf/) ja laskentataulukkoon [XLS](/spreadsheet/xls/). Elixir Repertoire -raportointimoottori voidaan yhdistää monenlaisiin JDBC-tietolähteisiin.

## RML-tiedostomuoto

RML-tiedostomuodon sisäiset tiedostorakenteen tiedot eivät ole saatavilla julkisesti. Elixir Repertoire -sovellus luo ja tallentaa tiedostot sisäisesti raporttien luomiseksi liitetyistä tietolähteistä täytetyillä tiedoilla. RML-mallitiedosto sisältää tiedoista luotavan loppuraportin yleisen asettelun ja paikkamerkit.

## Kuinka RML-mallitiedosto?

RML-mallin luomiseksi Elixir Repertoaarissa voidaan noudattaa seuraavia vaiheita.

1. Yhdistä JDBC-tietolähde tiedostojärjestelmään.
1. Käynnistä ohjattu raporttimallin toiminto
1. Käytä ohjelmistoa tietolähteen .ds-tiedoston paikantamiseen
1. Valitse vientivaihtoehdoksi taulukkoraportti
1. Valitse raporttimalliin sisällytettävät kentät
1. Lopuksi, kun napsautat Valmis-painiketta, First report.rml lisätään arkistoon ja avataan näyttämään Layout-välilehti.

## Viitteet

* [Elixir Repertoire](https://elixirtech.com/repertoire-2/)


