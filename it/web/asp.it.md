{
  "date" : "2019-10-11",
  "keywords" :[ "asp","file asp", "formato di file asp", "tipo di file asp", "file", "tipo", "che cos'è un file asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Formato file Active Server Pages",
  "description" :"Scopri cos'è un file ASP e le API che possono crearli e aprirli.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file ASP?

ASP sta per Active Server Pages che è un framework di sviluppo per la creazione di pagine web. Consente al codice del computer di essere eseguito da un server interno per soddisfare le richieste web. Quando viene generata una richiesta per un file ASP dal browser web, il server legge il file ed esegue qualsiasi codice/script al suo interno per generare il risultato **[HTML](/it/web/html/)** che viene restituito al browser per la visualizzazione.

A differenza delle pagine HTML, che sono pagine statiche servite dal server, i file ASP generano contenuti dinamici in fase di esecuzione che possono comportare richieste di dati da un database. Le pagine ASP in genere utilizzano l'estensione .asp anziché .html. Poiché il codice/script all'interno di un file ASP viene eseguito sul lato server, il browser richiedente non può vedere il codice utilizzato per creare la pagina servita. Tutti i browser moderni sono in grado di visualizzare le pagine generate come risultato. Essendo basate sulla tecnologia Microsoft, le pagine create con ASP sono ospitate su server Microsoft Internet Information Services (IIS).

## Breve storia del formato di file ASP
ASP ha subito solo poche revisioni ed è stato sostituito da ASP.NET che è un modo più moderno ed efficiente di sviluppare e gestire le pagine lato server. Il supporto per ASP è incluso per impostazione predefinita insieme a Internet Information Services (IIS). ASP è stato pubblicato in tre diverse versioni con miglioramenti in ciascuna.

* ASP 1.0 è stato rilasciato nel dicembre 1996 come parte di IIS 3.0
* ASP 2.0 è stato rilasciato nel settembre 1997 come parte di IIS 4.0
* ASP 3.0 è stato rilasciato nel novembre 2000 come parte di IIS 5.0

## Oggetti funzionali ASP

I file ASP utilizzano oggetti lato server per elaborare le richieste degli utenti e generare pagine di output da servire agli utenti. Ogni oggetto ha un insieme di raccolte, proprietà e metodi per elaborare richieste e risposte. Questi oggetti includono:

### Richiedi oggetto

Quando un browser richiede una pagina da un server, viene chiamata richiesta. L'oggetto Richiesta viene utilizzato per ottenere informazioni da un visitatore.

### Oggetto di risposta

L'oggetto ASP Response viene utilizzato per inviare l'output all'utente dal server.

### Oggetto Server

L'oggetto ASP Server viene utilizzato per accedere a proprietà e metodi sul server. Consente le connessioni a database (ADO), filesystem e l'uso di componenti installati sul server.

### Oggetto Sessione

Un oggetto sessione è come un collegamento tra il browser dell'utente che richiede una pagina dal server e il server stesso. Ciò è ottenuto da un cookie creato da ASP e inviato al computer dell'utente. L'oggetto Session memorizza informazioni o modifica le impostazioni per una sessione utente. Le informazioni memorizzate in un oggetto Session sono condivise su tutte le pagine di un'applicazione. Le informazioni comuni memorizzate nelle variabili di sessione sono nome, ID e preferenze. Il server crea un nuovo oggetto Session per ogni nuovo utente e distrugge l'oggetto Session alla scadenza della sessione.

### Oggetto applicazione

L'oggetto Applicazione contiene informazioni che verranno utilizzate da molte pagine dell'applicazione (come le informazioni sulla connessione al database). Le informazioni sono accessibili da qualsiasi pagina. Le informazioni possono anche essere modificate in un'unica posizione e le modifiche si rifletteranno automaticamente su tutte le pagine. L'oggetto Application viene utilizzato per memorizzare e accedere alle variabili da qualsiasi pagina, proprio come l'oggetto Session.

### Oggetto ASPError

L'oggetto ASPError è stato implementato in ASP 3.0 ed è disponibile in IIS5 e versioni successive. L'oggetto ASPError viene utilizzato per visualizzare informazioni dettagliate su qualsiasi errore che si verifica negli script in una pagina ASP.

**Nota:** L'oggetto ASPError viene creato quando viene chiamato Server.GetLastError, quindi è possibile accedere alle informazioni sull'errore solo utilizzando il metodo Server.GetLastError.

## Riferimenti

* [ASP - Da W3C](https://www.w3schools.com/asp/default.asp)
* [Creazione di pagine ASP semplici](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

