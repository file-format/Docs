{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File HTACCESS - Formato file Apache HTACCESS",
  "description" :"La tua guida al formato del file per sapere cos'è un file HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file HTACCESS?

Un file HTACCESS è un file di configurazione di Apache che fornisce un meccanismo per consentire modifiche alla configurazione per diverse cartelle/directory di un sito Web. Include direttive di configurazione applicabili alla directory e alle sottodirectory.

Un file HTACCESS esegue una serie di controlli come definire la pagina di indice di un sito Web, elencare la pagina di errore 404 (Pagina non trovata), eseguire reindirizzamenti di pagina 301 o 302, bloccare l'accesso da un indirizzo IP specifico o da altri siti Web. L'uso di file .htaccess, quindi, rallenta le prestazioni complessive del tuo server Apache [HTTP](/it/web/http/).

## Formato file HTACCESS

I file HTACCESS vengono archiviati su disco in formato di file di testo normale. Ciò significa che puoi aprire e modificare questi file in qualsiasi editor di testo. Non c'è un nome prima di "." in un file .htaccess, mostrando che si tratta di un file nascosto all'interno della cartella.

## Usi comuni di un file HTACCESS

Cinque usi comuni di un file HTACCESS sono i seguenti.

### Mod_Riscrivi

Un file HTACCESS può essere utilizzato per designare e modificare il modo in cui gli URL e le pagine Web su un sito Web vengono visualizzati agli utenti.

### Autenticazione

L'autenticazione può essere ottenuta con .htaccess creando un file password chiamato .htpasswd. Ciò consente ai visitatori del sito di fornire una password se desiderano visitare una determinata sezione della pagina web.

### Pagine di errore personalizzate

Puoi creare pagine di errore personalizzate come 400 Richiesta non valida, 401 Autorizzazione richiesta, 403 Pagina proibita, 404 File non trovato e 500 Errore interno con il file .htaccess. Tuttavia, questi rallenteranno le prestazioni del server poiché tutti i controlli verranno eseguiti quando si accede alle pagine.

### Tipi MIME

I file Apache HTACCESS possono essere modificati per includere i tipi MIME (Multipurpose Internet Mail Extensions). Ciò consente al tuo server di supportare la consegna dei file dell'applicazione che non erano supportati dal sito.

### SSI

Server Side Include (SSI) funge da grande risparmio di tempo su un sito web. SSI può essere abilitato inserendo il codice seguente nel tuo file .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Esempio di file Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Riferimenti

* [Esercitazione sul server HTTP Apache: file .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

