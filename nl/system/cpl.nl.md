{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extensie", "bestand", "format", "systeem", "Configuratieschermbestand", "Windows", "programma's", "computer", "toepassing"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Configuratieschermbestand",
  "description":"Meer informatie over CPL-bestandsindeling en API's die CPL-bestanden kunnen maken en openen.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Wat is een CPL-bestand? ##

Een CPL-bestand is een type "systeem"-bestand. Het wordt gebruikt door het Windows-besturingssysteem. Een CPL-bestand is een afkorting voor Control Panel File. Deze bestanden zijn binaire bestanden die worden geopend met het configuratiescherm in een Microsoft Windows-besturingssysteem en worden gebruikt om de beschikbare tools in het configuratiescherm, zoals muis, beeldschermen en netwerken, weer te geven en te openen. De CPL-bestanden worden meestal opgeslagen in de systeemmap op uw apparaat. Deze bestanden mogen niet handmatig worden geopend.


## CPL-bestandsindeling ##

Verschillende CPL-bestanden in uw Windows-besturingssysteem zijn verbonden om verschillende items op het bedieningspaneel weer te geven. Alle items op het bedieningspaneel zijn gekoppeld aan een CPL-bestand en hebben het achtervoegsel ".cpl" aan hun items.

Enkele veelvoorkomende typen CPL-bestanden met hun indelingen zijn:

* Inetcpl.cpl - Voor interneteigenschappen op uw apparaat
* Appwiz.cpl - Om eigenschappen van programma's op uw apparaat toe te voegen of te verwijderen
* Desk.cpl – Voor de weergave-eigenschappen
* Main.cpl – Voor eigenschappen met betrekking tot muis, lettertypen, toetsenbord en printers.
* Netcpl.cpl – Voor netwerkgerelateerde eigenschappen
* System.cpl – Voor systeemgerelateerde eigenschappen en de wizard Nieuwe hardware toevoegen
* TimeDate.cpl – Voor eigenschappen voor datum of tijd
* Mlcfg32.cpl – Voor eigenschappen van Microsoft Exchange of Windows Messaging
* Intl.cpl – Dit heeft betrekking op de eigenschappen van Regionale instellingen
* Modem.cpl – Voor modemgerelateerde eigenschappen
* Themes.cpl - Slaat bureaubladthema's en eigenschappen op.
* Password.cpl – Voor wachtwoordeigenschappen
* Mmsys.cpl – Voor multimedia-eigenschappen
* Wgpocpl.cpl – Heeft betrekking op Microsoft Mail Post Office

## Korte geschiedenis ##

CPL-bestandstype is ontwikkeld door Microsoft Windows en is een integraal onderdeel van het Windows-besturingssysteem sinds Windows 1.0. Het wordt nog steeds gebruikt in alle Windows-versies en alle eigenschappen van het configuratiescherm worden opgeslagen met dit bestandstype.

## CPL-voorbeeld ##

Een voorbeeld van een CPL-bestand is hieronder te zien:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
