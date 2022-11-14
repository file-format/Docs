{
  "date" : "2019-10-11",
  "keywords" :[ "file psb", "formato file psb", "cos'è un file psb", "file", "esempio psb", "estensione file psb", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Formato file immagine grande Photoshop",
  "description":"Scopri il formato di file PSB e le API che possono creare e aprire file PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PSB?
Adobe Photoshop salva i file in due formati. I file con dimensioni di 30.000 per 30.000 pixel vengono salvati con estensione PSD e file più grandi di PSD fino a 300.000 per 300.000 pixel vengono salvati con estensione PSB nota come "Photoshop Big". Più in particolare, i file PSB possono avere dimensioni fino a 4 EB (oltre 4,2 miliardi di GB) con immagini che hanno un'altezza e una larghezza fino a 300.000 pixel. I PSD, d'altra parte, possono avere un massimo di 2 GB e dimensioni dell'immagine di 30.000 pixel.

PSB è anche noto come formato grande per Photoshop e supporta tutte le funzionalità di Photoshop come livelli, effetti e filtri. Photoshop può convertire file PSB in [PSD](/it/image/psd/), [JPG](/it/image/jpeg/) , [PNG](/it/image/png/), [EPS](/it/page-description-language/eps/), [GIF](/it/image/gif/) e anche altri formati. Il formato per documenti di grandi dimensioni di Photoshop è disponibile una volta abilitata la funzione del pannello di gestione dei file della finestra di dialogo delle preferenze di Photoshop.

## Informazioni sul formato del file ##

Il formato di file di Photoshop è diviso in cinque parti principali con molti indicatori di lunghezza per spostarsi tra le sezioni.

|Formato file
---|
|Intestazione del file
|Dati modalità colore
| Risorse di immagine
|Informazioni su livelli e maschere
|(((
Dati immagine
)))

### Intestazione del file ###

L'intestazione del file ha una lunghezza fissa di 26 byte e contiene le proprietà di base dell'immagine.

BYTE Signature [4] – Equivale a '8BPS'.

WORD Versione [2] – Numero di versione, PSD n. 1, PSB n. 2.

BYTE Riservato [6] – Riservato e sempre zero.

Canali WORD [2] – Numero di canali di colore nell'immagine inclusi i canali alfa. Il suo valore varia da 1 a 56.

Righe LUNGHE [4] – Altezza dell'immagine in pixel, PSD 1-30.000, PSB 1-300.000.

Colonne LONG [4] – Larghezza dell'immagine in pixel, PSD 1-30.000, PSB 1-300.000.

WORD Profondità [2] – Numero di bit per canale. I valori supportati sono 1,8,16 e 32.

Modalità WORD [2] – Modalità colore del file.

#### Modalità Descrizione ####


|Modalità|Descrizione
---|---|
|0|Bitmap (monocromatica)
|1|Scala di grigi
|2|Indicizzato
|3|RGB
|4|CMYK
|7|Multicanale
|8|Duotone (mezzitoni)
|9|Laboratorio

### Dati modalità colore ###

Dopo la sezione dell'intestazione del file segue la sezione dei dati della modalità colore. Il blocco inizia con un numero LONG che fornisce la lunghezza del blocco in byte. La struttura dei dati della modalità colore è la seguente:

4 byte – La lunghezza dei seguenti dati colore.

Variabile – Dati colore

Se il valore del campo della modalità nella sezione dell'intestazione non è Colore indicizzato o due tonalità, la lunghezza del blocco sarà 0 e non ci saranno dati dopo il campo della lunghezza.

Per le immagini a colori indicizzate, la lunghezza sarà di 768 byte che conterrà una tavolozza di 256 colori. Per la bicromia, i dati conterranno i parametri dello schermo e altre informazioni correlate.

### Risorse per le immagini ###

Dopo la sezione dei dati della modalità colore, il terzo blocco è la sezione delle risorse dell'immagine. I primi quattro byte sono un numero LONG che specifica la lunghezza del blocco seguito da una serie di blocchi di risorse. La struttura del blocco di risorse immagine è la seguente:

BYTE Tipo [4] – Firma '8BIM'

ID PAROLA [2] – ID risorsa immagine. C'è un elenco di ID risorsa che può essere visto dal collegamento di riferimento.

BYTE Nome [Variabile] – Nome: Pascal Stringa di lunghezza pari. ** **

LONG Size [4] – Dimensione effettiva dei dati delle risorse che seguono.

BYTE Dati [Variabile} – Dati della risorsa. È imbottito per rendere la dimensione uniforme.

Alcuni dei formati delle risorse sono brevemente spiegati di seguito:

**Formato risorse griglia e guide:** le informazioni su griglia e guide sono archiviate nel blocco risorse. Questi blocchi di risorse contengono una griglia di 16 byte e un'intestazione di guida seguiti da blocchi di 5 byte di informazioni di guida.

**Formato risorsa miniatura:** Le informazioni sulle miniature vengono memorizzate nel blocco delle risorse immagine per la visualizzazione dell'anteprima che consiste in un'intestazione di 28 byte e una miniatura JFIF in RGB.

**Formato delle risorse dei campionatori di colore:** Le informazioni sui campionatori di colore sono archiviate in un blocco di risorse immagine con un'intestazione di 8 byte seguita da un blocco di informazioni sui campionatori di colore a lunghezza variabile.

### Informazioni su livelli e maschere ###

Il quarto blocco è il blocco delle informazioni sui livelli e sulle maschere e contiene informazioni sui livelli e sulle maschere. Le informazioni sui livelli vengono prima memorizzate e poi le informazioni sulla maschera.

**Informazioni sul livello:** Le informazioni sul livello iniziano con un valore LONG che mostra la lunghezza delle informazioni sul livello. Dopodiché c'è il conteggio del valore WORD che mostra il numero di record di livello da seguire.

[8] – lunghezza degli strati

[2] – Conteggio strati

[Variabile] – Informazioni su ciascun livello.

[Variabile] – Dati immagine canale.** **

**Informazioni sulla maschera:** La struttura della maschera ha il seguente formato:


|Struttura dati|Nome campo| Descrizione
---|---|---|
|PAROLA| Sovrapposizione spazio colore| (Non documentato)
|BYTE[8]| Componenti colore| Componenti di colore 4x2 byte
|PAROLA| Opacità| 0#trasparente, 1#opaco
|BYTE| gentile| 0#invertito, 1#protetto, 128#usa il valore memorizzato
|BYTE| imbottitura| impostato a zero

### Dati immagine ###

L'ultima sezione contiene i dati dei pixel dell'immagine. I dati dell'immagine vengono memorizzati come una serie di sequenze in piani, ovvero prima tutti i dati rossi, poi tutti i dati verdi, ecc. WORD all'inizio di ogni riga mostra la dimensione in byte relativa a ciascuna riga di scansione.

[2] – Metodo di compressione:

[Variabile] – Dati immagine in ordine planare, ad esempio RRRR, GGGG, BBBB ecc.

Metodi di compressione:

0 – Raw Dati immagine

1 – RLE compresso

2 – Zip senza pronostico

3 – Zip con pronostico

## Riferimento ##

* [Formato file PSB - Di Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

