{
  "date" : "2021-08-31",
  "keywords" :[ "file xbe", "formato file xbe", "cos'è un file xbe", "file", "esempio xbe", "estensione file xbe", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file XBE e le API che possono creare e aprire file XBE.",
  "title" :"XBE - File del pacchetto dell'applicazione iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## Che cos'è un file XBE?
Un file con estensione .xbe è un'applicazione eseguibile da un disco di videogiochi Xbox. I file XBE sono i file principali che vengono eseguiti nel sistema Xbox e non dovrebbero essere aperti in genere su un computer, ma possono essere aperti su un PC utilizzando un programma di emulazione Xbox. Questi file vengono in genere creati dagli sviluppatori di giochi e quindi firmati da Microsoft. La struttura del file è simile ai file di Windows PE, ma vengono applicate alcune modifiche importanti in base alle impostazioni di XBox per renderlo eseguibile su XBox.

## formato di file XBE
Il file XBE è composto da un'intestazione di immagine, una raccolta di intestazioni di sezione, un certificato, dati di archiviazione locale del thread, una raccolta di versioni della libreria, bitmap Microsoft e le sezioni che contengono il codice e le risorse.

### Intestazione immagine
L'intestazione dell'immagine comprende le informazioni che spiegano dove si trovano gli altri componenti dell'eseguibile all'interno del file e come trattare e caricare l'eseguibile.

### Tabella TLS
La tabella TLS è costituita da tutte le informazioni necessarie all'XBE per configurare correttamente l'archiviazione thread-local. È fondamentalmente unico per la directory TLS che si trova nei file PE32 e può essere copiato direttamente da lì. Questa tabella può essere omessa se il file XBE non utilizza alcun archivio thread-local e il rispettivo campo nell'intestazione dell'immagine è impostato su zero.

| Compensazione | Dimensioni | Nome | Descrizione |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Inizio dati grezzi | Indirizzo assoluto (cioè non RVA) di inizio dei dati variabili TLS nell'immagine del programma. |
| 0x0004 | 0x0004 | Fine dei dati grezzi | Indirizzo assoluto (cioè non RVA) di fine dei dati variabili TLS nell'immagine del programma. |
| 0x0008 | 0x0004 | Indirizzo dell'Indice | Indirizzo assoluto (cioè non RVA) della variabile Indice TLS. |
| 0x000C | 0x0004 | Indirizzo delle richiamate | Indirizzo assoluto (cioè non un RVA) della tabella delle funzioni di callback TLS con terminazione null. |
| 0x0010 | 0x0004 | Dimensione del riempimento zero | Il numero di byte che seguono i dati grezzi che devono essere impostati su zero in memoria. |
| 0x0014 | 0x0004 | Caratteristiche | Descrive l'allineamento. |

### Certificato

Un certificato è obbligatorio per ogni eseguibile Xbox che contiene informazioni sui titoli:
 


- Ora e data di creazione del certificato
- ID del titolo
- Nome del titolo
- ID titolo alternativi
- Tipi di supporto consentiti da cui è possibile eseguire l'eseguibile (HD, DVD, CD, ecc.)
- Regione di gioco
- Valutazioni del gioco
- Numero del disco
- Versione
- Dati grezzi chiave LAN utilizzati per System Link
- Dati grezzi della chiave di firma (usati per firmare i salvataggi)
- Chiavi di firma alternative
- Dimensioni originali del certificato
- Nome del servizio online (non presente nei primi eseguibili)
- Flag di sicurezza runtime (non presenti nei primi eseguibili)
 


### Tipi di media consentiti
Tipi di supporto da cui è consentito eseguire l'eseguibile. Sono noti i seguenti valori:
| Tipo di supporto | Valore |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| CD_DVD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| SCHEDA_MEDIA | 0x00000200 |
| NON SECURE_HARD_DISK | 0x40000000 |
| MODALITÀ_NON SICURA | 0x80000000 |
| MASCHERA_MEDIA | 0x00FFFFFF |

### Sezioni
Le sezioni sono espresse dalle intestazioni delle sezioni. Le intestazioni delle sezioni iniziano subito dopo il certificato e contengono informazioni in cui nel file esistono le sezioni effettive. Almeno due sezioni sono sempre presenti in un eseguibile Xbox:


- .testo


- .rdata


## Riferimenti



* [Xbe - Eseguibile XBox](https://xboxdevwiki.net/Xbe)


