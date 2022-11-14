{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Video audio compresso", "File", "Estensione", "Formato file", "Contenitore multimediale", "XVid", "DivX", "Codec", "Formato file interscambio risorse", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file AVI - Un file interleave audio video",
  "description":"Scopri il formato di file AVI e le API che possono creare e aprire file AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## Che cos'è un file AVI? ##

Il formato di file **AVI** è un formato di file contenitore multimediale Audio Video introdotto da Microsoft. Contiene i dati audio e video creati e compressi utilizzando diversi codec (Coder/Decoder) come **XVid** e **DivX**. Dato che diversi codec possono essere usati per codificare i contenuti AVI, le applicazioni di recupero, ad esempio i lettori AVI, dovrebbero essere in grado di aprirli solo se hanno installato i codec richiesti con cui sono stati creati i contenuti AVI. Il formato è supportato per impostazione predefinita su tutte le piattaforme **Microsoft Windows** e su quasi tutte le altre piattaforme principali. Diverse applicazioni e API offrono la possibilità di creare/salvare, leggere e convertire AVI in altri formati popolari come MP4, MOV, WMV, ecc.

## Formato file AVI ##

Un file con estensione .avi è un file AVI. È un sottoformato del Resource Interchange File Format (RIFF). RIFF organizza i dati in blocchi, o "blocchi", identificati con un tag FourCC. Un file AVI è semplicemente un "pezzo" in un file formattato RIFF.

Nel primo sub-chunk, l'intestazione del file è identificata dal tag "hdrl"; i suoi contenuti includono la larghezza, l'altezza e la frequenza dei fotogrammi del video. Nel secondo sottoblocco, il tag di movimento rappresenta la frequenza dei fotogrammi del video. Il video AVI è composto dai dati audio/visivi effettivi in questo blocco. C'è anche un terzo subchunk opzionale con il tag "idx1", che indica la posizione all'interno del file dei singoli blocchi di dati che appartengono al file.

### Limitazioni ###

* Le informazioni sulle proporzioni non possono essere codificate nella specifica AVI originale, sebbene la successiva specifica OpenDML (AVI 2.0) offra un metodo standardizzato
* Sebbene i file AVI siano ampiamente utilizzati nella post-produzione cinematografica e televisiva, vari approcci all'aggiunta di un codice temporale sono in competizione, influenzando l'usabilità del formato.
* Un file video codificato in AVI non può utilizzare una tecnica di compressione che richiede dati di fotogrammi futuri oltre il fotogramma da codificare (fotogramma B)
* È problematico utilizzare file AVI con bitrate variabili (VBR) (come l'audio MP3 a frequenze di campionamento inferiori a 32 kHz)
* È probabile che un file AVI che codifica lungometraggi a definizione standard come normalmente utilizzato comporti un sovraccarico di circa 5 MB all'ora, a seconda di come viene utilizzato il file
* I sottotitoli devono essere codificati nel flusso video o distribuiti in un file separato nel caso in cui i file AVI non possano contenere allegati come font e sottotitoli

## Breve storia ##

AVI è stato introdotto da Microsoft nel 1992 con l'obiettivo di fornire un formato di file audio e video più robusto e avanzato. Il formato è diventato rapidamente popolare con l'uso di Internet, consentendo alle persone di condividere file video direttamente e indirettamente tramite l'archiviazione multimediale basata su cloud.

## Riferimenti ##

* [AVI - Di Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

