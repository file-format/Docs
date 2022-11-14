---
date: 2019-10-11
keywords: step, .step, formato file step, come aprire i file step, estensione .step, estensione step
autore:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato file STEP
linktitle: STEP
description: "Scopri il formato di file STEP e le API che possono creare e aprire file STEP."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Che cos'è un file STEP?

Il file STEP è un formato di scambio dati ampiamente utilizzato per la progettazione assistita da computer (CAD). È stato standardizzato nel 1994 dal comitato ISO con il nome di "ISO 10303-21". ISO 10303-21 definisce il meccanismo di codifica per rappresentare i dati nel linguaggio di modellazione dei dati EXPRESS. Un file STEP è anche noto come p21-File e STEP Physical File. Le estensioni di file utilizzate per il file STEP sono .stp e .step.

## Storia di base

Nel 1994 è stata emessa la specifica originale della Parte 21. Ha alcuni bug che sono stati corretti dalla rettifica tecnica emessa nel 1996. La seconda edizione è stata pubblicata nel 2002 che includeva la rettifica e le estensioni per diverse sezioni di dati. La terza edizione è stata pubblicata nel 2016 che ha aggiunto sezioni di ancoraggio e riferimento che consentivano di archiviare entità e valori in file esterni. È stato aggiunto il supporto UTF-8 delle stringhe. Sono state aggiunte firme digitali per verificare il contenuto del file e per convalidare le credenziali. È stato inoltre aggiunto il supporto per la compressione e la memorizzazione della struttura di scambio tramite ZIP.

## Formato file STEP

Il formato di testo normale per un file STEP è costituito da una sequenza di record. Il set di caratteri è definito come punti di codice della ISO 10646. "ISO-10303-21;" sono i primi caratteri nel primo record. I commenti sono racchiusi tra i caratteri "/*" e "*/". L'ultimo record contiene "END-ISO-10303-21;" se il file STEP è conforme alla versione 2002. Nel caso sia conforme alla versione 2016, potrebbero esserci una o più firme digitali dopo "END-ISO-10303-21;" terminatore. Le interruzioni di riga sono indicate con "\N\" e le interruzioni di pagina con "\F\".

Il file STEP è diviso in sezioni e i loro nomi sono termini riservati. Tutte le sezioni terminano con il record "ENDSEC" e devono essere nell'ordine mostrato di seguito.

- **HEADER**: questa è una sezione obbligatoria e non ripetibile. Si compone delle seguenti entità:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: è una sezione opzionale non ripetitiva introdotta nella versione 2016. Definisce i nomi esterni per le istanze in modo che possano essere referenziati.
- **RIFERIMENTO**: è una sezione facoltativa non ripetitiva introdotta anche nella versione 2016. Ogni voce in questa sezione associa un nome istanza voce/valore a un'istanza/valore in un file esterno.
- **DATI**: è una sezione ripetibile facoltativa che contiene il contenuto principale dell'istanza del modello.
- **SIGNATURE**: è una sezione ripetibile opzionale introdotta nella versione 2016. Contiene la firma digitale per verificare il contenuto del file o per convalidare le credenziali.

## Riferimenti

- [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)

