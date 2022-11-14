{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "extension", "fichier", "format", "système", "Dynamic Link Library", "paramètres", "programmes", "ordinateur", "application" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Bibliothèque de liens dynamiques",
  "description":"En savoir plus sur le format de fichier DLL et les API qui peuvent créer et ouvrir des fichiers DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Qu'est-ce qu'un fichier DLL ? ##

Un fichier DLL ou Dynamic Link Library est un type de fichier exécutable. C'est l'un des fichiers d'extension les plus courants sur votre appareil et il est généralement stocké dans le dossier System32 de votre Windows. Le fichier d'extension DLL a été développé par Microsoft et est couramment utilisé par eux. Il a une cote d'utilisateur élevée. La DLL fonctionne comme une étagère qui contient les *pilotes/procédures/fonctions/propriétés* qui sont conçus et appliqués pour un programme/une application par le serveur Windows. Un seul fichier DLL peut également être partagé entre plusieurs programmes Windows. Ces fichiers d'extension sont essentiels au bon fonctionnement des programmes Windows sur votre appareil car ils sont responsables de l'activation et de l'exécution de diverses fonctions sur le programme telles que l'écriture et la lecture de fichiers, la connexion avec d'autres appareils externes à votre configuration.
Cependant, ces fichiers ne peuvent être ouverts que sur un appareil prenant en charge n'importe quelle version de Windows (Windows 7/Windows 10/etc.) et ne peuvent donc pas être ouverts directement sur un appareil prenant en charge Mac OS. (Si vous souhaitez ouvrir un fichier DLL sur Mac OS, diverses applications externes peuvent vous aider à les ouvrir.)


## Format de fichier DLL ##

Le fichier DLL a été développé par Microsoft et porte l'extension ".dll" qui représente le type. Il fait partie intégrante du serveur Windows 1.0 et au-delà. Il s'agit d'un type de fichier binaire pris en charge par toutes les versions de Microsoft Windows. Ce type de fichier a été créé pour créer un système de bibliothèque partagée dans les programmes Windows, afin de permettre des modifications ou des modifications séparées et indépendantes dans les bibliothèques de programmes sans avoir besoin de relier les programmes.


## Exemple de DLL ##

Un exemple de code pour un point d'entrée DLL peut être trouvé ci-dessous :

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

## Référence ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
