{
  "date" : "2021-06-30",
  "keywords" :[ "file mst", "formato file mst", "cos'è un file mst", "file", "esempio mst", "estensione file mst", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file MST e le API che possono creare e aprire file MST.",
  "title" :"MST - File del pacchetto di Windows Installer",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Che cos'è un file MST?
I file con estensione .mst vengono utilizzati per trasformare il contenuto di un pacchetto MSI. Sono comunemente usati dagli amministratori di sistema per applicare le impostazioni personalizzate a un file MSI esistente. I file MST vengono utilizzati insieme al pacchetto MSI originale nei loro sistemi di distribuzione software come i criteri di gruppo. I file MST vengono generalmente utilizzati nello sviluppo e nel test del software per la configurazione delle versioni in fase di sviluppo del software.

## Formato file MST
Un file MST o Transform viene utilizzato per raccogliere le opzioni di installazione per i programmi che utilizzano Microsoft Windows Installer in un file. Questi file vengono comunemente utilizzati nella riga di comando del programma di installazione (MSIEXEC.EXE) o utilizzati in un criterio di gruppo dell'installazione del software; in un dominio Microsoft Active Directory. I file MST possono essere utilizzati anche con programmi di installazione eseguibili racchiusi. Un caso generale è che qualcuno vuole passare i parametri della riga di comando al programma di installazione avvolto. Per fare ciò è necessario un file MST che aggiunga la proprietà WRAPPED_ARGUMENTS alla tabella delle proprietà. Questi file non possono essere creati o modificati utilizzando editor generali. A tale scopo sono disponibili strumenti specifici.

### Come utilizzare i file MST?
I file MST possono essere generati utilizzando vari strumenti e Ocra viene generalmente utilizzato per generare file MST. Quindi le impostazioni possono essere personalizzate in base alle necessità e salvarle in una posizione specifica. Successivamente i file MST possono essere utilizzati insieme ai file MSI. Se vuoi testare questi file; utilizzare la seguente sintassi sulla riga di comando

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### TRANSFORMS proprietà

Puoi anche utilizzare la proprietà **TRANSFORMS** del programma di installazione di Windows che è in realtà un elenco delle trasformazioni che il programma di installazione applica durante l'installazione del pacchetto. Il programma di installazione esegue le trasformazioni nello stesso ordine in cui sono elencate nella proprietà TRANSFORM. Le trasformazioni possono essere specificate per nome file con estensione .mst o percorso completo. Per specificare più di una trasformazione, separa ogni nome di file o un punto e virgola come nell'esempio seguente.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Riferimenti

* [File di trasformazione MST](https://www.exemsi.com/documentation/mst-transformation-files/)
* [Proprietà TRANSFORMS](https://docs.microsoft.com/en-us/windows/win32/msi/transforms)


