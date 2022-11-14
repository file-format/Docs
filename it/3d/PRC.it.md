---
date: 2019-10-11
keywords: prc, .prc, formato file prc, come aprire file prc, estensione .prc, estensione prc
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file RPC
linktitle: PRC
description: "Informazioni sul formato di file PRC e sulle API che possono creare e aprire file PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## I formati di file della RPC
Le estensioni ".prc" vengono utilizzate per il formato file 3D Product Representation Compact e un formato file e-book da MobiPocket.

## Che cos'è un file Product Representation Compact (PRC)?

PRC (Product Representation Compact) è un formato di file 3D ottimizzato per archiviare, caricare e visualizzare dati 3D provenienti soprattutto da sistemi CAD (Computer-Aided Design). È un file binario sequenziale, scritto in modo portatile. PRC può essere utilizzato per incorporare dati 3D in un file PDF. PRC supporta la maggior parte dei costrutti principali del CAD come assiemi e parti, alberi di entità 3D, rappresentazione della geometria esatta, rappresentazione triangolare e markup. PRC utilizza l'estensione .prc e il tipo di supporto Internet utilizzato è *model/prc*.

PRC è un formato di file multiuso che, in base al suo utilizzo, può essere archiviato utilizzando la normale compressione per rappresentare direttamente i dati CAD o essere archiviato utilizzando una compressione elevata per ridurre le dimensioni del file. I dati 3D archiviati in un PDF utilizzando il formato PRC sono interoperabili con le applicazioni CAM e CAE.

### Specifica del formato file di rappresentazione del prodotto Compact (PRC).

Un file PRC ha una sezione di intestazione principale seguita da una o più strutture di file seguite da un file modello alla fine. Una struttura di file ha un'intestazione seguita dalle seguenti sezioni di dati:

- **Globali**: contiene le strutture e i colori dei file di riferimento, gli stili di linea e i sistemi di coordinate per ciascuna entità ad albero della struttura del file.
- **Albero**: contiene una descrizione dell'albero di elementi come occorrenze del prodotto, definizioni delle parti, elementi di rappresentazione e markup.
- **Tessellation**: contiene tutti i dati tassellati (triangolati) nelle entità foglia dell'albero (elementi di rappresentazione e markup).
- **Geometria**: contiene tutti i dati esatti di geometria e topologia delle entità foglia dell'albero (elementi di rappresentazione).
- **Geometria extra**: Contiene i dati di riepilogo della geometria. Ciò consente di caricare parzialmente il file senza caricare l'intera geometria.

Quella che segue è la struttura di un tipico file PRC.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Che cos'è un file di e-book MobiPocket con estensione PRC
Anche un formato di file e-book introdotto da una società francese denominata **Mobipocket** utilizza l'estensione ".prc". Inizialmente, Mobipocket ha lanciato un'applicazione gratuita per più dispositivi intelligenti come tablet pc, PDA e smartphone. L'estensione ".prc" è in realtà identica a .mobi ma viene utilizzata in particolare per i PDA che supportano solo le estensioni **.prc** o **.pdb**.

### Specifiche del formato di file Mobipocket PRC
Il formato di file MobiPocket PRC si basa sullo standard Open eBook utilizzando XHTML e può anche includere JavaScript e frame. È inoltre disponibile il supporto per le query SQL native da utilizzare con i database incorporati.

Il Mobipocket Reader ha una libreria di home page. I lettori possono inserire pagine bianche in qualsiasi parte di un libro e aggiungere disegni variabili. Gli oggetti come Annotazioni, segnalibri, correzioni, note e disegni sono gestibili da un'unica posizione. Le immagini vengono convertite in formato GIF e hanno una dimensione massima di 64K, sufficiente per telefoni cellulari con schermi piccoli. Mobipocket Reader ha i segnalibri elettronici e un dizionario integrato.

Il lettore ha una modalità a schermo intero per la lettura e il supporto per molti PDA, Comunicatori e Smartphone. I prodotti Mobipocket supportano la maggior parte dei sistemi operativi Palm, Windows, Symbian, BlackBerry, ma non Android. Il lettore funziona sotto Linux o Mac OS X usando WINE.

## Riferimenti

- [PRC - Wikipedia](https://en.wikipedia.org/wiki/PRC_(file_format))
- [Specifica del formato PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [Confronto dei formati di e-book - Di Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

