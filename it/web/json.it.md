---
date: 2019-10-11
keywords: json, .json, formato file json, come aprire file json, notazione oggetto javascript, formato dati json, formato file .json
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file JSON - Che cos'è un file JSON?
linktitle: JSON
description: "Ulteriori informazioni sul formato di file JSON e sulle API che possono creare e aprire file JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Che cos'è un file JSON?

JSON (JavaScript Object Notation) è un formato di file standard aperto per la condivisione di dati che utilizza testo leggibile per archiviare e trasmettere dati. I file JSON vengono archiviati con l'estensione .json. JSON richiede meno formattazione ed è una buona alternativa per [XML](/it/web/xml/). JSON è derivato da JavaScript ma è un formato di dati indipendente dalla lingua. La generazione e l'analisi di JSON è supportata da molti linguaggi di programmazione moderni. *application/json* è il tipo di supporto utilizzato per JSON.

## Formato file JSON - Breve cronologia

C'era bisogno di una comunicazione server-client in tempo reale che portasse alla creazione di JSON. Il formato JSON è stato specificato per la prima volta da Douglas Crockford nel marzo 2001. JSON era basato sullo standard ECMA-262 3a edizione, dicembre 1999, che è un sottoinsieme di JavaScript.

La prima edizione dello standard JSON ECMA-404 è stata pubblicata nell'ottobre 2013 da Ecma International. RFC 7159 è diventato il riferimento principale per gli usi Internet di JSON nel 2014. Nel novembre 2017, ISO/IEC 21778:2017 è stato pubblicato come standard internazionale. RFC 8259 è stato pubblicato il 13 dicembre 2017 da The Internet Engineering Task Force, che è la versione attuale dell'Internet Standard STD 90.

## Struttura del file JSON

I dati JSON vengono scritti in coppie **chiave/valore**. La chiave e il valore sono separati da due punti(:) al centro con la chiave a sinistra e il valore a destra. Diverse coppie chiave/valore sono separate da una virgola(). La chiave è una stringa racchiusa tra virgolette doppie, ad esempio "nome". I valori possono essere dei seguenti tipi.

- 'Numero'
- `Stringa`: sequenza di caratteri Unicode racchiusi tra virgolette doppie.
- `Booleano`: Vero o Falso.
- `Array`: un elenco di valori racchiusi tra parentesi quadre, per esempio

```json
[ "Mela", "Banana", "Arancia" ]
```

- `Oggetto`: una raccolta di coppie chiave/valore racchiuse tra parentesi graffe, per esempio

```json
{"name": "Jack", "età": 30, "favoriteSport" : "Calcio"}
```

Gli oggetti JSON possono anche essere nidificati per rappresentare la struttura dei dati. Di seguito è riportato un esempio di un oggetto JSON.

### Esempio di formato JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Qual è la dimensione massima del file JSON?

Non c'è praticamente alcun limite alla dimensione massima di un file JSON. Può essere lungo quanto lo spazio richiesto dal contenuto da archiviare.

Quando si tratta di utilizzare il formato di file JSON per il trasferimento di dati su Internet, è necessario prestare attenzione alle risorse disponibili del computer. Se vengono trasferiti dati JSON di grandi dimensioni, il trasferimento sarà interessato se il browser client ha memoria limitata.


Non esiste un limite rigido definito dalle specifiche, ma devi fare attenzione a non esaurire le risorse sui computer dei tuoi utenti, poiché degraderà rapidamente la loro esperienza utente ed è probabile che abbandonino la tua app.

## JSON contro XML

**XML** è un altro formato di file comune e ampiamente utilizzato per lo scambio di dati su Internet. Quando si tratta di scambio di dati tra applicazioni, gli sviluppatori hanno la possibilità di utilizzare sia i formati di file XML che JSON. Tuttavia, JSON viene adottato come il modo più conveniente per lo scambio di dati tra applicazioni su Internet per i seguenti motivi.

1. JSON offre una visualizzazione dei dati chiara e di facile lettura rispetto ai formati di file XML
1. JSON riduce il sovraccarico del trasferimento di dati su Internet poiché ha un numero inferiore di caratteri per definire lo stesso set di dati rispetto a XML
1. I moderni linguaggi di programmazione forniscono parser integrati per analizzare la risposta JSON sul Web.

## Lo sapevate?

Puoi diventare un collaboratore su FileFormat.com per mantenere la comunità dei formati di file aggiornata con i tuoi risultati. Se devi condividere qualcosa sui formati di file JSON o Web, puoi pubblicare i tuoi risultati nella sezione [Notizie sul formato file Web](https://news.fileformat.com/t/Web) affinché le persone possano saperne di più da questi.

## Riferimenti

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Un'introduzione a JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

