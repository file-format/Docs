{
  "date" : "2019-12-13",
  "keywords" :[ "WAV", "file", "estensione", "formato", "formato file di interscambio audio", "musica" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file WAV e le API che possono creare e aprire file WAV.",
  "title" :"WAV - Formato file audio forma d'onda",
  "linktitle" : "WAV",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2019-12-13"
}

## Che cos'è un file WAV?

WAV, noto per WAVE (Waveform Audio File Format), è un sottoinsieme della specifica RIFF (Resource Interchange File Format) di Microsoft per la memorizzazione di file audio digitali. Il formato non applica alcuna compressione al flusso di bit e memorizza le registrazioni audio con frequenze di campionamento e bitrate differenti. È stato ed è uno dei formati standard per i CD audio. I file Wave sono di dimensioni maggiori rispetto ai nuovi formati di file audio come [MP3](/it/audio/mp3/) che utilizza la compressione con perdita di dati per ridurre le dimensioni del file mantenendo la stessa qualità audio. Tuttavia, i file WAV possono essere compressi utilizzando i codec Audio Compression Manager (ACM). Sono disponibili diverse API e applicazioni in grado di convertire file WAV in altri formati di file audio popolari.

**Lo sapevate?**
Puoi diventare un collaboratore su FileFormat.com per mantenere la comunità dei formati di file aggiornata con i tuoi risultati. Se devi condividere qualcosa sui formati di file WAV o Audio, puoi pubblicare i tuoi risultati nella sezione [Notizie sui formati di file audio](https://news.fileformat.com/t/audio) affinché le persone rimangano aggiornate.

## Formato file WAV ##

Il formato di file WAVE, essendo un sottoinsieme della specifica RIFF di Microsoft, inizia con un'intestazione di file seguita da una sequenza di blocchi di dati. Un file WAVE ha un singolo blocco "WAVE" che consiste in due sottogruppi:

* un blocco "fmt" - specifica il formato dei dati
* un blocco "dati" - contiene i dati di esempio effettivi

### Intestazione del file WAV ###

L'intestazione di un file WAV (RIFF) è lunga 44 byte e ha il seguente formato:


|Posizioni|Valore campione|Descrizione
---|---|---|
|1 - 4|"RIFF"|Segna il file come un file riff. I caratteri sono lunghi 1 byte ciascuno.
|5 - 8|Dimensione del file (intero)|Dimensione del file complessivo - 8 byte, in byte (intero a 32 bit). In genere, lo compileresti dopo la creazione.
|9 -12|"WAVE"|Tipo file di intestazione. Per i nostri scopi, equivale sempre a "WAVE".
|13-16|"fmt "|Formatta l'indicatore di blocchi. Include null finale
|17-20|16|Lunghezza dei dati di formato come elencato sopra
|21-22|1|Tipo di formato (1 è PCM) - 2 byte intero
|23-24|2|Numero di canali - 2 byte intero
|25-28|44100|Frequenza di campionamento - Intero a 32 byte. I valori comuni sono 44100 (CD), 48000 (DAT). Frequenza di campionamento = Numero di campioni al secondo o Hertz.
|29-32|176400|(Frequenza di campionamento * Bit per campione * Canali) / 8.
|33-34|4|(BitsPerSample * Canali) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Bit per campione
|37-40|Intestazione del blocco "dati"|"dati". Contrassegna l'inizio della sezione dati.
|41-44|Dimensione file (dati)|Dimensione della sezione dati.
|I valori di esempio sono riportati sopra per una sorgente stereo a 16 bit.

## Riferimenti ##

* [WAV - Di Wikipedia](https://en.wikipedia.org/wiki/WAV)

