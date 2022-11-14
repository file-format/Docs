{
  "date" : "2019-10-11",
  "keywords" :[ "file mpx", "formato file mpx", "cos'è un file mpx", "file", "esempio mpx", "estensione file mpx", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPX - Formato file Microsoft Project Exchange",
  "description":"Scopri il formato di file MPX e le API che possono creare e aprire file MPX.",
  "linktitle" : "MPX",
  "menu" : {
    "docs" : {
      "parent" : "project-management"
}
},
  "lastmod" : "2021-05-07"
}

## Che cos'è un file MPX? ##

Un file con estensione .mpx è un formato di file di Microsoft Exchange. Un formato di file MPX è stato sviluppato da Microsoft Project (MSP) per facilitare lo scambio di informazioni sul progetto tra MSP e altre applicazioni che supportano il formato di file MPX, inclusi Primavera Project Planner, Sciforma e Timerline Precision Estimating. Utilizzando i file MPX, è possibile trasferire tutti i tipi di informazioni da un progetto a un sistema diverso, come informazioni dettagliate sull'assegnazione delle risorse, informazioni sul calendario o informazioni dalla finestra di dialogo Informazioni sul progetto.

Microsoft Project 4.0 ha introdotto il supporto per la creazione e la lettura di formati di file MPX che hanno continuato a essere utilizzati tramite Microsoft Project 98. Tuttavia, il supporto per la creazione di file MPX ha interrotto il rilascio di Microsoft Project 2000 e le versioni fino a Microsoft Project 2010 supportano solo la lettura MPX. Il formato file MPX non è supportato nelle versioni successive a MSP 2010.

## Formato file MPX ##

In questa sezione viene fornita una panoramica delle specifiche del file MPX. Le specifiche complete sono disponibili in questa [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) articolo e si può fare riferimento per i dettagli.

### Record ###

Un record del file MPX è costituito da informazioni per il progetto. Esistono diversi tipi di record in cui ogni record ha il proprio ordine. Ogni tipo di record è identificato dal suo numero di record. Per un file MPX, è necessario contenere il tipo di record Creazione file. Altri tipi di record non sono obbligatori. La tabella seguente mostra tutti i tipi di record, i relativi numeri di record e il numero di record che ciascun tipo può contenere nel file MPX. L'inclusione del record nel file MPX deve seguire l'ordine della tabella, con i commenti inseriti ovunque.

|Nome record|Numero record|Numero massimo di record
---|---|---|
|Creazione file (richiesto)|nessuno|1
|Impostazioni valuta|10|1
|Impostazioni predefinite|11|1
|Impostazioni data e ora|12|1
|Definizione del calendario di base|20|250
|Ore di calendario di base|25| 7 per record di definizione del calendario di base
|Eccezione calendario di base|26| 250 per record di definizione del calendario di base
|Intestazione progetto|30|1
|Definizione della tabella delle risorse di testo|140|1- (oppure puoi utilizzare il record di definizione della tabella delle risorse numeriche)
|Definizione della tabella delle risorse numeriche|41|1
|Risorsa|50|9.999
|Note sulle risorse|51| 1 per record di risorse
|Definizione del calendario delle risorse|55| 1 per record di risorse
|Orari del calendario delle risorse|56| 7 per Calendario delle risorse
|Eccezione calendario risorse| 57|250 per Calendario delle risorse
|Definizione tabella attività di testo|60|1 (oppure puoi utilizzare il record Definizione tabella attività numerica)
|Definizione tabella attività numerica|61|1
|Compito|70|9
|Note sull'attività|71| 1 per record di attività
|Attività ricorrente|72| 1 per record di attività
|Assegnazione risorse|75| 100 per record di attività
|Campi gruppo di lavoro assegnazione|76| 1 per record di incarico
|Nomi dei progetti|80|500
|Collegamenti client DDE e OLE|81|500
|Commenti|0|illimitato

### Struttura del file ###

Un file MPX è costituito dai record sopra menzionati che sono disposti in modo preimpostato all'interno del file. I dettagli su questi tipi di record sono discussi come segue:

**File Creation Record (FCR):** Questo è un record obbligatorio il cui scopo è identificare:

* Formato file (MPX)
* Elenca il carattere separatore utilizzato nel file
* Programma e numero di versione utilizzati per creare il file
* Numero di versione del formato file MPX utilizzato nel file
* Codepage utilizzata per creare il file

Questo deve essere il primo record nel file. Quando si esporta da Microsoft Project, il carattere separatore di elenco viene specificato nell'elemento Impostazioni internazionali nel Pannello di controllo di Windows. Un record FCR include i seguenti campi:

* MPX seguito immediatamente dal carattere separatore dell'elenco
* Nome/Identificatore del programma
* Numero di versione del file
* Code Page (850, 437, MAC, ANSI)

Ad esempio, il record può contenere informazioni **MPX, Microsoft Project, 3.0**, che specificano che viene utilizzata una virgola come carattere separatore di elenco in questo file MPX. La versione del formato MPX utilizzato nel file viene esportata da Microsoft Project versione 3.0.

**Impostazioni valuta** Questo record, con numero di record 10, specifica le impostazioni per le opzioni di valuta nella finestra di dialogo Opzioni. Se questo record non è incluso, vengono utilizzate le impostazioni correnti nella finestra di dialogo Opzioni. I separatori delle migliaia e dei decimali sono specificati nella voce Impostazioni internazionali nel Pannello di controllo di Windows.
I campi inclusi in questo record sono:

* Simbolo di valuta
* Posizione del simbolo (0 # dopo, 1 # prima, 2 # dopo con uno spazio, 3 # prima con uno spazio)
* Cifre valuta (0,1,2)
* Separatore di migliaia
* Separatore decimale

**Esempio:** 10,$,1,2,",",.
Questo esempio specifica che i valori di valuta includono un simbolo del dollaro ($) prima di essi, che due cifre sono incluse dopo la virgola decimale, che una virgola viene utilizzata per separare le migliaia e che un punto viene utilizzato come punto decimale. Poiché il carattere separatore di elenco è incluso nel campo Separatore di migliaia, il campo è racchiuso tra virgolette.

**Impostazioni predefinite:** questo record, con il numero di record 11, specifica le impostazioni per le opzioni predefinite nella finestra di dialogo Opzioni. Se non viene specificata una durata, è necessario impostare l'unità di durata predefinita per calcolare correttamente l'unità di durata. Se questo record non è incluso, vengono utilizzate le impostazioni correnti nella finestra di dialogo Opzioni.
I campi inclusi in questo record sono:

* Unità di durata predefinite (0 # minuti, 1 # ore, 2 # giorni, 3 # settimane)
* Tipo di durata predefinito (0 # non fisso, 1 # fisso)
* Unità di lavoro predefinite (0 # minuti, 1 # ore, 2 # giorni, 3 # settimane)
* Orario/giorno predefinito
* Orario/settimana predefinito
* Tariffa standard predefinita
* Tasso di lavoro straordinario predefinito
* L'aggiornamento dello stato delle attività Aggiorna lo stato delle risorse (0 # no, 1 # sì)
* Dividi le attività in corso (0 # no, 1 # sì)

**Impostazioni di data e ora:** questo record, con il numero di record 12, specifica le impostazioni per le opzioni di data e ora nella finestra di dialogo Opzioni e l'opzione Formato data testo a barre nella finestra di dialogo Layout. Se questo record non è incluso, vengono utilizzate le impostazioni correnti nella finestra di dialogo Opzioni.
\\I campi inclusi in questo record sono:

* Ordine di data (0 # mese/giorno/anno, 1 # giorno/mese/anno, 2 # anno/mese/giorno)
* Formato ora (0 # 12 ore, 1 # 24 ore)
* Default Time (numero di minuti dopo la mezzanotte)
* Separatore di data
* Separatore di tempo
* Dalle 0:00 alle 11:59 Testo
* Dalle 12:00 alle 23:59 Testo
* Formato data (0 -14)*
* Formato data testo barra (0 -194)*

**Definizione del calendario di base:** Questi record, con numero di record 20, definiscono i calendari di base e i relativi giorni lavorativi e non lavorativi della settimana. Le impostazioni predefinite vengono utilizzate se non ci sono voci per un giorno. Le impostazioni predefinite sono dal lunedì al venerdì per i giorni lavorativi e il sabato e la domenica per i giorni non lavorativi. In questo record, il campo Nome è obbligatorio. Per ciascuno dei giorni, una voce 0 indica che il giorno è un giorno non lavorativo e una voce 1 indica che il giorno è un giorno lavorativo.
I campi inclusi in questo record sono:

* Nome
* Domenica
* Lunedi
* Martedì
* Mercoledì
* Giovedì
* Venerdì
* Sabato

**Ore di calendario di base:** Questi record, con numero di record 25, specificano l'orario di lavoro per i giorni della settimana se differiscono dalle impostazioni predefinite. L'orario di lavoro predefinito è dalle 8:00 alle 12:00 e dalle 13:00 alle 17:00. Ciascun record delle ore di calendario di base si riferisce al record di definizione del calendario di base precedente. Fino a sette di questi record possono seguire ogni record di definizione del calendario di base.

* Giorno della settimana (1 - 7, dove 1#domenica e 7#sabato)
* Dal tempo 1
* Al tempo 1
* Dall'ora 2
* Al tempo 2
* Dall'ora 3
* Al tempo 3

**Eccezione calendario di base:** questi record, con numero di record 26, definiscono le eccezioni ai giorni e alle ore specificati nei due tipi di record precedenti. Fino a 250 di questi record possono seguire ogni record di definizione del calendario di base. Questi record devono essere elencati in ordine cronologico. Se un'eccezione è un giorno, puoi lasciare vuoto il campo Fino alla data. Se non vengono indicati orari, vengono utilizzati gli orari predefiniti dalle 8:00 alle 12:00 e dalle 13:00 alle 17:00.
I campi inclusi in questo record sono:

* Dalla data
* Ad oggi
* Non lavorativo/lavorativo (0 # non funzionante, 1 # funzionante)
* Dal tempo 1
* Al tempo 1
* Dall'ora 2
* Al tempo 2
* Dall'ora 3
* Al tempo 3

**Intestazione del progetto:** questo record, con valore del record 30, imposta i campi globali del progetto, come la data di inizio del progetto e la data di fine del progetto. I campi in questo record corrispondono alle informazioni nelle finestre di dialogo Informazioni sul progetto e Statistiche.
I campi e le schede inclusi in questo record sono:

* Scheda Progetto
* Azienda
* Gestore
* Calendario (standard utilizzato se nessuna voce)
* Data di inizio (questo campo o il campo successivo viene calcolato per un file importato, a seconda dell'impostazione Pianifica da)
* Data di fine
* Programma da (0 # inizio, 1 # arrivo)
* Data odierna*
* Commenti
* Costo
* Costo di base
* Costo attuale
* Opera
* Lavoro di base
* Lavoro effettivo
* Opera
* Durata*
* Durata di riferimento*
* Durata effettiva
* Percentuale di completamento
* Inizio linea di base
* Finitura di base
* Inizio effettivo
* Finitura effettiva
* Inizia varianza
* Finitura varianza
* Materia
* Autore
* Parole chiave

**Definizione della tabella delle risorse di testo**: questo record elenca i campi delle risorse, in ordine, che vengono importati o esportati. Per i file importati, i nomi devono corrispondere ai nomi dei campi utilizzati in Microsoft Project. Per i file esportati, questo record proviene dalla tabella Export delle risorse. È necessario utilizzare questo record o il record Definizione tabella risorse numerica. Quando si esporta da Microsoft Project, vengono inclusi entrambi questi record.

**Definizione della tabella delle risorse numeriche:** Utilizzando numeri anziché nomi, questo record elenca i campi delle risorse, in ordine, che vengono importati o esportati. Questo è un metodo alternativo per identificare i campi di risorse inclusi in ciascun record di risorse ed è utile quando si definisce un file MPX creato da un prodotto in lingua straniera.

**Risorsa:** questi record contengono le informazioni per ciascuna risorsa importata o esportata. Ogni record di Risorsa descrive una risorsa. Quando si importano le informazioni, i campi inclusi vengono definiti dal record Definizione tabella risorse di testo o Definizione tabella risorse numeriche. Quando esporti le informazioni, i campi inclusi sono quelli elencati nella tabella Esporta risorse.

**Note sulla risorsa:** questi record contengono note sul record della risorsa immediatamente precedente. Per una nuova riga all'interno della nota, viene utilizzato il carattere ASCII 127. Se la nota include il carattere separatore di elenco, racchiudere la nota tra virgolette.

**Definizione del calendario della risorsa:** questi record definiscono i giorni lavorativi per la risorsa specificata nel record della risorsa immediatamente precedente. Per i file importati, se non è presente alcuna voce per il campo Nome calendario di base, viene utilizzato Standard. Nessuna voce per il giorno specifico indica che il giorno è impostato sul valore predefinito (2). Se non sono presenti record di definizione del calendario delle risorse, Standard viene utilizzato come calendario di base per la risorsa, con l'impostazione predefinita utilizzata per i giorni. Per ciascuno dei giorni, una voce 0 indica che il giorno è un giorno non lavorativo, 1 indica che il giorno è un giorno lavorativo e 2 specifica che viene utilizzata l'impostazione predefinita.

**Ore del calendario della risorsa:** questi record definiscono l'orario di lavoro per la risorsa che differisce dal calendario di base utilizzato dalla risorsa. Questi record si applicano al record Resource Calendar Definition immediatamente precedente a questo record. Fino a sette di questi record possono seguire ogni record di definizione del calendario delle risorse.

**Eccezione calendario risorse:** questi record definiscono le eccezioni ai giorni e alle ore specificati nei due tipi di record precedenti. Fino a 250 di questi record possono seguire ogni record di definizione del calendario delle risorse. Questi record devono essere elencati in ordine cronologico. Se l'eccezione riguarda solo un giorno, puoi lasciare vuoto il campo Fino alla data. Se non vengono indicati orari, vengono utilizzati gli orari predefiniti dalle 8:00 alle 12:00 e dalle 13:00 alle 17:00.

**Definizione tabella attività di testo:** Questo record elenca i campi attività, in ordine, che vengono importati o esportati. Per i file importati, i nomi devono corrispondere ai nomi dei campi utilizzati in Microsoft Project. Se il file viene esportato, questo record proviene dalla tabella Esporta attività. Quando si esporta da Microsoft Project, vengono inclusi entrambi questi record. I campi calcolati da Microsoft Project, ad esempio Inizio programmato e Fine programmato, vengono ignorati se importati. Se le date di inizio o fine dell'attività sono fisse, utilizzare i campi Tipo di vincolo e Data di vincolo.

**Definizione tabella attività numerica:** Utilizzando numeri anziché nomi, questo record elenca i campi attività, in ordine, che vengono importati o esportati. Questo è un metodo alternativo per identificare i campi delle attività inclusi in ciascun record delle attività ed è utile quando si definisce un file MPX creato da un prodotto in lingua straniera.

**Attività:** questi record contengono le informazioni per ciascuna attività importata o esportata. Ogni record di attività descrive un'attività. Quando si importano le informazioni, i campi inclusi sono definiti dal record Definizione tabella attività di testo o dal record Definizione tabella attività numerica. Quando esporti le informazioni, i campi inclusi sono quelli elencati nella tabella Esporta attività.

**Note sull'attività:** questi record contengono note sul record dell'attività immediatamente precedente. Utilizzare il carattere ASCII 127 per indicare una nuova riga all'interno della nota. Se la nota include il carattere separatore di elenco, racchiudere la nota tra virgolette.

**Assegnazione delle risorse**: questi record elencano le informazioni sulle risorse assegnate all'attività definita nel record dell'attività precedente. Se si uniscono file e si desidera conservare le informazioni sull'assegnazione delle risorse, è necessario includere le informazioni nel file MPX. Se esegui l'unione, tutte le assegnazioni esistenti sulle attività unite verranno eliminate. Se si uniscono file in base a ID univoci, le risorse vengono assegnate utilizzando gli ID univoci delle risorse anziché gli ID.

**Campi gruppo di lavoro assegnazione risorse:** questi record elencano le informazioni archiviate con ogni assegnazione per le funzionalità gruppo di lavoro di Microsoft Project 4.0 e 4.1. Se si utilizzano le funzionalità del gruppo di lavoro, è necessario includere questo record per assicurarsi che nessuna delle informazioni vada persa.

**Nomi progetto:** Questi record elencano tutti i nomi dei collegamenti DDE memorizzati nel progetto.

**Collegamenti client DDE e OLE:** Questi record elencano i collegamenti DDE nel progetto.

**Commenti:** questi record possono essere utilizzati per aggiungere commenti al file e possono apparire in qualsiasi posizione nel file. Ogni record Commenti deve iniziare con uno "0".

## Problemi per aprire un file MPX ##

Ecco l'elenco di alcuni problemi comuni che possono sorgere e causare il malfunzionamento del formato MPX:

* Assenza di software di supporto
* File corrotto
* File infetto a causa di virus
* Nessun diritto di accesso nel sistema per aprire i file
* Unità obsoleta nel tuo sistema
* L'estensione del file viene rinominata

## Riferimenti ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)

