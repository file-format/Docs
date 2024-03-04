{
  "date": "2021-06-29",
  "keywords": [
"DLL",
"pratęsimas",
"failą",
"formatu",
"sistema",
"Dinaminių nuorodų biblioteka",
"nustatymus",
"programas",
"kompiuteris",
"taikymas"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DLL – dinaminių saitų biblioteka",
  "description": "Sužinokite apie DLL failo formatą ir API, kurios gali kurti ir atidaryti DLL failus.",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dl-ltl"
}
},
  "lastmod": "2021-06-29"
}

## Kas yra DLL failas? ##

DLL failas arba dinaminių nuorodų biblioteka yra vykdomojo failo tipas. Tai vienas iš dažniausiai aptinkamų plėtinių failų jūsų įrenginyje ir paprastai saugomas Windows aplanke System32. DLL plėtinio failą sukūrė Microsoft ir jie plačiai naudoja. Jis turi aukštą populiarumo vartotojų įvertinimą. DLL veikia kaip lentyna, kurioje yra *tvarkyklės/procedūros/funkcijos/ypatybės*, kurios yra sukurtos ir pritaikytos programai / programai Windows serverio. Vienas DLL failas taip pat gali būti bendrinamas tarp įvairių Windows programų. Šie plėtinių failai yra labai svarbūs sklandžiam Windows programų veikimui jūsų įrenginyje, nes jie yra atsakingi už įvairių programos funkcijų, pvz., failų rašymo ir skaitymo, prisijungimą prie kitų įrenginių, kurie yra išoriniai jūsų sąrankoje, įgalinimą ir vykdymą.
Tačiau šiuos failus galima atidaryti tik įrenginyje, kuris palaiko bet kurią Windows versiją (Windows 7 / Windows 10 ir kt.), todėl jų negalima atidaryti tiesiogiai įrenginyje, kuris palaiko Mac OS. (Jei norite atidaryti DLL failą Mac OS, įvairios išorinės programos gali padėti juos atidaryti.)


## DLL failo formatas ##

DLL failą sukūrė Microsoft ir turi plėtinį .dll, kuris nurodo tipą. Tai buvo neatskiriama Windows 1.0 serverio dalis ir ne tik. Tai dvejetainis failo tipas, kurį palaiko visos Microsoft Windows versijos. Šis failo tipas buvo sukurtas kaip priemonė sukurti bendrai naudojamų bibliotekų sistemą Windows programose, kad būtų galima atskirai ir nepriklausomai redaguoti arba keisti programų bibliotekas, nereikia iš naujo susieti programų.


## DLL pavyzdys Nr.

DLL įėjimo taško kodo pavyzdį galite rasti žemiau:

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

## Nuoroda ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
