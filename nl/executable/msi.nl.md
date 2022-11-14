{
  "date" : "2021-06-30",
  "keywords" :[ "msi-bestand", "MSI-bestandsindeling", "wat is een msi-bestand", "bestand", "msi-voorbeeld", "msi-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over MSI-bestandsindeling en API's die MSI-bestanden kunnen maken en openen.",
  "title" :"MSI - Windows Installer-pakketbestand",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Wat is een MSI-bestand?
Een MSI-bestand dat wordt gebruikt om Windows-programma's te installeren en te starten; een compleet pakket voor Microsoft Windows dat installatie-informatie bevat voor een typisch softwareprogramma, inclusief essentiële bestanden die moeten worden geïnstalleerd en informatie over de installatielocatie. De MSI-bestanden kunnen ook het pakket voor software-updates bevatten. MSI-bestanden lijken op [EXE](/nl/executable/exe/), maar EXE bevat soms geen informatie over het installatieprogramma en het softwareprogramma kan direct worden uitgevoerd wanneer het EXE-bestand wordt uitgevoerd.

## MSI-bestandsindeling
Windows Installer is eigenlijk een API (Application Programming Interface) en softwarecomponent van Microsoft Windows die wordt gebruikt voor de installatie, verwijdering en het onderhoud van een softwareprogramma. De installatie-informatie en de optionele bestanden zijn verpakt als installatiepakketten en losjes relationele databases gestructureerd als COM Structured Storages; bekend als **MSI-bestanden**, met de bestandsextensie .msi. De pakketten met de bestandsextensie **.mst** bevatten **Transformation Scripts** van Windows Installer, bestanden met de **.msm** extensie bevatten **Merge Modules** en de bestandsextensie **.pcp** wordt gebruikt voor **Eigenschappen voor het maken van patches**. Windows Installer wordt geavanceerder na belangrijke wijzigingen ten opzichte van de eerdere versies, Setup API. Een GUI-framework en het automatisch genereren van de de-installatievolgorde zijn de nieuwe functies van Windows Installer. Het is nu beschouwd als een alternatief voor stand-alone uitvoerbare installatiekaders.

### Logische structuur van MSI-pakketten
Een pakket duidt de installatie van een of meer volledige producten aan en wordt over het algemeen geïdentificeerd door een **GUID**. Een product bestaat uit een of meerdere componenten en is gegroepeerd in verschillende kenmerken. De Windows Installer verwerkt de afhankelijkheden tussen verschillende producten niet tegelijkertijd. De logische opbouw van pakketten bestaat uit de volgende elementen:

- **Producten**: Een enkel, geïnstalleerd, werkend programma of een set van meerdere programma's gecombineerd is een product. Een product wordt geïdentificeerd door een unieke GUID.
- **Kenmerken**: kan een willekeurig aantal componenten en andere subfuncties bevatten. Kleinere pakketten kunnen uit één functie bestaan.
- **Componenten**: Component wordt door Windows Installer als een eenheid behandeld; kan programmabestanden, mappen, registersleutels, COM-componenten en snelkoppelingen bevatten.
- **Key Paths**: een sleutelpad is een specifiek bestand, ODBC-gegevensbron of registersleutel die door de pakketauteur als essentieel voor een bepaald onderdeel is opgegeven.

## Referenties

* [Windows Installer - door Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


