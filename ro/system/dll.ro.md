{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "extensie", "fișier", "format", "sistem", "Biblioteca de linkuri dinamice", "setări", "programe", "calculator", "aplicație"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL – Biblioteca de linkuri dinamice",
  "description":"Aflați despre formatul de fișier DLL și despre API-urile care pot crea și deschide fișiere DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier DLL? ##

Un fișier DLL sau Dynamic Link Library este un tip de fișier executabil. Este unul dintre fișierele de extensie cel mai frecvent găsite pe dispozitivul dvs. și este de obicei stocat în folderul System32 de pe Windows. Fișierul cu extensia DLL a fost dezvoltat de Microsoft și este folosit în mod popular de către aceștia. Are o popularitate ridicată a utilizatorilor. DLL-ul funcționează ca un raft care conține *driverele/procedurile/funcțiile/proprietățile* care sunt proiectate și aplicate pentru un program/aplicație de către serverul Windows. Un singur fișier DLL poate fi, de asemenea, partajat între diferite programe Windows. Aceste fișiere de extensie sunt vitale pentru buna funcționare a programelor Windows pe dispozitivul dvs., deoarece sunt responsabile pentru activarea și rularea diferitelor funcții ale programului, cum ar fi scrierea și citirea fișierelor, conectarea cu alte dispozitive care sunt externe configurației dvs.
Cu toate acestea, aceste fișiere pot fi deschise numai pe un dispozitiv care acceptă orice versiune de Windows (windows 7/windows 10/etc.) și, prin urmare, nu pot fi deschise direct pe un dispozitiv care acceptă Mac OS. (Dacă doriți să deschideți un fișier DLL pe Mac OS, diverse aplicații externe vă pot ajuta să le deschideți.)


## Format de fișier DLL ##

Fișierul DLL a fost dezvoltat de Microsoft și are extensia „.dll” care reprezintă tipul. A fost o parte integrantă a serverului Windows 1.0 și nu numai. Este un tip de fișier binar și este acceptat de toate versiunile de Microsoft Windows. Acest tip de fișier a fost creat ca mijloc de a crea un sistem de bibliotecă partajată în cadrul programelor Windows, pentru a permite editări sau modificări separate și independente în bibliotecile de programe fără a fi nevoie să reconectați programele.


## Exemplu DLL ##

Exemplu de cod pentru un punct de intrare DLL poate fi găsit mai jos:

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

## Referință ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
