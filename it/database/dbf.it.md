{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "estensione", "file dbf", "formato file dbf", "Tipo file database", "Formato file database", "che cos'è un file dbf", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file DBF e le API che possono creare e aprire file DBF.",
  "title" :"DBF - File di database dBase",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Che cos'è un file DBF?
Il file con estensione .dbf è un file di database utilizzato da un'applicazione del sistema di gestione dei database denominata **dBASE**. Inizialmente, il database dBASE era chiamato Project Vulcan; iniziato da **Wayne Ratliff** nel 1978. Il tipo di file DBF è stato introdotto con dBASE II nel 1983. Organizza più record di dati con campi di tipo Array. Il software database **xBase** che è popolare per la sua compatibilità con un'ampia gamma di formati di file; supporta anche i file DBF.

## Formato file DBF
Il formato di file DBF appartiene al sistema di gestione del database dBASE ma potrebbe essere compatibile con xBase o altri software DBMS. La versione iniziale del file dbf consisteva in una semplice tabella che poteva avere dati aggiunti, modificati, eliminati o stampati utilizzando il set di caratteri ASCII. Con il passare del tempo .dbf è stato migliorato e sono stati aggiunti file aggiuntivi per aumentare le funzionalità e le capacità del sistema di database.

Nel moderno dBASE un file DBF è costituito da un'intestazione, i record di dati e l'indicatore EOF (End of File)

- L'intestazione contiene informazioni sul file, come il numero di record e il numero di tipi di campi utilizzati nei record.
- I record contengono i dati effettivi.
- La fine del file è contrassegnata da un singolo byte, con valore 0x1A.

### Intestazione del file
Il layout dell'intestazione del file in dBase è riportato nella tabella seguente:

| byte | Contenuto | Significato |
---|---|---|
| 0 | 1 byte | dBASE valido per file DOS; i bit 0–2 indicano il numero di versione, il bit 3 indica la presenza di un file memo dBASE per DOS, i bit 4–6 indicano la presenza di una tabella SQL, il bit 7 indica la presenza di un file memo (dBASE m PLUS o dBASE per DOS) |
| 1–3 | 3 byte | Data dell'ultimo aggiornamento; formattato come AAMMGG |
| 4–7 | numero a 32 bit | Numero di record nel file di database |
| 8–9 | numero a 16 bit | Numero di byte nell'intestazione |
| 10–11 | numero a 16 bit | Numero di byte nel record |
| 12–13 | 2 byte | Riservato; riempi con 0 |
| 14 | 1 byte | Flag che indica transazione incompleta[nota 1] |
| 15 | 1 byte | Flag di crittografia[nota 2] |
| 16–27 | 12 byte | Riservato per dBASE per DOS in un ambiente multiutente |
| 28 | 1 byte | Flag del file .mdx di produzione; 1 se è presente un file .mdx di produzione, 0 in caso contrario |
| 29 | 1 byte | ID del driver della lingua |
| 30–31 | 2 byte | Riservato; riempi con 0 |
| 32–n [nota 3][nota 4] | 32 byte ciascuno | array di descrittori di campo (vedi sotto per il layout dei descrittori) |
| n + 1 | 1 byte | 0x0D come terminatore di matrice del descrittore di campo |

- La funzione ISMARKEDO controlla questo flag (BEGIN TRANSACTION lo imposta a 1, END TRANSACTION e ROLLBACK lo reimposta a 0).
- Se questo flag è impostato su 1, viene visualizzato il messaggio Database crittografato.
- Il numero massimo di campi è 255.
- n indica l'ultimo byte nell'array del descrittore di campo.

### Matrice del descrittore di campo
Disposizione dei descrittori di campo in dBASE:

| byte | Contenuto | Significato |
---|---|---|
| 0–10 | 11 byte | Nome del campo in ASCII (riempito con zero) |
| 11 | 1 byte | Tipo di campo. Valori consentiti: C, D, F, L, M o N (per i significati vedere la tabella successiva) |
| 12–15 | 4 byte | Riservato |
| 16 | 1 byte | Lunghezza campo in formato binario (massimo 254 (0xFE)). |
| 17 | 1 byte | Conteggio decimale campo in binario |
| 18–19 | 2 byte | ID area di lavoro |
| 20 | 1 byte | Esempio |
| 21–30 | 10 byte | Riservato |
| 31 | 1 byte | Bandiera di campo MDX di produzione; 1 se il campo ha un tag di indice nel file MDX di produzione, 0 in caso contrario |

### Record di database
Ogni record inizia con un flag di eliminazione (1 byte). I campi vengono inseriti in record senza separatori di campo. Tutti i dati del campo sono ASCII. A seconda del tipo di campo, l'applicazione impone ulteriori restrizioni. Ecco i tipi di campo in dBase:

| Tipo di campo | mnemonico | Cosa accetta |
-------|-----|----|
| C | Carattere | Qualsiasi testo ASCII (riempito con spazi fino alla lunghezza del campo) |
| D | Data | Numeri e un carattere per separare mese, giorno e anno (memorizzati internamente come 8 cifre nel formato AAAAMMGG) |
| F | Virgola mobile | -, ., 0–9 (giustificato a destra, riempito con spazi bianchi) |
| L | logico | Y, y, N, n, T, t, F, f o ? (se non inizializzato) |
| M | promemoria | Qualsiasi testo ASCII (memorizzato internamente come 10 cifre che rappresentano un numero di blocco .dbt, giustificato a destra, riempito con spazi bianchi) |
| N | numerico | -, ., 0–9 (giustificato a destra, riempito con spazi bianchi) |









## Riferimenti ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

