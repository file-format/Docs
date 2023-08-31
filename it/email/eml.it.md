{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - Messaggio di posta elettronica",
  "description":"Scopri il formato di file EML e le API che possono creare e aprire file EML.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Che cos'è un file EML?

Il formato di file EML rappresenta i messaggi di posta elettronica salvati utilizzando Outlook e altre applicazioni pertinenti. Quasi tutti i client di posta elettronica supportano questo formato di file per la sua conformità con RFC-822 Internet Message Format Standard. Microsoft Outlook è il software predefinito per l'apertura dei tipi di messaggi EML. I file EML possono essere utilizzati per il salvataggio su disco e per l'invio ai destinatari utilizzando i protocolli di comunicazione.

## Breve storia di EML

Le specifiche del formato file EML sono disponibili secondo [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Formato standard. Prima di RFC-822, RFC-733 governava le regole dello scambio di messaggi di rete fino a quando nel 1982 il primo è stato creato come miglioramento del laterale stabilendo standard ARPA. Allo stesso tempo, Microsoft ha creato i propri moduli COM per lo sviluppo del proprio client di posta elettronica, ovvero Outlook Express. RFC-822 ha intrapreso la strada per essere stabilito come formato proprietario quando Microsoft ha deviato dallo standard aperto e ha creato il formato di file [PST](/it/email/pst/) in cui le e-mail vengono salvate in un formato di database altamente strutturato. Ciò ha comportato problemi per gli utenti di client di posta elettronica non Microsoft quando le e-mail venivano inoltrate da Microsoft Outlook.

Era il 2001 quando lo standard 822 è stato migliorato in 2822 - Internet Message Format, attualmente in uso per creare, leggere e inviare messaggi EML in formato MIME RFC-822.

## Specifiche del formato file EML

I file EML comprendono due sezioni distinte:

* Intestazioni - Contiene informazioni sull'intestazione del messaggio
* Corpo del messaggio: contiene una serie di informazioni che possono includere il contenuto del messaggio, le immagini incorporate e gli allegati

### Informazioni sulle intestazioni ###

Un file EML è costituito da informazioni sulle intestazioni e, facoltativamente, dal corpo del messaggio. Ogni riga di intestazione nell'EML ha due parti separate da due punti ":". Il primo si chiama Header Name e quello che segue i due punti è il corpo dell'intestazione. Ad esempio, tali intestazioni includono:

* Indirizzo email del mittente
* Indirizzo email del destinatario
* Oggetto dell'e-mail
* Data e ora del messaggio

**Esempio di intestazione**

```
Da:<John@bmw.eml.light.com>

Per:<Andy@fileformat.com>

Data: Thu, 8 Mar 2018 10:43:37 +0100

Oggetto: luce bmw eml
```

### Corpo del messaggio ###

Il corpo del messaggio EML contiene le informazioni principali dell'e-mail sotto forma di testo, collegamenti ipertestuali e allegati. Il corpo dell'e-mail può contenere testo leggibile ma non è necessario. In questo caso, il corpo del messaggio può essere vuoto o contenere dati di allegati codificati.

I contenuti del corpo del messaggio sono descritti dal tipo di contenuto che consente alle applicazioni di lettura di leggere le informazioni nei rispettivi formati. Rappresenta in realtà la natura e il formato di un documento. La struttura di un tipo MIME o di un tipo di contenuto è molto semplice; è costituito da un tipo e un sottotipo, due stringhe, separate da '/'. Non è consentito spazio. Il `tipo` rappresenta la categoria e può essere un tipo discreto o multiparte. Il `sottotipo` è specifico per ogni tipo. L'elenco dei tipi, che rientrano nella categoria dei tipi di contenuto, è lungo ma alcuni tipi di contenuto importanti sono i seguenti:


|**Tipo**|**Descrizione**|**Esempio di sottotipi**
---|---|---|
|testo|Rappresenta un formato leggibile|testo/normale, testo/html, testo/css, testo/javascript
|immagine|Rappresenta immagini di qualsiasi tipo esclusi i video|immagine/bmp, immagine/png, immagine/jpg, immagine/gif
|audio|Rappresenta qualsiasi formato di file audio|audio/mdi, audio/wav
|applicazione|Rappresenta qualsiasi tipo di dato binario|applicazione/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Rappresentazione dell'attaccamento nel corpo EML ###

Il corpo EML contiene i limiti per ogni tipo di contenuto che contiene. L'allegato nel corpo del messaggio è identificato dal tipo di contenuto e dalla disposizione del contenuto, come mostrato nell'esempio seguente:

Tipo di contenuto: testo/semplice; set caratteri#"windows-1252"; nome#"app store.txt di Apple"
Contenuto-Disposizione: allegato; nomefile#"app store.txt di Apple"
Codifica di trasferimento di contenuti: base64
ID allegato X: f_jkhztmd02

Come si può vedere, l'impostazione Content-Disposition su allegato abilita le applicazioni di lettura per ottenere informazioni sugli allegati come il nome del file allegato e la codifica del trasferimento. Le informazioni sull'intestazione dell'allegato sono seguite dal contenuto dell'allegato codificato che deve essere letto.

#### Esempio di foglio elettronico come allegato ####

Tipo di contenuto: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; nome#"english_spodr.xlsx"
Contenuto-Disposizione: allegato; nomefile#"english_spodr.xlsx"
Codifica di trasferimento di contenuti: base64
ID allegato X: f_jkhztmd43

## Riferimenti

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

