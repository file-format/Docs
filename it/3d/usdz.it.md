{
  "date" : "2021-02-01",
  "keywords" :["usdz", "file usdz", "formato file usdz", "formato file", "3d", "download file usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Formato ZIP per la descrizione della scena universale",
  "description":"Scopri il formato di file USDZ e le API che possono aprire e creare file USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Che cos'è un file USDZ?

Un file con .usdz è un archivio ZIP non compresso e non crittografato per il formato di file [USD](/it/3d/usd/) (Descrizione scena universale) che contiene e proxy per file di altri formati (come trame e animazioni) incorporati all'interno l'archivio e li esegue direttamente con il runtime USD senza bisogno di decomprimere. I file USDZ sono pacchetti il cui design si basa sulla nuova astrazione a livello Ar di un pacchetto. Usdz è stato registrato con IANA e ha il nome del tipo di supporto del modello e un nome del sottotipo di vnd.usd+zip e i suoi dettagli possono essere trovati su [Pagina di registrazione IANA](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## Formato file USDZ

I file USDZ si basano sul formato di file ZIP che archivia i singoli file nel suo contenitore. Ciò consente al ricevitore di decomprimere semplicemente il contenuto e utilizzare i normali file di descrizione della scena USD per lavorare e ispezionare. Quasi tutti i sistemi operativi forniscono il supporto integrato per i formati di file ZIP e la scelta di questo formato di archiviazione rispetto a qualsiasi metodo personalizzato rende facile per i file USDZ essere utili come un semplice protocollo di trasporto.

### Vincoli ZIP

Il formato file USDZ utilizza il formato file ZIP senza alcuna "compressione" e "crittografia". Questo è stato mirato dalla progettazione per soddisfare due requisiti:

* Per un pacchetto già caricato in memoria o come singolo file su disco, le API sono disponibili in USD per accedere ai dati contenuti nell'immagine
* Non dovrebbe essere necessario estrarre file su disco o allocare più spazio di archiviazione heap

Con USDZ, entrambi questi requisiti sono soddisfatti poiché la maggior parte dei formati di immagine stessi consente schemi di compressione interni, con conseguente dimensione del file compatta.

### Requisiti di layout

I pacchetti USDZ richiedono che il layout dei file all'interno del pacchetto sia che i dati per ciascun file inizino a un multiplo di 64 byte dall'inizio del pacchetto. Tuttavia, il pacchetto dovrebbe iniziare con un file nativo [USD](/it/3d/usd/) in caso di destinazione del pacchetto con un semplice riferimento. In tal caso, questo primo file USD viene indicato come il livello predefinito. I clienti che desiderano fornire "contenuti in streaming" potrebbero voler considerare anche altri vincoli di layout.

## Download del file USDZ
Poiché i file usdz sono pieni di altre immagini e file usd di alta qualità, possono occupare una maggiore memoria su disco. Qui puoi trovare un file di esempio USDZ semplice e più piccolo da scaricare:

- [Sample.usdz](../sample.usdz)

## Riferimenti

* [Specifiche del formato file USDZ](https://openusd.org/release/spec_usdz.html)
