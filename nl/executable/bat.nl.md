{
  "date" : "2021-06-24",
  "keywords" :[ "bat-bestand", "wat is een bat-bestand", "bestand", "bat-bestandsvoorbeeld", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Meer informatie over BAT-bestandsindeling en API's die BAT-bestanden kunnen maken en openen.",
  "title" :"BAT - Batch-bestandsindeling",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## Wat is een BAT-bestand?
Een BAT-bestand staat bekend als een batchbestand dat wordt uitgevoerd met DOS en alle versies van Windows, onder cmd.exe. Het bestaat uit een reeks regelopdrachten in platte tekst die door de opdrachtregelinterpreter moeten worden uitgevoerd om verschillende taken uit te voeren, zoals het uitvoeren van onderhoudshulpprogramma's binnen Windows of het starten van typische programma's. Een batchbestand kan elke opdracht bevatten die interactief door de interpreter kan worden geaccepteerd en die de codestructuur gebruikt die voorwaardelijke vertakking en looping mogelijk maakt, zoals geschreven in het batchbestand.
## BAT-bestandsindeling
Een BAT-bestandsindeling is gewoon een script dat is ingebouwd om opdrachtreeksen te automatiseren die repetitief van aard zijn. De term "batch" wordt gebruikt voor batchverwerking. Het kan worden beschouwd als "niet-interactieve uitvoering". Daarom mag een batchbestand niet een batch van meerdere gegevens verwerken. In het oude Disk Operating System (DOS) werd het batchbestand uitgevoerd onder de opdrachtregelinterface door de bestandsnaam en de extensie .bat te typen. Het eerdere op een grafische interface van Microsoft gebaseerde besturingssysteem, zoals Microsoft Windows, was afhankelijk van DOS. De gebruikers moesten DOS gebruiken om typische bewerkingen uit te voeren, zoals het repareren, optimaliseren of opnieuw installeren van Windows. Later introduceerde Microsoft Windows NT dat niet afhankelijk was van het DOS-besturingssysteem. Daarom kunnen de batchbestanden worden uitgevoerd met behulp van de opdrachtprompt of **cmd.exe** in de moderne Microsoft-besturingssystemen.
### Batchbestand parameters
Opdrachtprompt ondersteunt een aantal speciale variabelen zoals **%0, %1 tot %9** om te verwijzen naar de naam en het pad van de batchtaak en de negen aanroepparameters vanuit de batchtaak. Niet-bestaande parameters worden vervangen door een string met een lengte van nul. Hoewel ze vergelijkbaar met omgevingsvariabelen kunnen worden gebruikt, worden ze niet in de omgeving opgeslagen. Microsoft en IBM noemen deze variabelen vervangingsparameters, terwijl Novell, Digital Research en Caldera de term vervangingsvariabelen voor hen introduceerden.

Hier zijn enkele handige opdrachten voor batchbestanden:
| Commando | Beschrijving |
------|------------|
| VER | Deze batchopdracht toont de versie van MS-DOS die u gebruikt. |
|ASSOC| Dit is een batchopdracht die een extensie koppelt aan een bestandstype (FTYPE), bestaande associaties weergeeft of een associatie verwijdert. |
|CD| Deze batchopdracht helpt bij het maken van wijzigingen in een andere map of geeft de huidige map weer. |
|CLS| Deze batchopdracht maakt het scherm leeg. |
|KOPIE| Deze batchopdracht wordt gebruikt om bestanden van de ene naar de andere locatie te kopiëren. |
|DEL| Deze batchopdracht verwijdert bestanden en geen mappen. |
|DIR| Deze batchopdracht geeft de inhoud van een map weer. |
|DATUM| Deze batchopdracht helpt bij het vinden van de systeemdatum. |
|ECHO| Dit batchcommando geeft berichten weer of zet commando-echo aan of uit. |
|EXIT| Met deze batchopdracht wordt de DOS-console afgesloten. |
|MD| Deze batchopdracht maakt een nieuwe map aan op de huidige locatie. |
|VERPLAATSEN| Deze batchopdracht verplaatst bestanden of mappen tussen mappen. |
|PATH| Deze batchopdracht geeft de padvariabele weer of stelt deze in. |
|PAUZE| Deze batchopdracht vraagt de gebruiker en wacht op het invoeren van een invoerregel. |
|PROMPT| Deze batchopdracht kan worden gebruikt om de cmd.exe-prompt te wijzigen of opnieuw in te stellen. |
|RD| Deze batchopdracht verwijdert mappen, maar de mappen moeten leeg zijn voordat ze kunnen worden verwijderd. |
|REN| Hernoemt bestanden en mappen |
|REM| Dit batchcommando wordt gebruikt voor opmerkingen in batchbestanden, waardoor de inhoud van de opmerking niet kan worden uitgevoerd. |
|START| Deze batchopdracht start een programma in een nieuw venster of opent een document. |
|TIJD| Met deze batchopdracht wordt de tijd ingesteld of weergegeven. |
|TYPE| Deze batchopdracht drukt de inhoud van een bestand of bestanden af naar de uitvoer. |
|VOL| Deze batchopdracht geeft de volumelabels weer. |
|ATTRIB| Toont of stelt de attributen van de bestanden in de huidige directory in |
|CHKDSK| Deze batchopdracht controleert de schijf op eventuele problemen. |
|KEUZE| Deze batchopdracht biedt de gebruiker een lijst met opties. |
|CMD| Deze batchopdracht roept een ander exemplaar van de opdrachtprompt aan. |
|COMP| Deze batchopdracht vergelijkt 2 bestanden op basis van de bestandsgrootte. |
|CONVERTEREN| Deze batchopdracht converteert een volume van het FAT16- of FAT32-bestandssysteem naar het NTFS-bestandssysteem. |
|DRIVERQUERY| Deze batchopdracht toont alle geïnstalleerde apparaatstuurprogramma's en hun eigenschappen. |
|UITBREID| Deze batchopdracht extraheert bestanden uit gecomprimeerde .cab-kastbestanden. |
|VINDEN| Deze batchopdracht zoekt naar een tekenreeks in bestanden of invoer, waarbij overeenkomende regels worden uitgevoerd. |
|FORMAAT| Deze batchopdracht formatteert een schijf om een door Windows ondersteund bestandssysteem zoals FAT, FAT32 of NTFS te gebruiken, waarbij de vorige inhoud van de schijf wordt overschreven. |
|HELP| Deze batchopdracht toont de lijst met door Windows geleverde opdrachten. |
|IPCONFIG| Deze batchopdracht geeft de Windows IP-configuratie weer. Toont configuratie per verbinding en de naam van die verbinding. |
|LABEL| Met deze batchopdracht wordt een schijflabel toegevoegd, ingesteld of verwijderd. |
|MEER| Deze batchopdracht geeft de inhoud van een bestand of bestanden weer, scherm voor scherm. |
|NET| Biedt verschillende netwerkdiensten, afhankelijk van de gebruikte opdracht. |
|PING| Deze batchopdracht stuurt ICMP/IP "echo"-pakketten over het netwerk naar het opgegeven adres. |
|UITSCHAKELEN| Met deze batchopdracht wordt een computer afgesloten of wordt de huidige gebruiker uitgelogd. |
|SORTEREN| Deze batchopdracht haalt de invoer uit een bronbestand en sorteert de inhoud alfabetisch, van A naar Z of Z naar A. Het drukt de uitvoer af op de console. |
|SUBST| Deze batchopdracht wijst een stationsletter toe aan een lokale map, geeft huidige toewijzingen weer of verwijdert een toewijzing. |
|SYSTEMINFO| Deze batchopdracht toont de configuratie van een computer en het besturingssysteem. |
|TASKILL| Deze batchopdracht beëindigt een of meer taken. |
|TASKLIJST| Deze batchopdracht geeft een lijst van taken, inclusief taaknaam en proces-ID (PID). |
|XCOPY| Deze batchopdracht kopieert bestanden en mappen op een meer geavanceerde manier. |
|BOOM| Deze batchopdracht toont een boomstructuur van alle subdirectories van de huidige directory tot elk niveau van recursie of diepte. |
|FC |Dit batch-commando geeft de feitelijke verschillen tussen twee bestanden weer. |
|DISKPART |Deze batchopdracht toont en configureert de eigenschappen van schijfpartities. |
|TITLE |Deze batchopdracht stelt de titel in die in het consolevenster wordt weergegeven. |
|SET | Geeft de lijst met omgevingsvariabelen op het huidige systeem weer. |

## BAT-bestand voorbeeld
Batchscripts worden meestal opgeslagen als eenvoudige tekstbestanden; met opdrachten die in een reeks worden uitgevoerd. Deze bestanden worden opgeslagen met de extensie .bat; herkend en uitgevoerd met behulp van **Command Interpreter**-software. Deze software is standaard beschikbaar in Microsoft Windows met de naam **cmd.exe**.

Hier is een voorbeeld van een batchscript dat alle bestanden in de huidige map verwijdert:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referenties

* [Batchscript - Beknopte handleiding](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Batchbestand - door Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

