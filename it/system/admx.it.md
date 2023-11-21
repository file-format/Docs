{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File ADMX - Formato file modello amministrativo Criteri di gruppo",
  "description":"Ulteriori informazioni sul formato file ADMX e su come aprire i file ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Cos'è un file ADMX?

Un file ADMX è un file di configurazione dei criteri utilizzato dal software Criteri di gruppo di Microsoft Windows che gestisce un gruppo di computer in un gruppo. Si tratta di un file modello amministrativo basato su XML ed è stato introdotto con Windows Vista Service Pack 1. I file ADMX contengono impostazioni di configurazione per account utente, configurazioni del sistema operativo e applicazioni. I file ADMX vengono utilizzati per archiviare e distribuire le configurazioni per la gestione centralizzata di molti sistemi informatici.

È possibile creare o modificare file ADMX utilizzando qualsiasi editor di testo compatibile con XML o editor di oggetti Criteri di gruppo Microsoft.

## Formato file ADMX: ulteriori informazioni

I file ADMX sono archiviati nel formato di file universale [XML](/it/web/xml/) leggibile dall'uomo. È un formato file multilingue e consente agli amministratori di sistema di diverse lingue di lavorare con gli stessi file ADMX. I file ADMX hanno sostituito il vecchio formato di file [ADM](/it/system/adm/), che è un formato di file di testo con formattazione Unicode. I file ADMX specificano le chiavi del Registro di sistema che vengono modificate quando viene modificata una determinata impostazione di Criteri di gruppo.

### Cosa posso fare con il file ADMX?

I file ADMX definiscono quali azioni devono essere consentite ai computer degli utenti che fanno parte di un gruppo. La policy di gruppo impone le regole impostate in combinazione con il software Active Directory. I file ADMX vengono gestiti dall'archivio centrale sul sistema operativo Windows che è una posizione centrale nel dominio.

Un file ADMX distribuito in un ambiente di lavoro può consentire agli amministratori di implementare criteri quali:

* Controllare l'uso di Internet
* Download di determinati tipi di file
* Utilizzo di dispositivi rimovibili sui sistemi

## Riferimenti

* [File modello amministrativo - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gestione dei file modello amministrativi](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

