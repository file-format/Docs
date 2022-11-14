{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Ulteriori informazioni sul formato del file di backup dei dati di gioco Steam CSD e sulle API.",
  "title" :"Formato file CSD - File di backup dei dati di gioco Steam",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Che cos'è un file CSD?

Un file CSD è un file di backup del gioco generato dal servizio di gioco **Steam** che consente agli utenti di scaricare e gestire i giochi **Valve**. Contiene i dati di backup relativi ai giochi che possono essere utilizzati per ripristinare un gioco eliminato. Steam è in grado di ripristinare il gioco da un file CSD solo se il gioco è stato scaricato, installato e corretto tramite Steam. Per ripristinare il gioco dal file CSD, usa l'opzione di Steam → Backup e ripristino di Gamesteam e seleziona il file.

## Formato file CSD - Ulteriori informazioni

La struttura interna del formato di file CSD non è disponibile pubblicamente e le sue specifiche di formato di file non sono disponibili come riferimento per gli sviluppatori. I file CSD sono accompagnati dai file CSM e ISS che sono anche formati di file di gioco Steam.

### Dove trovare i file di backup di Steam?

Gli interi file di backup di Steam possono essere trovati nelle seguenti posizioni:

* C:\Programmi (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - Configurazioni personalizzate e script di configurazione
* \downloads\ - Contenuti personalizzati per giochi multiplayer
* \maps\ - Mappe personalizzate che sono state installate o scaricate durante le partite multiplayer
* \materials\ - Texture e skin personalizzate
* \SALVA\ - Partite salvate per giocatore singolo

Tuttavia, la posizione dei giochi creati da terze parti può essere diversa ed è determinata dallo sviluppatore del gioco.

### Ripristino dal file di backup CSD

Installa Steam e accedi all'account Steam corretto (consulta Installazione di Steam per ulteriori istruzioni)
* Avvia Steam
* Fai clic su "Steam" nell'angolo in alto a sinistra dell'applicazione Steam
* Seleziona "Backup e ripristino giochi..."
* Seleziona "Ripristina un backup precedente"
* Cerca la posizione dei file di backup del gioco
* Continua attraverso le finestre di Steam per installare i giochi necessari.

## Riferimenti

* [Utilizzo della funzione di backup di Steam](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

