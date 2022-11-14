{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","file mhtml", "formato file mhtml", "tipo di file mhtml", "file", "tipo", "che cos'è un file mhtml"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - File HTML MIME",
  "description":"Scopri il formato di file MHTML e le API che possono creare e aprire file MHTML.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file MHTML?

I file con estensione MHTML rappresentano un formato di archivio di pagine Web che può essere creato da una serie di applicazioni diverse. Il formato è noto come formato archivio perché salva il codice Web **[HTML](/it/web/html/)** e le risorse associate in un unico file. Queste risorse includono qualsiasi cosa collegata alla pagina Web come immagini, applet, animazioni, file audio e così via. I file MHTML possono essere aperti in una varietà di applicazioni come Internet Explorer e Microsoft Word. Microsoft Windows utilizza il formato di file MHTML per la registrazione di scenari di problemi osservati durante l'utilizzo di qualsiasi applicazione su Windows che solleva problemi. Il formato di file MHTML codifica il contenuto della pagina in modo simile alle specifiche definite in message/rfc822, che sono specifiche relative all'e-mail di testo normale. Le specifiche effettive del formato sono dettagliate da [RFC 2557](https://tools.ietf.org/html/rfc2557).

## Formato file MHTML

MHTML è anche noto come MIME Encapsulation of Aggregate HTML documents per la sua capacità di codificare pagine Web HTML insieme alle sue risorse in un unico archivio Web. Secondo le specifiche RFC 2557, un documento aggregato è un messaggio con codifica MIME che contiene una risorsa radice (oggetto) e altre risorse ad essa collegate tramite URI. Tali altre risorse possono essere rappresentazioni di immagini in linea, fogli di stile, applet, ecc. Inoltre, queste possono essere la radice di altri documenti multimediali. Le specifiche complete del documento per il formato di file MHTML sono dettagliate nella [RFC 2557](https://tools.ietf.org/html/rfc2557) e dovrebbero essere riferite per qualsiasi tipo di sviluppo di applicazioni per la lettura/scrittura di questo formato di file. Lo standard specifica che le parti del corpo a cui fare riferimento possono essere identificate da un Content-ID o da una Content-Location.

### Intestazioni di contenuto MIME

Un'intestazione di contenuto MIME, Content-Location, è definita per risolvere i riferimenti URI a risorse in altre parti del corpo. Questa intestazione può essere presente in qualsiasi messaggio o intestazione di contenuto.

### Intestazione della posizione del contenuto

Un Content-Location è una rappresentazione di un URI che etichetta il contenuto di una parte del corpo in cui è posizionato. Il suo valore può essere un URI assoluto o relativo. Può essere utilizzato per etichettare una risorsa che non è recuperabile da alcuni o da tutti i destinatari di un messaggio. Un singolo messaggio può avere una sola intestazione Content-Location. Esempio di una struttura multiparte/correlata contenente parti del corpo con etichette Content-Location e Content-ID:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### URI di aggregati MHTML

L'URI dell'aggregato MHTML è diverso da quello dell'URI radice. Il campo di intestazione Content-Location dovrebbe essere applicato all'intero aggregato se viene utilizzato nell'intestazione di un'intestazione multiparte/correlata. Allo stesso modo, l'insieme di risorse recuperate può essere diverso dall'insieme di risorse recuperate utilizzando i Content-Locations delle sue parti quando l'URI che fa riferimento all'aggregato MHTML viene utilizzato per recuperare questo aggregato. Ad esempio, il recupero di un aggregato MHTML può restituire una versione precedente, mentre il recupero dell'URI radice e dei suoi oggetti collegati in linea può restituire una versione più recente.

## Riferimenti

* [Incapsulamento MIME di documenti aggregati - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [Formato file MHTML - Di Wikipedia](https://en.wikipedia.org/wiki/MHTML)

