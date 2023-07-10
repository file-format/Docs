{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "file", "estensione", "formato", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri i file GLTF e le API che possono creare e aprire file GLTF.",
  "title" :"GLTF - Formato file di trasmissione GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file GLTF?

glTF (GL Transmission Format) è un formato di file 3D che memorizza le informazioni sul modello 3D in formato JSON. L'uso di JSON riduce al minimo sia la dimensione delle risorse 3D che l'elaborazione di runtime necessaria per decomprimere e utilizzare tali risorse. È stato adottato per la trasmissione e il caricamento efficienti di scene e modelli 3D dalle applicazioni. glTF è stato sviluppato dal Khronos Group 3D Formats Working Group ed è anche descritto come [JPEG](/it/image/jpeg/) di 3D dai suoi creatori.

Il formato file GLTF definisce un formato di pubblicazione estensibile e comune per strumenti e servizi di contenuto 3D che semplifica i flussi di lavoro di creazione e consente l'uso interoperabile dei contenuti in tutto il settore. L'intenzione alla base della creazione del formato file glTF era definire un formato di pubblicazione estensibile e comune per strumenti e servizi di contenuto 3D che dovrebbe semplificare i flussi di lavoro di creazione e consentire l'uso interoperabile dei contenuti in tutto il settore. Riduce al minimo l'elaborazione del runtime da parte delle applicazioni che utilizzano WebGL e altre API.

## Breve storia del file GLTF

Le prime specifiche per il formato di file glTF 1.0 sono state annunciate nell'ottobre 2015. Ciò era arrivato come una serie di sforzi iniziati nel marzo 2012 da Khronos. Lo scopo di questi sforzi era di valutare le opportunità intorno alla trazione WebGL. Di conseguenza, la prima demo del formato glTF, basato sul formato JSON, è stata presentata al meetup WebGl nel 2012. Il formato è stato adottato di volta in volta da diverse aziende tra cui Cesium, 3D Tiles, Oculus, Microsoft, Archilogic e altre.

glTF 2.0 è stato pubblicato il 5 giugno 2017 alla Web3D 2017 Conference. C'è un lungo elenco di aziende che hanno adottato il formato di file glTF in seguito.

## Formato file GLTF

Le specifiche del formato file per glTF 2.0 sono disponibili [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) come riferimento e dovrebbero essere consultate in qualsiasi implementazione relativa alla lettura/scrittura per il supporto di formato file glTF.

glTF definisce le risorse come file JSON con supporto di dati esterni. Rappresenta modelli 3D con l'ausilio di:

* Descrizione completa della scena contenuta in un file .glTF in formato JSON che include informazioni sulla gerarchia dei nodi, sui materiali, sulle telecamere, nonché informazioni sui descrittori per mesh, animazioni e altri costrutti
* File binari (.bin) contenenti geometrie e dati di animazione e altri dati basati su buffer
* File di immagine ([.jpg](/it/image/jpeg/), [.png](/it/image/png/)) per le trame

Eventuali risorse esterne come le immagini vengono archiviate in file esterni a cui viene fatto riferimento tramite URI. Questi URI vengono archiviati insieme al contenitore GLB o incorporati direttamente nel JSON utilizzando URI di dati. Ogni glTF valido deve specificare la sua versione.

glTF è stato progettato per ottenere file di piccole dimensioni, caricamento rapido, rappresentazione completa della scena 3D ed estensibilità. Questi obiettivi di progettazione unici sono i motivi principali della popolarità del formato di file glTF nel dominio 3D. Di seguito sono riportati i tipi mime supportati dal formato di file glTF per diversi tipi di file:

* I file .gltf utilizzano model/gltf+json
* I file .bin utilizzano application/octet-stream
* I file di texture utilizzano il tipo di immagine/* ufficiale in base al formato immagine specifico. Per la compatibilità con i moderni browser web, sono supportati i seguenti formati di immagine: image/jpeg, image/png.

### Codifica JSON

glTF impone le seguenti restrizioni aggiuntive sul formato di file JSON

Per semplificare l'implementazione lato client, glTF ha restrizioni aggiuntive sul formato e la codifica JSON.

1. JSON deve utilizzare la codifica UTF-8 senza BOM.
1. Tutte le stringhe definite in queste specifiche (nomi delle proprietà, enumerazioni) utilizzano solo set di caratteri ASCII e devono essere scritte come testo normale, ad esempio "buffer" invece di `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. I nomi (chiavi) all'interno degli oggetti JSON devono essere univoci, ovvero non sono consentite chiavi duplicate.

### URI

I buffer e le risorse immagine sono referenziati tramite URI. I seguenti due tipi di URI devono essere supportati dai client.

**URI di dati:** Gli URI di dati sono definiti dalla RFC 2397 e vengono utilizzati da glTF per incorporare risorse nel JSON.

**Percorsi URI relativi:** o path-noscheme come definito da RFC 3986, [Sezione 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — senza schema, autorità o parametri. I caratteri riservati devono essere codificati in percentuale, per RFC 3986, [Sezione 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Riferimenti ##

* [Specifiche glTF 2.0 - Khronos](https://github.com/KhronosGroup/glTF)
* [Formato file glTF - Di Wikipedia](https://en.wikipedia.org/wiki/GlTF)

