{
  "date" : "2019-10-11",
  "keywords" :[ "file exif", "formato file exif", "cos'è un file exif", "file", "esempio exif", "estensione file exif", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Scopri il formato di file EXIF e le API che possono creare e aprire file EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file EXIF?
EXIF sta per "Exchangeable Image File Format", la definizione data per la prima volta da [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) nel 1985. Lo standard è gestito da Japan Electronics e Information Technology Industries Association (JEITA) ad oggi. EXIF è uno standard per le specifiche dei formati di immagini e suoni utilizzati principalmente da fotocamere digitali e scanner.

Lo standard EXIF include le informazioni sui tag e sui metadati con il file immagine. I metadati possono contenere informazioni come modello della fotocamera, velocità dell'otturatore, data e ora, apertura, produttore, tempo di esposizione, risoluzione X, risoluzione Y ecc. Normalmente i dati EXIF sono nascosti per impostazione predefinita. Per visualizzare i dati EXIF, è necessario selezionare le proprietà di visualizzazione all'interno dell'applicazione di visualizzazione delle immagini. I metadati Exif possono anche includere miniature insieme a dati di immagine tecnici e primari in un singolo file immagine.

## Storia e versioni ##

* Nell'ottobre 1995, JEIDA ha stabilito la versione 1. In questa versione JEIDA ha definito la struttura, che consiste in formato dati immagine e informazioni sugli attributi, e tag di base.
* Novembre 1997, la versione 1.1 è stata introdotta con la maggior parte dei tag della versione 1, ma ha anche aggiunto disposizioni per informazioni sugli attributi opzionali e operazioni di formattazione.
* Giugno 1998, versione 2 con spazio colore sRGB, miniature compresse e file audio.
* Dicembre 1998, Versione 2.1 con memoria migliorata e informazioni sugli attributi.
* Febbraio 2002, versione 2.2, versione migliorata 2.1 con l'aggiunta della finitura di stampa.
* Settembre 2003, versione 2.21 con spazio colore opzionale noto come Adobe RGB.

## Formato file EXIF

EXIF utilizza i seguenti formati di file con l'aggiunta di metadati specifici.

1. [JPEG](/it/image/jpeg/) - trasformata discreta del coseno (DCT) per file di immagine compressi.
1. [TIFF](/it/image/tiff/) Rev. 6.0 (RGB o YCbCr) per file di immagine non compressi.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) per file audio (Linear [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) o ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM per dati audio non compressi e [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) per dati audio compressi).

### Indicatore utilizzato da EXIF ###

Il marker 0xFFE0~~0xFFEF è "Application Marker", utilizzato dall'applicazione utente. Ad esempio, le vecchie fotocamere digitali utilizzano JFIF (JPEG File Interchange Format) per la memorizzazione delle immagini. JFIF utilizza l'indicatore APP0 (0xFFE0) per inserire i dati di configurazione della digi cam e l'immagine in miniatura. Inoltre, EXIF utilizza anche un indicatore di applicazione per inserire i dati, ma EXIF utilizza un indicatore APP1 (0xFFE1) per evitare un conflitto con il formato JFIF. Tutti i formati di file EXIF iniziano da questo formato.


|Marcatore SOI|Marcatore APP1|Dati APP1|Altro marcatore
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Inizia da SOI (0xFFD8) Marker, quindi è un file JPEG. Quindi APP1 Marker segue immediatamente. Tutti i dati di EXIF sono memorizzati in questa area dati APP1. La parte di "SSSS" nella tabella superiore indica la dimensione dell'area dati APP1 (area dati EXIF). Si prega di notare che la dimensione "SSSS" include anche la dimensione del descrittore stesso. Dopo il "SSSS", iniziano i dati dell'APP1. La prima parte è un dato speciale per l'identificazione, EXIF o meno, vengono utilizzati il carattere ASCII "EXIF" e 2 byte di 0x00. Dopo l'area dell'indicatore APP1, seguono gli altri indicatori JPEG.

### Struttura dati Exif ###

Di seguito viene mostrata una struttura approssimativa dei dati EXIF (APP1). Come discusso in precedenza, i dati EXIF iniziano dal carattere ASCII "EXIF" e 2 byte di 0x00, quindi seguono i dati EXIF. EXIF utilizza il formato TIFF per memorizzare i dati.


|FFE1|Segnale APP1
---|---|
|SSSS|Dati APP1|Dimensioni dati APP1
|45786966 0000|Intestazione Exif
|49492A00 08000000|Intestazione TIFF
|XXXX. . . .|IFD0 (immagine principale)|Directory
|LLLLLLLL|Collegamento a IFD1
|XXXX. . . .|Area dati di IFD0
|XXXX. . . .|Exif SubIFD|Directory
|00000000|Fine del collegamento
|XXXX. . . .|Area dati di Exif SubIFD
|XXXX. . . .|IFD1(immagine miniatura)|Directory
|00000000|Fine del collegamento
|XXXX. . . .|Area dati di IFD1
|FFD8XXXX. . . XXXXFFD9|Immagine in miniatura

#### Intestazione TIFF ####

L'intestazione del file [TIFF](/it/image/tiff/) a 8 byte contiene le seguenti informazioni:

`Byte 0-1:` L'ordine dei byte utilizzato all'interno del file. I valori legali sono: “II”(4949.H)“MM” (4D4D.H).

Nel formato "II", l'ordine dei byte va sempre dal byte meno significativo al byte più significativo, sia per gli interi a 16 bit che a 32 bit. Questo è chiamato ordine dei byte little-endian. Nel formato "MM", l'ordine dei byte va sempre dal più significativo al meno significativo, sia per gli interi a 16 bit che a 32 bit. Questo è chiamato ordine dei byte big-endian.

`Byte 2-3:` Un numero arbitrario ma scelto con cura (42) che identifica ulteriormente il file come file TIFF. L'ordine dei byte dipende dal valore di Byte 0-1.

`Byte 4-7:` L'offset (in byte) del primo IFD. La directory può trovarsi in qualsiasi posizione nel file dopo l'intestazione, ma deve iniziare su un limite di parola. In particolare, una directory di file di immagine può seguire i dati di immagine che descrive. I lettori devono seguire i puntatori ovunque conducano. Il termine byte offset è sempre usato in questo documento per riferirsi a una posizione rispetto all'inizio del file TIFF. Il primo byte del file ha un offset di 0.

#### Directory file immagine ####

Un IFD contiene informazioni sull'immagine e puntatori ai dati effettivi dell'immagine. Consiste in un conteggio di 2 byte del numero di voci della directory (cioè il numero di campi), seguito da una sequenza di voci di campo di 12 byte , seguito da un offset di 4 byte dell'IFD successivo (o 0 se nessuno). Ci deve essere almeno 1 IFD in un file TIFF e ogni IFD deve avere almeno una voce.

##### Voce IFD #####

Ciascuna voce IFD a 12 byte è nel formato seguente.


|Byte|Descrizione
---|---|
|0-1|Il tag che identifica il campo
|2-3|Il tipo di campo
|4-7|Conteggio del tipo indicato
|8-11|The Value Offset, l'offset del file (in byte) del valore per il campo. Il valore dovrebbe iniziare su un limite di parola; il corrispondente Value Offset sarà quindi un numero pari. Questo offset del file può puntare in qualsiasi punto del file, anche dopo i dati dell'immagine

Un campo TIFF è un'entità logica costituita dal tag TIFF e dal suo valore. Questo concetto logico è implementato come voce IFD, più il valore effettivo se non rientra nella parte valore/offset, gli ultimi 4 byte della voce IFD. I termini campo TIFF e voce IFD sono intercambiabili nella maggior parte dei contesti.

#### Immagine in miniatura ####

Il formato Exif contiene la miniatura dell'immagine (tranne Ricoh RDC-300Z). Di solito si trova accanto all'IFD1. Ci sono 3 formati per le miniature; Formato JPEG (JPEG utilizza YCbCr), formato RGB TIFF, formato YCbCr TIFF.

##### Anteprima in formato JPEG #####

Se il valore di Compression(0x0103) Tag in IFD1 è '6', il formato immagine miniatura è JPEG. La maggior parte delle immagini Exif utilizza il formato JPEG per le miniature. In tal caso, puoi ottenere l'offset della miniatura dal tag JpegIFOffset(0x0201) in IFD1, la dimensione della miniatura dal tag JpegIFByteCount(0x0202). Il formato dei dati è un normale formato JPEG, inizia da 0xFFD8 e termina con 0xFFD9. Sembra che il formato JPEG e le dimensioni di 160x120 pixel siano il formato miniatura consigliato per Exif2.1 o successivo.

##### Anteprima in formato TIFF #####

Se il valore di Compression(0x0103) Tag in IFD1 è '1', il formato dell'immagine in miniatura non è compressione (chiamata immagine TIFF). Il punto iniziale dei dati della miniatura è il tag StripOffset(0x0111), la dimensione della miniatura è la somma del tag StripByteCounts(0x0117).

## Riferimenti ##

* [EXIF - Di Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [Formato file EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

