{
  "date": "2021-06-29",
  "keywords": [
"DLL",
"udvidelse",
"fil",
"format",
"system",
"Dynamisk linkbibliotek",
"indstillinger",
"programmer",
"computer",
"Ansøgning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DLL - Dynamic Link Library",
  "description": "Lær om DLL-filformat og API'er, der kan oprette og åbne DLL-filer.",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dl-dal"
}
},
  "lastmod": "2021-06-29"
}

## Hvad er en DLL-fil? ##

En DLL-fil eller Dynamic Link Library er en type eksekverbar fil. Det er en af de mest almindeligt fundne udvidelsesfiler på din enhed og er normalt gemt i System32-mappen på din Windows. DLL-udvidelsesfilen blev udviklet af Microsoft og er populært brugt af dem. Det har en høj popularitet brugervurdering. DLL'en fungerer som en hylde, der indeholder *drivere/procedurer/funktioner/egenskaber*, der er designet og anvendt til et program/applikation af Windows-serveren. En enkelt DLL-fil kan også deles mellem forskellige Windows-programmer. Disse udvidelsesfiler er afgørende for den glatte afvikling af Windows-programmer på din enhed, da de er ansvarlige for at aktivere og køre forskellige funktioner på programmet, såsom at skrive og læse filer, oprette forbindelse til andre enheder, der er eksterne til din opsætning.
Disse filer kan dog kun åbnes på en enhed, der understøtter enhver version af Windows (windows 7/windows 10/osv.) og kan derfor ikke åbnes direkte på en enhed, der understøtter Mac OS. (Hvis du vil åbne en DLL-fil på Mac OS, kan forskellige eksterne programmer hjælpe med at åbne dem.)


## DLL-filformat ##

DLL-filen er udviklet af Microsoft og har filtypenavnet .dll, der repræsenterer typen. Det har været en integreret del af Windows 1.0-serveren og videre. Det er en binær filtype og understøttes af alle versioner af Microsoft Windows. Denne filtype blev oprettet som et middel til at skabe et delt bibliotekssystem i Windows-programmer, for at tillade separate og uafhængige redigeringer eller ændringer i programbibliotekerne uden behov for at gen-linke programmerne.


## DLL-eksempel ##

Eksempelkode for et DLL-indgangspunkt kan findes nedenfor:

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

## Reference ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
