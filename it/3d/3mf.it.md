{
  "date" : "2019-12-09",
  "keywords" :[ "file 3mf", "formato file 3mf", "cos'è un file 3mf", "file", "esempio 3mf", "estensione file 3mf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"3MF",
  "description":"Scopri il formato di file 3MF e le API che possono aprire e creare file 3MF.",
  "linktitle" : "3MF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-12-09"
}

## Che cos'è un file 3MF?

3MF, 3D Manufacturing Format, viene utilizzato dalle applicazioni per eseguire il rendering di modelli di oggetti 3D in una varietà di altre applicazioni, piattaforme, servizi e stampanti. È stato creato per evitare le limitazioni e i problemi in altri formati di file 3D, come [STL](/it/cad/stl/), per lavorare con le ultime versioni di stampanti 3D. 3MF è un formato di file relativamente nuovo che è stato sviluppato e pubblicato dal consorzio 3MF. È abbastanza ricco da descrivere completamente un modello, conservando informazioni interne, colore e altre caratteristiche che lo rendono estensibile per supportare le nuove innovazioni nella stampa 3D. Il formato è estensibile, in grado di essere ampiamente adottato e privo di problemi che affliggono altri formati di file ampiamente utilizzati.

## Breve storia del formato file 3MF

Le limitazioni esistenti nei formati di file descrittivi dei modelli disponibili, come STL e altri, portano i marchi leader a riunirsi e formulare un formato di file più estensibile per la stampa 3D. Un'importante considerazione riguardava il modo in cui le applicazioni avrebbero dovuto trasferire i dati del modello alle stampanti 3D. Il consorzio 3MF, quindi, è nato per supportare un nuovo formato di file 3D chiamato 3MF con l'obiettivo di renderlo sufficientemente estensibile per soddisfare le esigenze della stampa 3D. Diverse aziende facevano parte di questo consorzio tra cui Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP e altri. Microsoft ha donato i lavori in corso in formato file 3D come punto di partenza per l'ulteriore sviluppo collaborativo delle specifiche da parte del Consorzio 3MF.

## Formato file 3MF - Ulteriori informazioni

3MF è un formato di dati basato su XML – XML compresso leggibile dall'uomo – che include definizioni per i dati relativi alla produzione 3D, inclusa l'estendibilità di terze parti per i dati personalizzati. Il formato di file 3MF è stato progettato tenendo presente le limitazioni e i problemi affrontati da altri formati di file 3D. Ciò ha portato alla formulazione del formato di file 3MF che è:

* **Completo:** Contenente tutte le informazioni necessarie su modello, materiale e proprietà in un unico archivio
* **Leggibile dall'uomo:** utilizzando strutture comuni come OPC, [ZIP](/it/compression/zip/) e XML per facilitare lo sviluppo
* **Semplice:** una specifica breve e chiara, che semplifica lo sviluppo e la convalida veloce
* **Estendibile:** L'utilizzo degli spazi dei nomi XML consente estensioni sia pubbliche che private mantenendo la compatibilità
* **Non ambiguo:** Linguaggio chiaro e test di conformità assicurano che un file sia sempre coerente dal digitale al fisico
* **Gratuito:** L'accesso e l'implementazione della specifica 3MF è e sarà sempre esente da royalties, brevetti e licenze

Le specifiche per il formato file 3MF sono ospitate su [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) per l'accesso pubblico e aggiornamenti continui. L'attuale versione pubblicata è la 1.2.3 che descrive l'insieme delle convenzioni per l'uso di XML e di altre tecnologie ampiamente disponibili per descrivere il contenuto e l'aspetto di uno o più modelli 3D. Gli sviluppatori, che desiderano creare sistemi per l'elaborazione di formati di file 3MF, possono fare riferimento a queste specifiche per scopi di implementazione.

## Specifiche del formato file 3MF

Il formato di file 3MF utilizza le specifiche Open Packaging sotto forma di archivio ZIP per il suo modello fisico. Include un insieme ben definito di parti e relazioni che soddisfano uno scopo particolare nel documento. Ciò consente inoltre al formato di seguire la funzionalità del pacchetto, comprese le firme digitali e le miniature.

### Il documento 3MF - Una panoramica

Un tipico documento 3MF ha il seguente aspetto:

![3MF Document Structure](https://github.com/3MFConsortium/spec_core/raw/master/images/figure_2-1.png "3MF Document Structure")

Il carico utile include il set completo di parti necessarie per l'elaborazione della parte del modello 3D. Tutto il contenuto da utilizzare per produrre un oggetto descritto nel carico utile 3D DEVE essere contenuto nel Documento 3MF. La descrizione di ciascuna parte del documento insieme al relativo stato come richiesto o opzione è riportata nella tabella seguente.


|**Nome**|**Descrizione**|**Origine relazione**|**Obbligatorio/Facoltativo**
--- | --- | --- | ---
|Modello 3D|Contiene la descrizione di uno o più oggetti 3D per la produzione.|Pacchetto|RICHIESTO
|Proprietà principali|La parte OPC che contiene varie proprietà del documento.|Pacchetto|FACOLTATIVO
|Origine firma digitale|La parte OPC che è la radice delle firme digitali nel pacchetto.|Pacchetto|FACOLTATIVO
|Firma digitale|Parti OPC che contengono ciascuna una firma digitale.|Origine firma digitale|FACOLTATIVA
|Certificato di firma digitale|Parti OPC che contengono un certificato di firma digitale.|Firma digitale|FACOLTATIVA
|PrintTicket|Fornisce le impostazioni da utilizzare durante l'output degli oggetti 3D nella parte del modello 3D.|Modello 3D|FACOLTATIVO
|Miniatura|Contiene una piccola immagine JPEG o PNG che rappresenta gli oggetti 3D nel pacchetto o il pacchetto nel suo insieme.|Pacchetto|FACOLTATIVO
|Texture 3D|Contiene una texture utilizzata per applicare il colore a un oggetto 3D nella parte del modello 3D (disponibile per estensioni)|Modello 3D|FACOLTATIVO
|Parti personalizzate|Parti OPC associate ai metadati|Pacchetto|FACOLTATIVO

Le [Parti e relazioni](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [Modelli 3D](https:/ /github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Risorse oggetto](https://github.com/3MFConsortium/spec_core/blob/master /3MF%20Core%20Specification.md#chapter-4-object-resources), [Risorse materiali](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5 -material-resources) e [Caratteristiche del pacchetto](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) sezioni delle specifiche documento fornisce informazioni dettagliate sul documento 3MF.

## Riferimenti ##

* [Specifiche del formato file 3MF](https://github.com/3MFConsortium/spec_core)
* [3MF - Di Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)

