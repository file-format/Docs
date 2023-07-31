{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "Erweiterung", "Datei", "Format", "System", "Dynamic Link Library", "Einstellungen", "Programme", "Computer", "Anwendung" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Dynamic Link Library",
  "description":"Erfahren Sie mehr über das DLL-Dateiformat und APIs, die DLL-Dateien erstellen und öffnen können.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Was ist eine DLL-Datei? ##

Eine DLL-Datei oder Dynamic Link Library ist eine Art ausführbare Datei. Es ist eine der am häufigsten gefundenen Erweiterungsdateien auf Ihrem Gerät und wird normalerweise im System32-Ordner auf Ihrem Windows gespeichert. Die DLL-Erweiterungsdatei wurde von Microsoft entwickelt und wird häufig von ihnen verwendet. Es hat eine hohe Popularität der Benutzerbewertung. Die DLL fungiert als Regal, das die *Treiber/Prozeduren/Funktionen/Eigenschaften* enthält, die vom Windows-Server für ein Programm/eine Anwendung entworfen und angewendet werden. Eine einzelne DLL-Datei kann auch von verschiedenen Windows-Programmen gemeinsam genutzt werden. Diese Erweiterungsdateien sind für das reibungslose Ausführen von Windows-Programmen auf Ihrem Gerät von entscheidender Bedeutung, da sie für das Aktivieren und Ausführen verschiedener Funktionen des Programms verantwortlich sind, z. B. das Schreiben und Lesen von Dateien und die Verbindung mit anderen Geräten, die sich außerhalb Ihres Setups befinden.
Diese Dateien können jedoch nur auf einem Gerät geöffnet werden, das eine beliebige Version von Windows (Windows 7/Windows 10/etc.) unterstützt, und können daher nicht direkt auf einem Gerät geöffnet werden, das Mac OS unterstützt. (Wenn Sie eine DLL-Datei unter Mac OS öffnen möchten, können verschiedene externe Anwendungen beim Öffnen helfen.)


## DLL-Dateiformat ##

DLL-Datei wurde von Microsoft entwickelt und hat die Erweiterung ".dll", die den Typ darstellt. Es war ein integraler Bestandteil des Windows 1.0-Servers und darüber hinaus. Es ist ein binärer Dateityp und wird von allen Versionen von Microsoft Windows unterstützt. Dieser Dateityp wurde erstellt, um ein gemeinsam genutztes Bibliothekssystem innerhalb von Windows-Programmen zu erstellen, um separate und unabhängige Bearbeitungen oder Änderungen in den Programmbibliotheken zu ermöglichen, ohne dass die Programme neu verknüpft werden müssen.


## DLL-Beispiel ##

Beispielcode für einen DLL-Einstiegspunkt finden Sie unten:

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

## Bezug ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
