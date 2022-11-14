{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK-bestandsindeling",
  "description":"Meer informatie over NPK-bestandsindelingen en API's die NPK-bestanden kunnen maken en openen.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
      "identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Wat is een NPK-bestand?

Een NPK-bestand is een software-upgradepakketbestand dat door **MikroTik**-routers wordt gebruikt voor het upgraden van het besturingssysteem van de router. Het wordt geleverd als een gecomprimeerd binair archief dat in de router wordt geladen voor het installeren van software-updates. Informatie in een NPK-bestand omvat netwerkinformatie zoals IP-adres en IP-service, connectorinformatie (ethernetinterfaces en seriële poort), e-mailconfiguratie, bridge-configuratie en lokaal gebruikersbeheer.

## NPK-bestandsindeling

NPK-bestanden worden opgeslagen als gecomprimeerd binair archief. Het is een gesloten bestandsformaat dat alleen door MikroTik zelf wordt gebruikt. Het is niet de bedoeling om RouterOS-add-ons te maken via derden. NPK-bestanden worden door MikroTik zelf onderhouden en geüpgradede versies daarvan kunnen worden gedownload van de downloadsecties van de website [MikroTik](https://mikrotik.com/download).

Wanneer een NPK-bestand naar een router wordt geüpload, wordt het router-besturingssysteem pas van kracht als het opnieuw wordt opgestart. Daarom is een herstart vereist om het router-besturingssysteem te kunnen upgraden.

## Referenties

* [MikroTik - Router-besturingssysteem upgraden](https://mikrotik.com/download)
* [Hoe NPK-bestanden maken](https://forum.mikrotik.com/viewtopic.php?t=87126)

