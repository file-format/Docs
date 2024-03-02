{
  "date": "2021-06-29",
  "keywords": [
"DLL",
"síneadh",
"comhad",
"formáid",
"córas",
"Leabharlann Nasc Dinimiciúla",
"socruithe",
"cláir",
"ríomhaire",
"iarratas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DLL - Leabharlann Nasc Dinimiciúla",
  "description": "Foghlaim faoi fhormáid comhaid DLL agus APIs ar féidir leo comhaid DLL a chruthú agus a oscailt.",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dl-gal"
}
},
  "lastmod": "2021-06-29"
}

## Cad is comhad dll ann? ##

Is cineál comhaid inrite é comhad DLL nó Leabharlann Nasc Dinimiciúla. Tá sé ar cheann de na comhaid síntí is coitianta a aimsítear ar do ghléas agus de ghnáth stóráiltear é san fhillteán System32 ar do Windows. D'fhorbair Microsoft an comhad síneadh DLL agus úsáideann siad go coitianta é. Tá rátáil úsáideora ard-tóir air. Oibríonn an dll mar sheilf ina bhfuil na *tiománaithe/nósanna imeachta/feidhmeanna/airíonna* a dhear agus a chuireann an freastalaí fuinneoga isteach ar chlár/iarratas. Is féidir comhad dll amháin a roinnt freisin i measc na gclár fuinneoga éagsúla. Tá na comhaid síntí seo ríthábhachtach chun cláir Windows a reáchtáil go réidh ar do ghléas mar go bhfuil siad freagrach as feidhmeanna éagsúla a chumasú agus a rith ar an gclár, mar shampla comhaid a scríobh agus a léamh, a nascadh le gléasanna eile atá lasmuigh de do shocrú.
Ní féidir na Comhaid seo a oscailt, áfach, ach ar ghléas a thacaíonn le haon leagan de Windows (fuinneoga 7/fuinneoga 10/etc.) agus mar sin ní féidir iad a oscailt go díreach ar ghléas a thacaíonn le Mac OS. (Más mian leat comhad DLL a oscailt ar Mac OS, is féidir le feidhmchláir sheachtracha éagsúla cabhrú leo iad a oscailt.)


## Formáid Chomhaid DLL ##

D'fhorbair Microsoft an comhad dll agus tá an síneadh .dll ann a sheasann don chineál. Bhí sé mar chuid lárnach de fhreastalaí Windows 1.0, agus ina dhiaidh sin. Is cineál comhaid dhénártha é agus tá gach leagan de Microsoft Windows tacaithe aige. Cruthaíodh an cineál comhaid seo mar mhodh chun córas leabharlainne roinnte a chruthú laistigh de chláir Windows, chun athruithe nó athruithe ar leith agus neamhspleácha a cheadú sna leabharlanna clár gan gá leis na cláir a athnascadh.


## DLL Sampla ##

Is féidir cód samplach do phointe iontrála dll a fháil thíos:

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

## Tagairt ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
