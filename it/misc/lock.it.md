{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file LOCK - Che cos'è un file Lock?",
  "description":"Scopri il formato di file LOCK e il suo .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Che cos'è un file LOCK?

Un file **LOCK** è un file rinominato utilizzato da applicazioni e sistemi operativi per contrassegnare un file o un dispositivo come bloccato. Questo indica ad altre applicazioni di non utilizzare il file a meno che non sia libero dall'applicazione che lo sta utilizzando. Nella maggior parte dei casi, questi file di blocco sono vuoti, ma in altri casi possono contenere informazioni relative al blocco come proprietà e impostazioni.

A volte, il file .lock viene utilizzato da .NET Framework di Microsoft per creare copie **bloccate** di un file di database. In tal caso, si aprirà una copia del file di database con estensione .lock. Ciò non consente all'utente di apportare modifiche al file mentre è in uso da un altro utente.

## LOCK Formato file - Ulteriori informazioni

Un file LOCK viene creato da ciascuna applicazione e il suo formato file è specifico per l'applicazione. Questi file di blocco possono essere salvati sia in formato file di testo che binario.

La presenza di file di blocco impedisce l'accesso simultaneo di una risorsa a più file che tentano di accedere a tale risorsa. Viene creata una copia del file originale con estensione .lock suffisso al suo nome. Questo indica ad altre applicazioni di avere accesso in sola lettura al file. Ad esempio, risorsa.dat diventerà risorsa.data.lock.

Per il linguaggio di programmazione Ruby, potresti imbatterti nel file **gemfile.lock**. È qui che Bundler tiene traccia delle versioni esatte che sono state installate. Pertanto, quando un progetto/libreria viene spostato su un'altra macchina, il bundle in esecuzione cercherà nel Gemfile l'esatta versione pertinente.

## Blocca file in Linux

Linux supporta due tipi di blocchi di file: blocchi di avviso e blocchi obbligatori.

* **Advisory Locks**: tipo di blocco non applicato. In questo caso, i processi partecipanti cooperano tra loro acquisendo lock in modo esplicito. Se ciò non è possibile, i blocchi di avviso vengono ignorati.

* **Blocchi obbligatori**: in caso di blocco obbligatorio, il sistema operativo impone il blocco del file impedendo ad altri processi di leggere o scrivere il file. Ciò non richiede alcuna cooperazione tra i processi.

la chiusura obbligatoria non richiede alcuna collaborazione tra i processi partecipanti. Una volta attivato un blocco obbligatorio su un file, il sistema operativo impedisce ad altri processi di leggere o scrivere il file.

## Riferimenti

* [GemFile e Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Blocco in Linux](https://www.baeldung.com/linux/file-locking)

