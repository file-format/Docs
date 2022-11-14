{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file FIT - File attività Garmin",
  "description":"Scopri il formato di file FIT e le API che possono creare e aprire file FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Che cos'è un file FIT?

Un file FIT è un file GIS creato dai dispositivi indossabili sportivi Garmin. Viene utilizzato per registrare le attività della persona quando si muove indossando questi dispositivi. I dati dell'attività includono la posizione e l'ora registrati dal dispositivo GPS. I file FIT vengono utilizzati anche per trasferire i dati dell'attività registrata utilizzando le API web. Questo è il motivo per cui i file FIT sono il formato di file più comunemente usato per condividere dati di fitness con altre piattaforme di fitness. Altri formati di file comuni includono [GPX](/it/gis/gpx/), TCX e [KML](/it/gis/kml/).

## Formato file FIT - Ulteriori informazioni

I file FIT vengono salvati su disco come file binari con le informazioni registrate dai dispositivi Garmin per l'attività. Le informazioni memorizzate all'interno di un file FIT includono:

* Appuntamento
* Tipi di sport
* Dati giro e divisione
* Traccia GPS
* Dati del sensore
* Eventi per la sessione attiva

I dati dell'attività possono essere registrati nel file in tempo reale o esportati una volta completata la registrazione dell'attività.

### Messaggi di attività FIT

Un file di attività FIT può includere alcuni tipi di messaggi richiesti. Di seguito sono riportati i messaggi richiesti per un file di attività.

|Messaggio|Scopo|
---|---|
|ID file| Il messaggio ID file è richiesto da tutti i tipi di file FIT e dovrebbe essere il primo messaggio nel file. Per i file di attività, la proprietà Tipo deve essere impostata su 4.|
|Attività| È necessario un singolo messaggio di attività in un file di attività FIT. Nel messaggio di attività sono incluse le proprietà Timestamp locale e Conteggio sessioni. Il timestamp locale viene utilizzato per determinare l'offset del fuso orario che può essere applicato a tutti i timestamp nel file. La maggior parte dei dispositivi registra i file FIT in tempo reale e il conteggio delle sessioni sarà sconosciuto fino alla fine della registrazione. Per questo motivo, il messaggio di attività sarà spesso l'ultimo messaggio nel file.|
|Sessione| I file di attività conterranno uno o più messaggi di sessione. Un messaggio di sessione è un tipo di messaggio di riepilogo. Ora inizio, Tempo trascorso totale, Tempo totale timer e Timestamp sono campi obbligatori per tutti i messaggi di riepilogo.|
|Giro| I messaggi di giro rappresentano giri o intervalli all'interno della sessione. Un messaggio Lap è un tipo di messaggio Riepilogo. Ora inizio, Tempo trascorso totale, Tempo totale timer e Timestamp sono campi obbligatori per tutti i messaggi di riepilogo.|
|Registra| I messaggi di registrazione includono coordinate GPS, velocità, distanza, frequenza cardiaca, potenza, ecc.|

## File FIT Risorse utili

* [Decodifica dei file di attività FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Codifica dei file di attività FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Riferimenti ##

* [File attività FIT](https://developer.garmin.com/fit/file-types/activity/)

