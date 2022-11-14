{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "extensie", "bestand", "format", "systeem", "Dynamic Link Library", "instellingen", "programma's", "computer", "toepassing" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Dynamic Link-bibliotheek",
  "description":"Meer informatie over DLL-bestandsindelingen en API's die DLL-bestanden kunnen maken en openen.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Wat is een DLL-bestand? ##

Een DLL-bestand of Dynamic Link Library is een soort uitvoerbaar bestand. Het is een van de meest voorkomende extensiebestanden op uw apparaat en wordt meestal opgeslagen in de System32-map op uw Windows. Het DLL-extensiebestand is ontwikkeld door Microsoft en wordt in de volksmond door hen gebruikt. Het heeft een hoge gebruikerswaardering. De DLL werkt als een plank die de *stuurprogramma's/procedures/functies/eigenschappen* bevat die zijn ontworpen en toegepast voor een programma/toepassing door de Windows-server. Een enkel DLL-bestand kan ook worden gedeeld tussen verschillende Windows-programma's. Deze extensiebestanden zijn van vitaal belang voor een soepele werking van Windows-programma's op uw apparaat, omdat ze verantwoordelijk zijn voor het inschakelen en uitvoeren van verschillende functies van het programma, zoals het schrijven en lezen van bestanden en het verbinden met andere apparaten die zich buiten uw installatie bevinden.
Deze bestanden kunnen echter alleen worden geopend op een apparaat dat elke versie van Windows ondersteunt (windows 7/windows 10/etc.) en kunnen daarom niet rechtstreeks worden geopend op een apparaat dat Mac OS ondersteunt. (Als u een DLL-bestand op Mac OS wilt openen, kunnen verschillende externe toepassingen u helpen deze te openen.)


## DLL-bestandsindeling ##

DLL-bestand is ontwikkeld door Microsoft en heeft de extensie ".dll" die het type vertegenwoordigt. Het is een integraal onderdeel van de Windows 1.0-server en verder. Het is een binair bestandstype en wordt ondersteund door alle versies van Microsoft Windows. Dit bestandstype is gemaakt als middel om een gedeeld bibliotheeksysteem binnen Windows-programma's te creëren, om afzonderlijke en onafhankelijke bewerkingen of wijzigingen in de programmabibliotheken mogelijk te maken zonder de programma's opnieuw te hoeven koppelen.


## DLL-voorbeeld ##

Voorbeeldcode voor een DLL-ingangspunt vindt u hieronder:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Referentie ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
