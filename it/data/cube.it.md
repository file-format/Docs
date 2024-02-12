{
  "date" : "2024-01-25",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "File CUBE - File cubo gaussiano - Cos'è il file .cube e come aprirlo?",
  "description" : "Scopri di più sul file cubo gaussiano e su come aprirlo.",
  "linktitle" : "CUBE",
  "menu" : {
    "docs" : {
      "identifier" : "data-it-cube",
      "parent" : "data"
    }
  },
  "lastmod" : "2024-01-25"
}

## Cos'è un file CUBE?

Il formato file CUBE, noto anche come file cubo gaussiano (.cube), viene utilizzato nella chimica computazionale per archiviare dati molecolari, in particolare informazioni sulla densità elettronica risultanti da calcoli di chimica quantistica. Questo formato è comunemente associato al **pacchetto software gaussiano**, ampiamente utilizzato per eseguire calcoli di strutture elettroniche ab initio.

I file del cubo gaussiano memorizzano dati tridimensionali, che in genere rappresentano la densità elettronica o altre proprietà delle molecole, ottenuti attraverso calcoli di chimica quantistica. Il file contiene una sezione di intestazione con metadati (come origine, numero di punti dati lungo ciascun asse e spaziatura), seguita da una griglia di valori numerici che rappresentano proprietà di interesse (ad esempio, densità elettronica) in ciascun punto della griglia nello spazio.

Il file cubo gaussiano (.cube) è un file di testo semplice con una struttura specifica. L'intestazione contiene informazioni sul sistema molecolare e sulla griglia di dati e i valori dei dati sono disposti in un formato di griglia tridimensionale. I file del cubo gaussiano vengono spesso utilizzati per visualizzare le proprietà molecolari utilizzando un software di visualizzazione molecolare. Programmi come **VMD (Visual Molecular Dynamics)** o **PyMOL** possono leggere file del cubo gaussiano per visualizzare superfici molecolari, densità elettronica o altre proprietà calcolate.

## Esempio semplificato di file del cubo gaussiano:

```
Esempio di file cubico
Generato da gaussiano
   0 1 0 0 0 0 0 0 0 0
   0.0000000000000000E+00 0.0000000000000000E+00 0.0000000000000000E+00
  50 0.1000000000000000E+01 0.0000000000000000E+00 0.0000000000000000E+00
  50 0.0000000000000000E+00 0.1000000000000000E+01 0.0000000000000000E+00
  50 0.0000000000000000E+00 0.0000000000000000E+00 0.1000000000000000E+01
    0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02 0,123456789E+02
    ... (valori dei dati per la densità elettronica in ciascun punto della griglia)
```

## Informazioni sulla gaussiana

Gaussian è una suite di applicazioni software per la chimica quantistica e la chimica computazionale. L'obiettivo principale di Gaussian è sui metodi di chimica quantistica ab initio, che sono approcci altamente accurati ma computazionalmente intensivi per studiare la struttura elettronica delle molecole. Il software è ampiamente utilizzato in contesti accademici e di ricerca per varie applicazioni, tra cui la previsione delle proprietà molecolari, lo studio dei meccanismi di reazione e l'esplorazione delle strutture molecolari.

## Informazioni su NWChem

NWChem è un software di chimica computazionale open source progettato per simulazioni di chimica quantistica ad alte prestazioni. Impiega metodi ab initio come Hartree-Fock e la teoria del funzionale della densità, supporta il calcolo parallelo per calcoli efficienti sui cluster e trova applicazioni in diversi campi scientifici, tra cui chimica computazionale, biochimica e scienza dei materiali. NWChem è noto per la sua versatilità, che consente ai ricercatori di studiare vari sistemi chimici, e la sua natura open source incoraggia i contributi e la personalizzazione della comunità.

## Informazioni su VMD

VMD, che sta per Visual Molecular Dynamics, è un programma di visualizzazione molecolare potente e ampiamente utilizzato per visualizzare, analizzare e animare traiettorie di dinamica molecolare (MD), nonché strutture molecolari statiche. È particolarmente popolare nei campi della chimica computazionale, della biologia molecolare e della bioinformatica strutturale. VMD eccelle nella visualizzazione delle strutture molecolari, fornendo rendering 3D di alta qualità di molecole e complessi molecolari. Supporta una varietà di formati di file molecolari.

## Informazioni su PyMOL

PyMOL è un sistema di visualizzazione molecolare e uno strumento software utilizzato per la visualizzazione tridimensionale di strutture molecolari. È particolarmente popolare nei campi della biologia strutturale, della bioinformatica e della chimica computazionale. PyMOL fornisce rendering 3D di alta qualità di strutture molecolari, consentendo agli utenti di visualizzare ed esplorare forme, superfici e interazioni di macromolecole biologiche.

## Come aprire il file CUBE?

Il file CUBE può essere aperto e referenziato utilizzando i seguenti programmi.

- **NWChem** (gratuito) per (Windows, MAC, Linux)

## Riferimenti
* [Formato file cubo gaussiano](https://paulbourke.net/dataformats/cube/)
