{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "file", "estensione", "format", "cos'è un file cda", "music", "formato file cda", "specifica del formato file cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file CDA e le API che possono creare, convertire e aprire file CDA.",
  "title" :"CDA - File di scelta rapida della traccia audio del CD",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Che cos'è un file CDA?

Un file con estensione .cda è un piccolo file stub generato da Microsoft Windows per ciascuna traccia audio su un CD audio. Questi file contengono informazioni tipiche come i tempi delle tracce e un collegamento di Windows che consente agli utenti di accedere a tracce audio specifiche. I file CDA non sono musica, ma puntano a un file musicale esistente da qualche parte nella memoria. Possiamo dirlo come una scorciatoia di un file audio che si trova su un CD.

## Formato file CDA

Il formato di file CDA viene utilizzato per dire a un computer quale file audio riprodurre su un CD. Quindi, i file CDA diventano inutili separati da un CD che rappresentano. I file CDA sono comunemente considerati risorse RIFF. C'è solo un blocco che si chiama "CDDA" e contiene un solo blocco di dati chiamato "FMT" nella versione corrente del file .cda. Questo blocco è lungo 24 byte. L'identificatore creato da Windows viene utilizzato dall'unità CD relativa a Windows 95 e Windows 98 e il suo lettore non può connettersi a FreeDB o CDDB. In modo che possa visualizzare il titolo del brano e il nome dell'artista, che devi inserire manualmente queste informazioni nel file cdplayer.ini.

### Organizzazione di un file CDA

La tabella seguente mostra le informazioni sugli offset tipici:
| compensazione | lunghezza | contenuto |
---|---|---|
| 0x00 | 4 | i 4 caratteri ASCII "RIFF" |
| 0x04 | 4 | la dimensione del seguente blocco: sempre 36 (44 - 8), su 4 byte (ordine Intel) |
| 0x08 | 4 | identificatore del pezzo: i 4 caratteri ASCII "CDDA" |
| 0x0C | 4 | i 3 caratteri ASCII "fmt" seguiti da uno spazio |
| 0x10 | 4 | lunghezza del pezzo: sempre 24, su 4 byte (ordine Intel) |
| 0x14 | 2 | versione del formato CD, su 2 byte (ordine Intel). Nel maggio 2006, sempre pari a 1. |
| 0x016 | 2 | numero dell'intervallo, su 2 byte (Intel order). La prima traccia ha il numero 1. |
| 0x18 | 4 | identificatore calcolato da Windows per cdplayer.exe. |
| 0x1c | 4 | offset dell'intervallo, in numero di frame (ordine Intel) |
| 0x20 | 4 | durata della traccia, numero totale di frame (ordine Intel) |
| 0x24 | 1 | posizione dell'intervallo: cornici |
| 0x25 | 1 | posizione dell'intervallo: secondi |
| 0x26 | 1 | posizione dell'intervallo: minuti |
| 0x27 | 1 | un byte nullo (valore binario 0) |
| 0x28 | 1 | durata della traccia: frame |
| 0x29 | 1 | durata del brano: secondi |
| 0x2a | 1 | durata del brano: minuti |
| 0x2b | 1 | un byte nullo (valore binario 0) |

## Riferimenti

* [file .cda - di Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

