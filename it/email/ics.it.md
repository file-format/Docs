{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - Formato file iCalendar",
  "description":"Scopri il formato di file ICS e le API che possono creare e aprire file ICS.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file ICS?

ICalendar (Internet Calendaring and Scheduling Core Object Specification) è uno standard Internet (RFC 2445) per lo scambio e la distribuzione degli eventi di calendario e della pianificazione. Il formato iCalendar è interoperabile, garantendo così lo scambio di informazioni di calendario tra gli utenti che dispongono di diverse applicazioni di posta elettronica. iCalendar formatta i dati di input come MIME (Multipurpose Internet Mail Extensions) e facilita lo scambio di oggetti tramite diversi protocolli di trasporto. Questi protocolli di trasporto possono essere SMTP, HTTP, comunicazione asincrona point-to-point e trasporto di rete basato su supporti fisici.

iCalendar consente agli utenti di condividere eventi, attività dipendenti da data/ora e informazioni sulla disponibilità tramite e-mail ad altri utenti che possono rispondere. I file iCalendar vengono archiviati utilizzando i suffissi ".ics" ".iCalendar" o ".ifb" con un tipo MIME di "text/calendar". iCalendar è mantenuto per essere autosufficiente senza alcuna dipendenza dal protocollo di trasporto. I server Web (con protocollo HTTP) possono trasportare informazioni iCalendar e le pagine Web possono contenere dati iCalendar in formato incorporato utilizzando iCalendar.

## Breve storia del formato di file ICS

Nel 1998, l'Internet Engineering Task Force (IETF) ha definito iCalendar come standard (RFC 2445). Lo standard è stato documentato da Frank Dawson (Lotus Notes Corporation) e Derik Stenerson ( Microsoft). Nel 2009, lo standard è stato nuovamente perfezionato da Bernard Desruisseaux (Oracle) come RFC 5545. Questa volta sono state aggiunte alcune nuove funzionalità e alcune funzionalità obsolete sono state deprecate. Nel 2016, RFC 7986 è stato rilasciato e aumentato all'originale iCalendar RFC. RFC 7986 ha aggiunto nuove caratteristiche all'oggetto principale di VCALENDAR e sono state introdotte anche nuove funzionalità di supporto per i sistemi di conferenza.

## Formato file ICS ##

Il tipo MIME utilizzato dai dati di iCalendar è "testo/calendario". Il set di caratteri predefinito per iCalendar è UTF-8, tuttavia, fornendo parametri in MIME, è possibile utilizzare un set di caratteri diverso. Un file iCalendar contiene sezioni, tra queste sezioni "VCALENDAR", è la sezione globale che incapsula tutte le altre sezioni. La sezione VEVENT definisce gli eventi, VTODO elenca tutte le cose da fare, VJOURNAL contiene le voci del diario e VTIMEZONE specifica le informazioni sul fuso orario. sono consentite più sezioni di categoria simile. Per numerosi eventi, più sezioni VEVENT possono essere presenti in un file iCalendar.

### Righe di contenuto ###

Gli oggetti iCalendar sono organizzati in righe di testo distinte "righe di contenuto". In questo formato di file, la sequenza CRLF termina una riga mentre la lunghezza della riga è limitata a 75 ottetti esclusa l'interruzione di riga. Un elemento di dati lungo può essere esteso a più righe.

### Elenco e separatori di campo ###

Proprietà e parametri specificano l'elenco di valori separati da un carattere COMMA. Le stringhe tra virgolette vengono utilizzate per i valori dei parametri basati su URI. L'elenco dei parametri può essere costruito dal valore della proprietà. Ciascun parametro di proprietà in questo elenco deve essere separato da un SEMICOLON.

In una lista valori, un SEMICOLON isola i parametri di proprietà e un COMMA separa i valori di proprietà. L'esempio è riportato di seguito:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Valori multipli

Alcune proprietà possono avere più valori. La semplice generazione di una nuova riga di contenuto con il nome della proprietà è la regola di base per le proprietà multivalore. Tuttavia, per un valore singolo con più varianti di lingua non è necessario utilizzare proprietà multivalore.

### Contenuto binario

All'interno di un oggetto iCalendar, il valore della proprietà può fare riferimento a dati di contenuto binario inseriti in un'entità MIME esterna utilizzando un URI. Il contenuto binario in linea può essere utilizzato in situazioni speciali con il parametro "ENCODING", in cui l'applicazione deve esprimere un oggetto iCalendar come un'unica entità. L'esempio seguente spiega una proprietà "ATTACH" con un riferimento URI:

ALLEGARE: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Set di caratteri

Sebbene lo schema di set di caratteri predefinito per un iCalendar sia UTF-8, tuttavia non viene specificato alcun parametro di proprietà per definire il set di caratteri di un valore di proprietà. nei trasferimenti MIME il parametro "charset" DEVE essere utilizzato per il set di caratteri esistente.

## Riferimenti

* [Specifica dell'oggetto principale di calendario e pianificazione Internet](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

