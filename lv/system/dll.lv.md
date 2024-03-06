{
  "date": "2021-06-29",
  "keywords": [
"DLL",
"pagarinājumu",
"failu",
"formātā",
"sistēma",
"Dinamiskās saites bibliotēka",
"iestatījumi",
"programmas",
"dators",
"pieteikumu"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DLL — dinamisko saišu bibliotēka",
  "description": "Uzziniet par DLL failu formātu un API, kas var izveidot un atvērt DLL failus.",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dl-lvl"
}
},
  "lastmod": "2021-06-29"
}

## Kas ir DLL fails? ##

DLL fails vai dinamisko saišu bibliotēka ir izpildāmā faila veids. Tas ir viens no visbiežāk atrastajiem paplašinājuma failiem jūsu ierīcē, un tas parasti tiek saglabāts sistēmas Windows mapē System32. DLL paplašinājuma failu izstrādāja Microsoft, un viņi to plaši izmanto. Tam ir augsts popularitātes lietotāju vērtējums. DLL darbojas kā plaukts, kurā ir ietverti *draiveri/procedūras/funkcijas/īpašības*, kuras ir izstrādājis un lietojis programmai/lietojumprogrammai Windows serveris. Vienu DLL failu var arī koplietot starp dažādām Windows programmām. Šie paplašinājumu faili ir ļoti svarīgi Windows programmu vienmērīgai darbībai jūsu ierīcē, jo tie ir atbildīgi par dažādu programmas funkciju iespējošanu un izpildi, piemēram, failu rakstīšanu un lasīšanu, savienojuma izveidi ar citām ierīcēm, kas ir ārpus jūsu iestatīšanas.
Tomēr šos failus var atvērt tikai ierīcē, kas atbalsta jebkuru Windows versiju (Windows 7/windows 10/u.c.), un tāpēc tos nevar atvērt tieši ierīcē, kas atbalsta Mac OS. (Ja vēlaties atvērt DLL failu operētājsistēmā Mac OS, dažādas ārējās lietojumprogrammas var palīdzēt tos atvērt.)


## DLL faila formāts ##

DLL failu izstrādāja Microsoft, un tam ir paplašinājums .dll, kas apzīmē veidu. Tā ir bijusi Windows 1.0 servera un citur neatņemama sastāvdaļa. Tas ir binārais faila tips, un to atbalsta visas Microsoft Windows versijas. Šis faila tips tika izveidots, lai izveidotu koplietojamu bibliotēku sistēmu Windows programmās, lai varētu veikt atsevišķus un neatkarīgus labojumus vai izmaiņas programmu bibliotēkās bez nepieciešamības atkārtoti saistīt programmas.


## DLL piemērs ##

DLL ieejas punkta koda piemēru var atrast zemāk:

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

## Atsauce Nr.

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
