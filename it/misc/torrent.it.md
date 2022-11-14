{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file torrent - File BitTorrent",
  "description":"Scopri i file TORRENT e le API che possono creare e aprire file TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Che cos'è un file TORRENT?

Un file TORRENT è un file di testo utilizzato da BitTorrent e altri programmi P2P (peer-to-peer) per il download e lo scambio di contenuti. Il contenuto scaricabile può includere documenti, video, giochi, film e altri media disponibili su Internet. Include informazioni sui metadati sui contenuti e sulla posizione dei media da scaricare. Software come BitTorrent utilizza le informazioni da questo file come il nome, la dimensione del file e la struttura delle cartelle per il download dei dati. I file torrent possono essere convertiti in altri formati di file come [PDF](/it/pdf/) online.

## Che cos'è il torrent? Il formato di file TORRENT per lo scambio di dati

Il torrenting è il concetto di scambio (download e upload) di file di dati utilizzando la rete BitTorrent. A differenza dei server convenzionali in cui i dati vengono caricati per consentire ad altri di accedervi e scaricarli, i file torrent vengono recuperati e inviati utilizzando la rete torrent. Quando un utente apre un file .torrent in applicazioni come BitTorrent, il software inizia a scaricare il contenuto del file bit a bit. Se più utenti hanno lo stesso file, BitTorrent divide i download tra tutti gli utenti per accelerare il processo di download. Allo stesso tempo, il computer dell'utente che sta scaricando il file, diventa anche la fonte del file per inviarlo ad altri utenti che stanno scaricando lo stesso file.

### Struttura di un file TORRENT

Un file torrent è una combinazione di un elenco di file e informazioni sui metadati su tutte le parti del file da scaricare. Contiene le seguenti informazioni sotto forma di chiavi.

- `announce` — L'URL del tracker che viene annunciato ad altri peer per informare sulla disponibilità del file
- `info` — Esegue il mapping a un dizionario le cui chiavi dipendono dal fatto che uno o più file siano condivisi:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — dimensione del file in byte.
- `percorso` — un elenco di stringhe corrispondenti ai nomi delle sottodirectory, l'ultima delle quali è il nome del file effettivo
- `length` — la dimensione del file in byte (solo quando un file viene condiviso)
- `name` — il nome del file in cui deve essere salvato il file
- `lunghezza pezzo` — numero di byte per pezzo. Questo è comunemente 28 KiB = 256 KiB = 262.144 B.
- `pieces` — una lista hash che è una concatenazione dell'hash SHA-1 di ogni pezzo.

## Il torrenting è sicuro e legale?

Il protocollo di torrent per lo scambio di dati tra utenti P2P è sicuro in quanto è solo il mezzo per condividere qualsiasi tipo di file. Pertanto, il protocollo stesso non è pericoloso o illegale. Tuttavia, il contenuto condiviso tramite la rete può contenere file o media che possono violare lo stato legale dei documenti condivisi. In tal caso, lo scambio di tali dati può comportare azioni legali contro le parti coinvolte nella condivisione di tali file pubblicamente.

## Riferimenti

* [File TORRENT - wikipedia](https://en.wikipedia.org/wiki/File_Torrent)

