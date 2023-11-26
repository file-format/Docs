{
"data": "08-06-2023",
  "keywords": [
"file CRX",
"cos'è un file crx",
"come installare il file crx in Google Chrome",
"come aprire il file CRX",
"cosa contiene il file crx",
"qual è il formato del file crx",
"file",
"estensione file CRX",
"estensione"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file CRX - Estensione Google Chrome",
  "description":"Informazioni sul formato CRX e sulle API in grado di creare e aprire file CRX.",
"titolo collegamento": "CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
"parent": "varie"
}
},
"lastmod": "2023-06-08"
}

## Cos'è un file CRX?

Il formato file CRX è associato alle estensioni del browser Google Chrome. Un file CRX è essenzialmente un pacchetto compresso contenente i file e i metadati necessari per l'installazione e l'esecuzione di un'estensione in Google Chrome. Migliora la funzionalità o l'aspetto di un browser Web fornendo una funzionalità o un tema extra.

Quando un file CRX viene scaricato e installato in Google Chrome, il browser verifica l'integrità dell'estensione utilizzando la chiave pubblica e la firma. Se la verifica ha esito positivo, Chrome estrae il contenuto del file CRX e installa l'estensione, rendendola disponibile per l'uso. Gli utenti possono gestire le proprie estensioni tramite la pagina Estensioni di Chrome, che consente di abilitare, disabilitare o rimuovere le estensioni installate.

## Come installare il file CRX in Google Chrome?

Per installare un file CRX in Google Chrome, puoi seguire questi passaggi:

1. Apri il browser Chrome.
2. Digita "chrome://extensions" nella barra degli indirizzi e premi Invio.
3. Abilita l'interruttore a levetta "Modalità sviluppatore" situato nell'angolo in alto a destra della pagina Estensioni.
4. Fare clic sul pulsante "Carica non imballato".
5. Individua e seleziona la cartella contenente i contenuti estratti del file CRX (o seleziona semplicemente il file CRX stesso).
6. Fai clic su "Apri" per installare l'estensione.

## Cosa contiene il file CRX?

Un file CRX contiene i file e i metadati necessari richiesti per l'estensione Google Chrome. Ecco una ripartizione dei contenuti tipici trovati all'interno di un file CRX:

- **File manifest (manifest.json):** questo file è un file in formato JSON che include informazioni sull'estensione come nome, versione, descrizione, autorizzazioni e script in background. Definisce la struttura e il comportamento dell'estensione.
- **File JavaScript:** questi file contengono il codice che definisce la funzionalità dell'estensione. Possono includere script per la gestione di eventi, la modifica di pagine Web o l'interazione con le API di Chrome.
- **HTML, CSS e file di immagine:** le estensioni spesso includono elementi dell'interfaccia utente, come finestre popup o pagine di opzioni. I file HTML definiscono la struttura di queste interfacce, mentre i file CSS ne controllano l'aspetto. I file di immagine vengono utilizzati per icone o altre risorse grafiche.
- **File di risorse facoltativi:** le estensioni possono includere risorse aggiuntive, come file di localizzazione per il supporto di più lingue. Questi file contengono traduzioni del testo utilizzato nell'interfaccia utente dell'estensione.
- **Script in background:** se un'estensione dispone di processi in background o script che vengono eseguiti indipendentemente dalla pagina Web attiva, questi script verranno inclusi nel file CRX.
- **Script di contenuto:** Gli script di contenuto sono script che possono essere inseriti nelle pagine Web per modificarne il comportamento o interagire con il contenuto. Se l'estensione utilizza script di contenuto, i file necessari per tali script saranno presenti nel file CRX.
- **Altre risorse:** A seconda dei requisiti specifici dell'estensione, potrebbero essere inclusi file aggiuntivi come file audio o video, caratteri o file di dati.

Il formato file CRX è essenzialmente un pacchetto compresso che contiene tutti questi file e cartelle in modo strutturato. Quando il file CRX è installato in Google Chrome, il browser estrae i contenuti e li inserisce nelle posizioni appropriate, consentendo il caricamento e l'esecuzione dell'estensione nel browser.

## Qual è il formato del file CRX?

Il formato file CRX è un formato specifico per il confezionamento e la distribuzione delle estensioni di Google Chrome. È essenzialmente un archivio ZIP compresso con estensione di file diversa. La struttura di base del file CRX è la seguente:

- **Firma del file:** I primi 4 byte del file contengono il numero magico "Cr24" (esadecimale: 43 72 32 34) che serve come firma per identificare il file come file CRX.
- **Numero di versione:** I successivi 4 byte rappresentano il numero di versione del formato CRX.
- **Lunghezza chiave pubblica:** I seguenti 4 byte indicano la lunghezza della chiave pubblica codificata utilizzata per la verifica della firma dell'estensione.
- **Lunghezza della firma:** I 4 byte successivi specificano la lunghezza della firma dell'estensione.
- **Chiave pubblica:** questa sezione contiene la chiave pubblica codificata utilizzata per verificare l'integrità dell'estensione.
- **Firma:** questa sezione contiene la firma dell'estensione, che viene generata firmando i contenuti dell'estensione utilizzando una chiave privata corrispondente alla chiave pubblica menzionata sopra.
- **Archivio ZIP:** i restanti byte del file CRX comprendono un archivio ZIP compresso. Questo archivio contiene tutti i file e le cartelle di estensione necessari, inclusi file manifest, file JavaScript, file HTML, file CSS, immagini e qualsiasi altra risorsa.

## Riferimenti
* [Specifica del formato CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

