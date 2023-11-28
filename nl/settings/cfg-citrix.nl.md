{
"datum": "27-09-2023",
  "keywords": [
"cfg",
"cfg-bestand",
"cfg citrix serververbindingsbestand",
"wat is een cfg-bestand",
"hoe cfg-bestand te openen",
"bestand",
"cfg-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CFG-bestandsindeling - Citrix Server Connection-bestand",
  "description":"Leer meer over het CFG Citrix Server Connection-bestandsformaat en API's waarmee CFG-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix",
"parent" : "settings"
}
},
"laatste mod": "27-09-2023"
}

## Wat is een CFG-bestand?

CFG-bestand is ook bekend als **Citrix Server Connection File**. Het is een essentieel onderdeel dat wordt gebruikt voor het tot stand brengen van een verbinding met de Citrix-server. Dit bestand bevat essentiële informatie die nodig is voor een succesvolle verbinding tussen het clientapparaat en de Citrix-server. Het bevat doorgaans details zoals de hostnaam of het IP-adres van de server, de specifieke serverpoort die moet worden gebruikt en de inloggegevens die vereist zijn voor authenticatie, die vaak een gebruikersnaam en wachtwoord omvatten.

Deze CFG-bestanden spelen een cruciale rol bij het configureren van Citrix-clientsoftware, waardoor gebruikers naadloos verbinding kunnen maken met verschillende Citrix-servers. Ze fungeren als configuratiebestanden die het verbindingsproces stroomlijnen door essentiële parameters vooraf te definiëren, waardoor gebruikers deze informatie niet elke keer handmatig hoeven in te voeren wanneer ze toegang willen krijgen tot de Citrix-server.

## Citrix-server

Een Citrix-server, ook bekend als Citrix XenApp of Citrix XenDesktop-server, is een gespecialiseerde server die wordt gebruikt in Citrix-virtualisatieoplossingen. Citrix is een bedrijf dat technologie levert voor externe toegang, applicatievirtualisatie en desktopvirtualisatie. Citrix-servers spelen een centrale rol in deze oplossingen door de levering van applicaties en desktopomgevingen aan externe gebruikers of clientapparaten te vergemakkelijken.

Hier ziet u hoe de Citrix-server doorgaans functioneert:

1. **Applicatie- en desktoplevering**: Citrix-servers hosten applicaties en desktopomgevingen. In plaats van dat de software rechtstreeks op het apparaat van de gebruiker wordt uitgevoerd, draait de applicatie of desktop op de Citrix-server en wordt alleen de gebruikersinterface naar het clientapparaat verzonden. Hierdoor hebben gebruikers toegang tot Windows-applicaties en desktops vanaf een breed scala aan apparaten, waaronder pc's, Macs, tablets en smartphones.
    















2. **Toegang op afstand**: Citrix-servers maken externe toegang tot applicaties en desktops mogelijk, waardoor gebruikers overal met een internetverbinding kunnen werken. Dit is vooral waardevol voor externe en gedistribueerde teams, omdat het een consistente en veilige computerervaring biedt.
    















3. **Load Balancing**: Citrix-servers werken vaak in clusters om de belasting van inkomende verbindingen te verdelen. Load-balancing zorgt ervoor dat gebruikersverzoeken gelijkmatig over de servers worden verdeeld, waardoor de prestaties en beschikbaarheid worden geoptimaliseerd.

## Citrix Server-verbindingsbestand

Een Citrix Server Connection File, vaak CFG-bestand genoemd, is een configuratiebestand dat in Citrix-omgevingen wordt gebruikt om verbindingen tot stand te brengen tussen clientapparaten en Citrix-servers. Belangrijke details die doorgaans in het Citrix Server Connection File zijn opgenomen, kunnen het volgende omvatten:

1. **Hostnaam of IP-adres**: dit specificeert de netwerklocatie van de Citrix-server waarmee het clientapparaat verbinding moet maken. Het identificeert waar Citrix-bronnen worden gehost.
    















2. **Serverpoort**: het poortnummer dat wordt gebruikt voor communicatie met de Citrix-server. Dit zorgt ervoor dat gegevens worden verzonden naar de juiste service op de server.
    















3. **Gebruikersnaam en wachtwoord**: Gebruikersgegevens, inclusief gebruikersnaam en wachtwoord, kunnen worden opgenomen voor authenticatiedoeleinden. Met deze inloggegevens kunnen gebruikers hun identiteit bewijzen en toegang krijgen tot Citrix-bronnen.
    















4. **Verbindingsinstellingen**: CFG-bestanden kunnen verschillende verbindingsinstellingen bevatten, zoals coderingsinstellingen, sessietime-outwaarden en weergaveopties. Deze instellingen helpen bij het configureren van gebruikerservaring en beveiligingsparameters.
    















5. **Bronconfiguratie**: Afhankelijk van de configuratie kan het CFG-bestand specificeren welke Citrix-bronnen (applicaties of desktops) moeten worden gestart wanneer de verbinding tot stand is gebracht.

## Bestandsformaten gebruikt door Citrix

Citrix-servers en gerelateerde Citrix-technologieën ondersteunen verschillende bestandsformaten om de levering van applicaties, desktops en inhoud aan externe gebruikers mogelijk te maken. Hier volgen enkele veelvoorkomende bestandsindelingen die verband houden met Citrix-serverimplementaties:

1. **ICA (Independent Computing Architecture)**:
    















- **.ica**: het ICA-bestand is het kernonderdeel van de applicatie- en desktoplevering van Citrix. Het bevat informatie over de verbinding met de Citrix-server, zoals serveradres, poort, coderingsinstellingen en weergavevoorkeuren. Wanneer de gebruiker op een Citrix-bron klikt, wordt het bestand [.ica](/nl/misc/ica/) gegenereerd en gebruikt door de Citrix Receiver (of Citrix Workspace)-client om verbinding te maken.
2. **Citrix Receiver- (of Citrix Workspace)-pakketten**:
    















- **.exe**: Citrix Receiver- of Citrix Workspace-installatiepakketten hebben vaak een uitvoerbaar formaat voor verschillende besturingssystemen (bijv. [.exe](/nl/executable/exe/) voor Windows, [.dmg](/nl/compression/dmg /) voor macOS). Met deze pakketten kunnen gebruikers clientsoftware op hun apparaten installeren.
3. **Citrix Workspace-app (voorheen Citrix Receiver)**:
    















- **.app**: Op macOS wordt de Citrix Workspace App verpakt als macOS-applicatie [.app](/nl/executable/app/) bestand.
4. **Compatibiliteit met webbrowser**:
    















- Citrix-oplossingen zijn toegankelijk via webbrowsers, waarbij doorgaans HTML5 wordt gebruikt voor webgebaseerde toegang. Gebruikers maken via URL's verbinding met Citrix-bronnen zonder dat daarvoor specifieke bestandsformaten nodig zijn.
5. **Afbeeldingen van virtuele bureaubladschijven**:
    















- **.vhd, .vhdx**: Citrix XenDesktop en XenApp kunnen virtuele desktops en applicaties leveren met behulp van virtuele harde schijf [VHD](/nl/disc-and-media/vhd/) of [VHDX](/nl/disc-and-media /vhdx/) bestanden.
6. **Metagegevens voor het publiceren van bronnen**:
    















- **.xml**: Citrix-beheerders gebruiken vaak [XML](/nl/web/xml/)-bestanden om instellingen voor het publiceren van bronnen te definiëren, inclusief applicatie-eigenschappen, toegangsbeleid en gebruikerstoewijzingen.
7. **Printerstuurprogrammabestanden**:
    















- Citrix-omgevingen vereisen mogelijk specifieke printerstuurprogrammabestanden (bijvoorbeeld .inf) om een goede afdrukfunctionaliteit te garanderen bij het gebruik van externe toepassingen.
8. **Gebruikersprofielgegevens**:
    















- **.upm**: Citrix Profile Management kan gebruikersprofielgegevens opslaan in .upm-bestanden om consistente gebruikerservaringen te bieden voor alle sessies en apparaten.
9. **Configuratiebestanden**:
    















- **.conf**: Verschillende configuratiebestanden kunnen bijvoorbeeld worden gebruikt om instellingen voor Citrix-componenten te definiëren, zoals configuratiebestanden voor Citrix License Server (bijvoorbeeld CtxLicChk.conf).
10. **Citrix ADC (NetScaler)-configuratie**:

- **.nsconfig:** Configuratiebestanden voor Citrix Application Delivery Controllers (ADC), voorheen bekend als NetScaler, slaan instellingen op met betrekking tot taakverdeling, beveiliging en verkeersbeheer.

## Hoe open je een CFG-bestand?

Programma's die CFG-bestanden openen of ernaar verwijzen

- Citrix Access-client (Windows, MAC, Linux)

## Andere CFG-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cfg** gebruiken.

**Instellingen**
- [CFG - Celestia-configuratiebestand] (/nl/settings/cfg-celestia/)
- [CFG - Citrix-serververbindingsbestand](/nl/settings/cfg-citrix/)
- [CFG - MAME-configuratiebestand] (/nl/settings/cfg-mame/)
- [CFG - LightWave-configuratiebestand] (/nl/settings/cfg-lightwave/)

**Spel**
- [CFG - Wesnoth Markup Language-bestand] (/nl/game/cfg-wesnoth/)
- [CFG - MUGEN-configuratiebestand] (/nl/game/cfg-mugen/)
- [CFG - Bronengineconfiguratiebestand](/nl/game/cfg-sourceengine/)

**Systeem en Diversen**
- [CFG - CFG-bestand](/nl/system/cfg/)
- [CFG - Cal3D-modelconfiguratiebestand] (/nl/misc/cfg-cal3d/)

## Referenties
* [Citrix virtuele apps](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)

