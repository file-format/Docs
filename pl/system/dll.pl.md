{
  "date" : "2021-06-29",
  "keywords" :["DLL", "rozszerzenie", "plik", "format", "system", "Biblioteka dołączana dynamicznie", "ustawienia", "programy", "komputer", "aplikacja" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL — biblioteka dołączana dynamicznie",
  "description":"Poznaj format plików DLL i interfejsy API, które mogą tworzyć i otwierać pliki DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Czym jest plik DLL? ##

Plik DLL lub Dynamic Link Library to rodzaj pliku wykonywalnego. Jest to jeden z najczęściej znajdowanych plików rozszerzeń na twoim urządzeniu i zwykle jest przechowywany w folderze System32 w twoim systemie Windows. Plik rozszerzenia DLL został opracowany przez firmę Microsoft i jest przez nią powszechnie używany. Ma wysoką popularność wśród użytkowników. Biblioteka DLL działa jak półka zawierająca *sterowniki/procedury/funkcje/właściwości* zaprojektowane i zastosowane dla programu/aplikacji przez serwer Windows. Pojedynczy plik DLL może być również współużytkowany przez różne programy Windows. Te pliki rozszerzeń są niezbędne do sprawnego działania programów systemu Windows na urządzeniu, ponieważ są odpowiedzialne za włączanie i uruchamianie różnych funkcji programu, takich jak zapisywanie i odczytywanie plików, łączenie się z innymi urządzeniami zewnętrznymi w stosunku do konfiguracji.
Pliki te można jednak otworzyć tylko na urządzeniu obsługującym dowolną wersję systemu Windows (Windows 7/Windows 10/itp.), a zatem nie można ich otworzyć bezpośrednio na urządzeniu obsługującym system Mac OS. (Jeśli chcesz otworzyć plik DLL w systemie Mac OS, różne aplikacje zewnętrzne mogą pomóc w ich otwarciu).


## Format pliku DLL ##

Plik DLL został opracowany przez Microsoft i ma rozszerzenie ".dll", które reprezentuje typ. Jest integralną częścią serwera Windows 1.0 i nie tylko. Jest to plik binarny i jest obsługiwany przez wszystkie wersje systemu Microsoft Windows. Ten typ pliku został stworzony w celu stworzenia systemu bibliotek współdzielonych w programach Windows, aby umożliwić oddzielne i niezależne edycje lub zmiany w bibliotekach programów bez konieczności ponownego łączenia programów.


## DLL Przykład ##

Przykładowy kod punktu wejścia biblioteki DLL można znaleźć poniżej:

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

## Odniesienie ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
