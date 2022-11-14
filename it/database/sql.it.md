{
  "date" : "2020-11-11",
  "keywords" :[ "SQL", "estensione", "file", "formato file", "Tipo file database", "Formato file database", "File database" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file SQL e le API che possono creare e aprire file SQL.",
  "title" :"Formato file SQL - Un file di dati del linguaggio di query strutturato",
  "linktitle" : "SQL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Che cos'è un file SQL?

Un file con estensione .sql è un file SQL (Structured Query Language) che contiene il codice per lavorare con i database relazionali. Viene utilizzato per scrivere istruzioni SQL per operazioni CRUD (Crea, Leggi, Aggiorna ed Elimina) sui database. I file SQL sono comuni quando si lavora con database desktop e Web. Esistono diverse alternative a SQL come Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL e molti altri. I file SQL possono essere aperti da editor di query di Microsoft SQL Server, MySQL e altri editor di testo normale come Blocco note sul sistema operativo Windows.

## Breve storia

* Sviluppato e introdotto da Donal D. Chamberlin e Raymond F. Boyce presso IBM all'inizio degli anni '70
* Utilizzato per archiviare e recuperare i dati dal sistema di gestione del database quasi relazionale originale di IBM, System R
* Iniziato ad essere utilizzato nella base di prodotti commerciali con il prototipo System R, inclusi System/38, SQL/DS e DB2, che erano disponibili in commercio rispettivamente nel 1979, 1981 e 1983.
* Adottato ufficialmente dai gruppi di standard ANSI e ISO come standard "Database Language SQL" per i sistemi di gestione di database relazionali (RDBMS) entro il 1986

## Formato file SQL

I file SQL sono in formato testo normale e possono comprendere diversi elementi del linguaggio. È possibile aggiungere più istruzioni a un singolo file SQL se la loro esecuzione è possibile senza dipendere l'una dall'altra. Questi comandi SQL possono essere eseguiti da editor di query per eseguire operazioni CRUD.

### Elementi del linguaggio SQL

Gli elementi del linguaggio SQL sono elencati di seguito.

|Elemento|Descrizione|
---|---|
|Clausole| Componenti costitutivi di dichiarazioni e query.|
|Espressioni| Può produrre valori scalari o tabelle costituite da colonne e righe di dati|
|Predicati| Specifica le condizioni che possono essere valutate in base alla logica a tre valori SQL (3VL) (vero/falso/sconosciuto) o ai valori di verità booleani e vengono utilizzate per limitare gli effetti di istruzioni e query o per modificare il flusso del programma.|
|Domande| Recupera i dati in base a criteri specifici. Questo è un elemento importante di SQL.|
|Dichiarazioni| Può avere un effetto persistente su schemi e dati o può controllare transazioni, flusso di programma, connessioni, sessioni o diagnostica.|

### Esempio SQL
La seguente istruzione SQL crea una tabella denominata **DATA**, seguita da ulteriori comandi `INSERT` per inserire i record in questa tabella.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Riferimenti ##

* [SQL di Wikipedia](https://en.wikipedia.org/wiki/SQL)
* [Sintassi SQL](https://en.wikipedia.org/wiki/sintassi_SQL)

