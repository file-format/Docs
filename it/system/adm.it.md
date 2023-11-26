{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ADM - Formato file modello amministrativo",
  "description":"Scopri il formato file ADM e come aprire i file ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Cos'è un file ADM?

Un file ADM è un file modello utilizzato dal software Microsoft Group Policies per specificare la posizione delle impostazioni dei criteri basati sul registro nel file del registro. Viene utilizzato dagli amministratori di sistema per definire la policy per la gestione di un gruppo di computer che fanno parte del gruppo. Queste informazioni diventano parte degli oggetti Criteri di gruppo (GPO) creati per la gestione del gruppo.

È possibile aprire file ADM utilizzando l'Editor oggetti Criteri di gruppo Microsoft.

## Formato file ADM: ulteriori informazioni

I file ADM vengono archiviati come file di testo in formato Unicode. Questi sono stati utilizzati principalmente per individuare la posizione delle impostazioni dei criteri basati sul registro nel registro di Windows Vista e Windows 7.

I file ADM non sono più supportati e sono stati sostituiti dai file [ADMX](/it/system/admx/). GPA ignora i seguenti file ADM predefiniti sui computer che eseguono Microsoft Windows Vista Service Pack 1 o versione successiva.

* sistema.adm
* inetres.adm
*conf.amm
*wmplayer.adm
*wuau.adm

## Riferimenti

* [File modello amministrativo - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestione dei file modello amministrativi](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

