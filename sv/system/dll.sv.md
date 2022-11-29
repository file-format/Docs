{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "tillägg", "fil", "format", "system", "Dynamiskt länkbibliotek", "inställningar", "program", "dator", "applikation" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Dynamic Link Library",
  "description":"Läs mer om DLL-filformat och API:er som kan skapa och öppna DLL-filer.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Vad är en DLL-fil? ##

En DLL-fil eller Dynamic Link Library är en typ av körbar fil. Det är en av de vanligaste tilläggsfilerna på din enhet och lagras vanligtvis i System32-mappen på din Windows. DLL-förlängningsfilen utvecklades av Microsoft och används populärt av dem. Den har en hög popularitetsanvändarbetyg. DLL fungerar som en hylla som innehåller *drivrutiner/procedurer/funktioner/egenskaper* som är designade och applicerade för ett program/applikation av Windows-servern. En enda DLL-fil kan också delas mellan olika Windows-program. Dessa tilläggsfiler är viktiga för att Windows-program ska fungera smidigt på din enhet, eftersom de är ansvariga för att aktivera och köra olika funktioner i programmet som att skriva och läsa filer, ansluta till andra enheter som är externa till din installation.
Dessa filer kan dock bara öppnas på en enhet som stöder alla versioner av Windows (windows 7/windows 10/etc.) och kan därför inte öppnas direkt på en enhet som stöder Mac OS. (Om du vill öppna en DLL-fil på Mac OS kan olika externa program hjälpa till att öppna dem.)


## DLL-filformat ##

DLL-filen har utvecklats av Microsoft och har tillägget ".dll" som representerar typen. Det har varit en integrerad del av Windows 1.0-servern och vidare. Det är en binär filtyp och stöds av alla versioner av Microsoft Windows. Denna filtyp skapades för att skapa ett delat bibliotekssystem inom Windows-program, för att möjliggöra separata och oberoende redigeringar eller ändringar i programbiblioteken utan att behöva länka om programmen.


## DLL-exempel ##

Exempelkod för en DLL-ingångspunkt finns nedan:

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

## Referens ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
