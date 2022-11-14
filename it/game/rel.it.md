{
  "date" : "2021-09-08",
  "keywords" :[ "file rel", "formato file rel", "che cos'è un file rel", "file", "esempio rel", "estensione file rel", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file REL e le API che possono creare e aprire file REL.",
  "title" :"REL - File del modulo rilocabile",
  "linktitle" : "REL",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Che cos'è un file REL?
Un file con estensione .rel può essere utilizzato per diversi tipi di scopi. Pertanto, in termini di classificazione del gioco, è noto come un file modulo riposizionabile utilizzato da alcuni giochi per Nintendo Wii, come Brawl, Super Smash Bros e Mario Kart Wii. Comprende i dati di gioco, inclusi i modelli dei personaggi e le fasi. I file REL funzionano in modo simile ai file .DLL utilizzati da Microsoft Windows.

## formato di file REL
In un formato di file REL, il file è diviso in più sezioni, raggruppate per accesso simile, ad esempio dati di sola lettura in una sezione, tutto il codice eseguibile è inserito in un'altra, ecc. Il file inizia con una sezione di intestazione, seguita da:
- Tabella contenente le informazioni sulla sezione.
- I dati della sezione.
- Informazioni sul trasferimento.

### Intestazione del file
Il file inizia con un'intestazione fino a 0x4C byte:
| Compensazione | Dimensioni | Nome campo | Descrizione |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Numero di identificazione arbitrario. Deve essere unico tra tutti i REL utilizzati da un gioco. Non deve essere 0. |
| 0x04 | 4 | successivo | Puntatore al modulo successivo, compilato in fase di esecuzione. |
| 0x08 | 4 | precedente | Puntatore al modulo precedente, compilato in fase di esecuzione. |
| 0x0c | 4 | numSezioni | Numero di sezioni nel file. |
| 0x10 | 4 | sezioneInfoOffset | Offset all'inizio della tabella delle sezioni. |
| 0x14 | 4 | nomeOffset | Offset alla stringa ASCII contenente il nome del modulo. Potrebbe essere NULLO. Relativo all'inizio del file REL. |
| 0x18 | 4 | nomeTaglia | Dimensione del nome del modulo in byte. |
| 0x1c | 4 | versione | Numero di versione del formato file REL. |
| 0x20 | 4 | bssSize | Dimensione della sezione '.bss'. |
| 0x24 | 4 | relOffset | Offset alla tabella di trasferimento. |
| 0x28 | 4 | impOffset | Offset alla tabella imp. |
| 0x2c | 4 | impSize | Dimensione della tabella imp in byte. |
| 0x30 | 1 | prologSezione | Indice nella tabella delle sezioni a cui è relativo il prologo. Salta se questo campo è 0. |
| 0x31 | 1 | epilogSezione | Indice nella tabella delle sezioni a cui è relativo l'epilogo. Salta se questo campo è 0. |
| 0x32 | 1 | sezione non risolta | Indice nella tabella delle sezioni a cui si riferisce l'irrisolto. Salta se questo campo è 0. |
| 0x33 | 1 | bssSezione | Indice nella tabella delle sezioni a cui bss è relativo. Riempito in fase di esecuzione! |
| 0x34 | 4 | prologo | Offset nella sezione specificata della funzione _prolog. |
| 0x38 | 4 | epilogo | Offset nella sezione specificata della funzione _epilog. |
| 0x3c | 4 | irrisolto | Offset nella sezione specificata della funzione _non risolta. |
| 0x40 | 4 | allineare | Solo versione ≥ 2. Vincolo di allineamento su tutte le sezioni, espresso come potenza di 2. |
| 0x44 | 4 | bssAlign | Solo versione ≥ 2. Vincolo di allineamento su tutte le sezioni '.bss', espresso come potenza di 2. |
| 0x48 | 4 | fixSize | Solo versione ≥ 3. Se REL è collegato con OSLinkFixed (anziché OSLink), lo spazio dopo questo indirizzo può essere utilizzato per altri scopi (come BSS). |

### Tabella delle informazioni sulla sezione
La tabella delle informazioni sulla sezione contiene voci **numSections** ciascuna lunga 0x8 byte:
| Compensazione | Dimensioni | Descrizione |
-------|------------|-------------|
| 0x0 | 30 bit | Offset dall'inizio del REL alla sezione. Se questo è zero, la sezione è una sezione non inizializzata (es. .bss). |
| 0x3.6 | 1 bit | Sconosciuto. |
| 0x3.7 | 1 bit | Flag eseguibile; se questo è 1 la sezione è eseguibile. |
| 0x4 | 4 | Lunghezza in byte della sezione. Se questo è zero, questa voce viene ignorata. |
| 0x8 | Voce successiva | Voce successiva |

### Dati di trasferimento
I dati di rilocazione sono uno o più elenchi di strutture di 0x8 byte. La fine di ogni lista è contrassegnata dal codice speciale di tipo 203:
| Compensazione | Nome | Dimensioni | Descrizione |
-------|------------|------------|-----|
| 0x0 | compensazione | 2 | Offset in byte dal trasferimento precedente a questo. Se questo è il primo trasferimento nella sezione, è relativo all'inizio della sezione. |
| 0x2 | tipo | 1 | Il tipo di trasferimento. Descritto sotto. |
| 0x3 | sezione | 1 | La sezione del simbolo contro cui riposizionare. Per il tipo di trasferimento speciale 202, questo è invece il numero della sezione di questo file a cui si applicano le seguenti voci di trasferimento. |
| 0x4 | aggiungere | 4 | Offset in byte del simbolo rispetto al quale riposizionare, rispetto all'inizio della sua sezione. Questo è invece un indirizzo assoluto per i traslochi contro main.dol. |
| 0x8 | Voce successiva | Voce successiva | Voce successiva |


 




## Riferimenti


* [Formato modulo oggetto rilocabile](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)


