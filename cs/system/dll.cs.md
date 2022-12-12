{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "rozšíření", "soubor", "formát", "systém", "Dynamic Link Library", "nastavení", "programy", "počítač", "aplikace" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL – dynamická knihovna odkazů",
  "description":"Další informace o formátu souborů DLL a rozhraních API, která mohou vytvářet a otevírat soubory DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor DLL? ##

Soubor DLL nebo dynamická knihovna je typ spustitelného souboru. Je to jeden z nejčastěji nalezených souborů rozšíření na vašem zařízení a je obvykle uložen ve složce System32 ve vašem Windows. Soubor rozšíření DLL byl vyvinut společností Microsoft a je jím s oblibou používán. Má vysokou oblíbenost uživatelů. DLL funguje jako police, která obsahuje *ovladače/procedury/funkce/vlastnosti*, které jsou navrženy a použity pro program/aplikaci serverem Windows. Jeden soubor DLL lze také sdílet mezi různými programy systému Windows. Tyto soubory rozšíření jsou životně důležité pro bezproblémový chod programů Windows na vašem zařízení, protože jsou zodpovědné za povolení a spouštění různých funkcí v programu, jako je zápis a čtení souborů, připojení k dalším zařízením, která jsou mimo vaše nastavení.
Tyto soubory však lze otevřít pouze na zařízení, které podporuje jakoukoli verzi Windows (Windows 7/Windows 10/atd.), a nelze je tedy otevřít přímo na zařízení, které podporuje Mac OS. (Pokud chcete otevřít soubor DLL v systému Mac OS, mohou vám s jeho otevřením pomoci různé externí aplikace.)


## Formát souboru DLL ##

DLL soubor byl vyvinut společností Microsoft a má příponu ".dll", která představuje typ. Byl nedílnou součástí serveru Windows 1.0 i mimo něj. Je to binární typ souboru a je podporován všemi verzemi Microsoft Windows. Tento typ souboru byl vytvořen jako prostředek k vytvoření systému sdílených knihoven v rámci programů Windows, aby bylo možné provádět samostatné a nezávislé úpravy nebo změny v knihovnách programů bez nutnosti opětovného propojování programů.


## DLL příklad ##

Příklad kódu pro vstupní bod DLL lze nalézt níže:

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

## reference ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
