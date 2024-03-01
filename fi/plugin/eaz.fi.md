{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ File - Mikä on EAZ -tiedosto ja kuinka avata se?",
  "description":"Opi EAZ-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EAZ-tiedostoja.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-fiz"
}
},
  "lastmod" : "2023-12-23"
}

## Mikä on EAZ-tiedosto?

EAZ-tiedosto on lisäosatiedosto, jota käyttää ArcGIS Explorer, ESRI:n kehittämä ilmainen sovellus karttojen tutkimiseen, visualisointiin ja jakamiseen. Se sisältää pakatun tiedostoarkiston, joka sisältää {{HYPERLINKKI}}, käännetyn koodin ja apuohjelmassa tarvittavat tukitiedostot. Näitä tiedostoja käytetään laajentamaan ohjelmiston perustoimintoja lisäämällä uusia painikkeita, telakoitavia ikkunoita ja muita laajennuksia.

## EAZ-tiedostomuoto - lisätietoja

EAZ-tiedostot luodaan käyttämällä ArcGIS Explorer SDK:ta, kehityspakettia, joka on suunniteltu mukautettujen toimintojen luomiseen ArcGIS Explorerissa. Nämä tiedostot käyttävät [ZIP](/compression/zip/)-pakkausta sisällön tehokkaaseen pakkaamiseen. Arkiston ytimessä oleva **Addins.xml**-tiedosto sijaitsee juurihakemistossa, ja se on tärkeä osa EAZ-tiedostoon upotettuja eri mukautuksia ja yksityiskohtia.

Addins.xml-tiedosto toimii pohjimmiltaan etenemissuunnitelmana, joka tarjoaa näkemyksiä erityisistä parannuksista, muokkauksista ja laajennuksista, jotka EAZ-tiedosto tuo ArcGIS Exploreriin. Tämän kattavan rakenteen avulla kehittäjät voivat kapseloida ja integroida saumattomasti uusia ominaisuuksia, painikkeita ja telakoitavia ikkunoita, mikä parantaa ArcGIS Explorer -sovelluksen yleistä toimivuutta ja käyttökokemusta.

## Viitteet

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
