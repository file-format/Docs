{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "file", "estensione", "format", "audio", "smaf", "estensione mmf", "file mmf", "file musicale mobile", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file MMF e le API che possono creare e aprire file MMF.",
  "title" :"MMF - Formato file musicale mobile",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## Che cos'è un file MMF?

MMF è un'estensione di file associata a un file SMAF. MMF sta per Mobile Music File mentre SMAF sta per Mobile Application Format di musica sintetica. I file MMF all'interno di uno smartphone contengono suonerie di sistema, suoni e possono anche contenere grafica e display di testo. L'MMF contiene inoltre tre tipi di parametri dello strumento, inclusi FM, PCM e Stream PCM. Questi formati di file sono compatibili con la piattaforma di sistema Windows. I file MMF sono classificati come file di dati. In genere, Microsoft Mail supporta i file MMF. Il file con suffisso MMF può essere copiato su qualsiasi dispositivo mobile o piattaforma di sistema.

Inoltre, questi file sono di dimensioni molto inferiori rispetto ai file in formato MIDI standard. I file [WAV](/it/audio/wav/) e [MID](/it/audio/mid/) possono essere convertiti in formato MMF che può essere quindi condiviso e distribuito come contenuto audio. Questi file possono essere ricevuti via e-mail direttamente su telefoni e PC.


## Breve storia del formato di file MMF

Yamaha ha sviluppato strumenti SMAF come file audio in modo che gli smartphone possano memorizzare un numero maggiore di suonerie uniche. Yamaha ha introdotto SMAF con la produzione dei chip audio MA-1, MA-2, MA-3, MA-5 e MA-7 LSI. Tutti questi formati sono diventati abbastanza familiari tra i telefoni cellulari nel mercato dell'Asia orientale all'inizio del 2000.

A livello internazionale, il formato MMF è stato autorizzato da Samsung. Con l'aiuto del formato MMF, Samsung è stata in grado di progettare un'ampia gamma di suonerie polifoniche da utilizzare negli smartphone Samsung.

Yamaha voleva rendere il formato ancora più popolare e così sui file SMAF ufficiali Yamaha, ha pubblicato più strumenti compatibili con questo formato. Con questo gli utenti possono ora riprodurre facilmente file MMF sui loro computer.


## Specifiche del formato file MMF ##

I file MMF sono classificati in sezioni di dati. Per descrivere ciascun segmento viene utilizzata una struttura prefissata attorno a un 8 byte.
L'etichetta a 4 byte include CNTI, OPDA, MSTR, MTR e ATR. La dimensione dei dati più 8 byte è la dimensione del blocco; l'intera dimensione del file viene calcolata sommando tutte le dimensioni dei blocchi. Se un file non è stato danneggiato, la dimensione del file sommata dovrebbe essere la stessa della dimensione dell'intestazione principale.

### Intestazione ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

Ecco un esempio di file MMF:

![](../mmf.png)

## Riferimenti

* [MMF - Di Wikipedia](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

