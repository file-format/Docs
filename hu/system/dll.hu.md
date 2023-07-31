{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "kiterjesztés", "fájl", "formátum", "rendszer", "dinamikus hivatkozási könyvtár", "beállítások", "programok", "számítógép", "alkalmazás" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Dynamic Link Library",
  "description":"További információ a DLL fájlformátumról és az API-król, amelyek DLL-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Mi az a DLL fájl? ##

A DLL-fájl vagy a Dynamic Link Library egy végrehajtható fájltípus. Ez az egyik leggyakrabban megtalálható kiterjesztési fájl az eszközén, és általában a Windows System32 mappájában található. A DLL kiterjesztésű fájlt a Microsoft fejlesztette ki, és népszerűen használják. Nagy népszerűségnek örvend a felhasználók körében. A DLL polcként működik, amely tartalmazza a Windows szerver által egy programhoz/alkalmazáshoz tervezett és alkalmazott *illesztőprogramokat/eljárásokat/funkciókat/tulajdonságokat*. Egyetlen DLL fájl is megosztható a különböző Windows programok között. Ezek a kiterjesztési fájlok létfontosságúak a Windows-programok zökkenőmentes működéséhez az eszközön, mivel ezek felelősek a program különféle funkcióinak engedélyezéséért és futtatásáért, például fájlok írásáért és olvasásáért, valamint más, a telepítésen kívüli eszközökhöz való csatlakozásért.
Ezeket a fájlokat azonban csak olyan eszközön lehet megnyitni, amely támogatja a Windows bármely verzióját (windows 7/windows 10/stb.), ezért nem nyithatók meg közvetlenül olyan eszközön, amely támogatja a Mac OS rendszert. (Ha meg szeretne nyitni egy DLL fájlt Mac OS rendszeren, különféle külső alkalmazások segíthetnek a megnyitásban.)


## DLL fájl formátum ##

A DLL fájlt a Microsoft fejlesztette ki, és a „.dll” kiterjesztéssel rendelkezik, amely a típust jelöli. A Windows 1.0 kiszolgáló és azon túl is szerves része volt. Ez egy bináris fájltípus, és a Microsoft Windows összes verziója támogatja. Ezt a fájltípust azért hozták létre, hogy megosztott könyvtári rendszert hozzanak létre a Windows programokon belül, hogy lehetővé tegyék a programkönyvtárak különálló és független szerkesztését vagy módosítását anélkül, hogy a programokat újra kellene csatolni.


## DLL példa ##

Példakód egy DLL belépési ponthoz az alábbiakban található:

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

## Hivatkozási szám

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
