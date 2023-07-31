{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "estensione", "file udl", "formato file udl", "Tipo file database", "Formato file database", "che cos'è un file udl" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file UDL e le API che possono creare e aprire file UDL.",
  "title" :"UDL - File di collegamento dati universale Microsoft",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Che cos'è un file UDL?
Il file con estensione .udl è chiamato file Microsoft Universal Data Link; specificando gli attributi di connessione; utilizzato dalle app di Windows per stabilire una connessione con il database. Il file UDL contiene la stringa di connessione per un'origine dati OLE DB; con nome utente e password e proprietà essenziali della stringa di connessione. Per evitare di specificare direttamente le proprietà manualmente in una stringa di connessione, è possibile utilizzare una finestra di dialogo Proprietà collegamento dati per salvare le informazioni di connessione in un file .udl in alternativa.

## Formato file UDL
Fondamentalmente, un file UDL (Universal Data Link) è un semplice file di testo che consiste in una stringa di connessione al database con attributi o proprietà particolari. Una volta creato, il file UDL può essere testato utilizzando SQL Server Management Studio per verificare la connettività.

### Proprietà della stringa di connessione
Le seguenti proprietà possono essere impostate in un UDL per garantire la connettività corretta:

- **Nome server**: posizione del server in cui si trova il database a cui si desidera accedere.
- **Opzioni di autenticazione**
- **Autenticazione Windows**: autenticazione a SQL Server utilizzando le credenziali dell'account Windows dell'utente attualmente connesso.
- **Autenticazione SQL Server**: autenticazione tramite ID di accesso e password.
- **Active Directory - Integrato**: autenticazione integrata con un'identità di Azure Active Directory; può essere utilizzato anche per l'autenticazione di Windows su SQL Server.
- **Active Directory - Password**: autenticazione di ID utente e password con un'identità di Azure Active Directory.
- **Active Directory - Universale con supporto MFA**: autenticazione interattiva con un'identità di Azure Active Directory.
- **Active Directory - entità servizio**: autenticazione con un'entità servizio di Azure Active Directory.
- **SPN server**: se si utilizza una connessione attendibile, è possibile specificare un nome dell'entità servizio (SPN) per il server.
- **Nome utente**: digita l'ID utente da utilizzare per l'autenticazione quando accedi all'origine dati.
- **Password**: digita la password da utilizzare per l'autenticazione quando accedi all'origine dati.
- **Password vuota**: se selezionata, consente al provider specificato di utilizzare una password vuota nella stringa di connessione.
- **Consenti salvataggio password**: consente di salvare la password con la stringa di connessione.
- **Utilizza crittografia avanzata per i dati**: i dati passati attraverso la connessione verranno crittografati.
- **Trust server certificate**: il certificato del server verrà convalidato.
- **Database**: nome del database a cui desideri accedere.
- **Allega un file di database come nome di database**: specifica il nome del file principale per un database collegabile.

## Riferimenti ##

* [Componenti di Microsoft Data Access](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Configurazione Universal Data Link (UDL)](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

