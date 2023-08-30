{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Meer informatie over de VHDX-bestandsindeling en API's die VHDX-bestanden kunnen maken en openen.",
  "title" :"VHDX-bestandsindeling - Wat is een VHDX-bestand?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Wat is een VHDX-bestand?

Een VHDX-bestand is een schijfkopiebestand in de bestandsindeling Virtual Hard Disk v2. Het bevat een volledig besturingssysteem dat kan worden geladen en gebruikt als elke normale machine voor het testen van software of het uitvoeren van software waarvoor een specifiek besturingssysteem vereist is. Een VHDX wordt, ondanks dat het een volledige schijfkopie is, in één bestand opgeslagen. Software voor virtuele machines zoals Parallels Desktop, Windows Virtual Machine en Virtual Box kan de schijfkopie laden en openen.

VHDX-bestand kan worden geconverteerd naar [VHD](/nl/disc-and-media/vhd/) met Hyper-V Manager, of naar [VDI](/nl/disc-and-media/vdi/) met VirtualBox.

## VHDX-bestandsindeling - Meer informatie

De details van de VHDX-bestandsindeling zijn volledig gedocumenteerd en online beschikbaar als [VHDX-bestandsindelingsspecificaties](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) op Microsoft-documentatie. Het is een uitbreiding op het VHD-formaat en bevat verbeterde mogelijkheden. VHDX-bestandsindeling biedt extra functies die beschikbaar zijn op de virtuele harde schijf en virtuele harde schijf-bestandslagen. Het is meer geoptimaliseerd en geeft betere resultaten voor de configuratie en mogelijkheden van opslaghardware. VHDX-bestanden kunnen worden geopend

### Ondersteuning voor virtuele harde schijven in VHDX

Het ondersteunt drie soorten virtuele harde schijven.

1. **Vaste virtuele harde schijf** - Virtuele harde schijf met toegewezen vaste gegevensgrootte. De grootte van de virtuele harde schijf verandert niet bij het toevoegen of verwijderen van gegevens.

1. **Dynamische virtuele harde schijf** - Virtuele harde schijf met dynamische schijfgrootte. De grootte is op elk moment zo groot als de daadwerkelijke gegevens die erop zijn geschreven en metagegevens. De bestandsgrootte neemt dynamisch toe naarmate er gegevens worden toegevoegd of verwijderd.

1. **Verschillende virtuele harde schijf** - Vertegenwoordigt de stroom van de virtuele harde schijf als een set gewijzigde blokken in vergelijking met een bovenliggend virtueel harde-schijfbestand.

## Referenties

* [VHDX-bestandsindelingsspecificaties](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - door Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

