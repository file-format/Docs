{
  "date" : "2019-10-11",
  "keywords" :[ "file bmp", "formato file bmp", "cos'è un file bmp", "file", "esempio bmp", "estensione file bmp", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Formato file immagine",
  "description":"Scopri il formato di file BMP e le API che possono creare e aprire file BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Che cos'è un file BMP? #

I file con estensione .BMP rappresentano file di immagine bitmap utilizzati per memorizzare immagini digitali bitmap. Queste immagini sono indipendenti dalla scheda grafica e sono anche chiamate formato di file DIB (Device Independent Bitmap). Questa indipendenza serve allo scopo di aprire il file su più piattaforme come Microsoft Windows e Mac. Il formato file BMP può memorizzare dati come immagini digitali bidimensionali sia in formato monocromatico che a colori con varie profondità di colore.

## Specifiche del formato file BMP ##

Le bitmap indipendenti dal dispositivo fungono da ausilio per lo scambio di bitmap tra dispositivi e applicazioni. A causa della continua evoluzione di questo formato di file, le informazioni contenute nelle intestazioni possono essere diverse a seconda della versione di Bitmap. Un singolo file bitmap è costituito da strutture fisse e di dimensioni variabili in una sequenza specifica.

Le strutture in un file Bitmap sono disposte nel seguente ordine:


|Struttura|Opzionale|Dimensioni|Scopo
---|---|---|---|
|Intestazione file|No|14|Per memorizzare informazioni generali sul file immagine bitmap
|DiB Header|No|Fixed-Size|Per memorizzare informazioni dettagliate sull'immagine bitmap e definire il formato pixel
|Maschere di bit extra|Sì|12 o 16 byte|Per definire il formato dei pixel
|Tavolozza dei colori|Semi-opzionale|Dimensione variabile|Per definire i colori utilizzati dai dati dell'immagine bitmap
|Gap1|Sì|Dimensione variabile|Allineamento della struttura
|Matrice di pixel|No|Dimensione variabile|Il formato pixel è definito dall'intestazione DIB o dalle maschere di bit extra.
|Gap2|Sì|Dimensione variabile|Allineamento della struttura
|Profilo colore ICC|Sì|Dimensione variabile|Per definire il profilo colore per la gestione del colore

Quando un'immagine bitmap viene caricata in memoria, diventa una struttura DIB, utilizzata da Windows tramite la sua API GDI. L'intestazione del file non fa parte di questa struttura di dati. Il colore può anche essere costituito da voci a 16 bit che costituiscono indici alla tavolozza correntemente referenziata invece di definizioni di colore RGB esplicite. Diamo un'occhiata ad alcuni di questi in dettaglio, in particolare le intestazioni.

### Intestazione del file bitmap ###

Un'intestazione di file bitmap è simile ad altre intestazioni di file utilizzate per identificare il file. Poiché esistono diverse varianti del formato di file BMP, i primi 2 byte del formato di file BMP sono il carattere "B" e quindi il carattere "M" nella codifica ASCII. Tutti i valori interi sono memorizzati in formato little-endian.

|Offset esadecimale|Offset dec|Dimensione|Scopo
---|---|---|---|
|00|0|2 byte|Il campo di intestazione utilizzato per identificare il file BMP e DIB è 0x42 0x4D in esadecimale, come BM in ASCII. Può seguire i valori possibili.* **BM** – Windows 3.1x, 95, NT, ... ecc. * **BA** – array bitmap struct OS/2 * **CI** – struct OS/2 icona colore * **CP** – Puntatore colore const OS/2 * **IC** – Icona struttura OS/2 * **PT** – Puntatore OS/2
|02|2|4 byte|La dimensione del file BMP in byte
|06|6|2 byte|Riservato; il valore effettivo dipende dall'applicazione che crea l'immagine
|08|8|2 byte|Riservato; il valore effettivo dipende dall'applicazione che crea l'immagine
|0A|10|4 byte|L'offset, cioè l'indirizzo iniziale, del byte in cui si trovano i dati dell'immagine bitmap (array di pixel).

#### Intestazione DIB (intestazione delle informazioni bitmap) ####

Le informazioni dettagliate sull'immagine sono rappresentate da questa intestazione. Sulla base di queste informazioni, verrà determinata l'applicazione che verrà utilizzata per visualizzare l'immagine sullo schermo. Tutte queste intestazioni contengono un campo DWORD (32 bit), che ne specifica le dimensioni, in modo che un'applicazione possa determinare facilmente l'intestazione utilizzata nell'immagine. Ciò è fondamentalmente dovuto al fatto che il formato DIB ha subito diverse estensioni. Di seguito è riportata l'intestazione DIB con i campi elencati.

#### Palette dei colori ####

Una tavolozza dei colori BMP è una matrice di strutture che specificano i valori di intensità RGB di ciascun colore nella tavolozza dei colori di un dispositivo di visualizzazione. Ciascun pixel nei dati bitmap memorizza un singolo valore utilizzato come indice nella tavolozza dei colori. Le informazioni sul colore memorizzate nell'elemento in corrispondenza di quell'indice specificano il colore di quel pixel. La disponibilità del colore in un file bitmap varia come segue:

* Uno, 4 e 8 bit: dovrebbe contenere sempre una tavolozza di colori
* Sedici, 24 e 32 bit: non contengono mai tavolozze di colori
* File BMP a sedici e 32 bit: contengono valori di maschera dei campi di bit al posto della tavolozza dei colori

#### Memoria pixel ####

I pixel bitmap vengono archiviati come bit compressi in righe in cui la dimensione di ciascuna riga viene arrotondata a un multiplo di 4 byte (una DWORD a 32 bit) mediante riempimento. La quantità totale di byte necessari per memorizzare i pixel di un'immagine non può essere calcolata direttamente contando solo i bit. Poiché è coinvolto il riempimento, è richiesto l'effetto di arrotondare per eccesso la dimensione di ciascuna riga a un multiplo di 4 byte. I byte di riempimento (non necessariamente 0) devono essere aggiunti alla fine delle righe per portare la lunghezza delle righe a un multiplo di quattro byte. Quando l'array di pixel viene caricato in memoria, ogni riga deve iniziare con un indirizzo di memoria multiplo di 4.

L'immagine è effettivamente descritta dalla rappresentazione DWORD a 32 bit dell'array di pixel. Di solito i pixel vengono memorizzati "dal basso verso l'alto", iniziando nell'angolo in basso a sinistra, andando da sinistra a destra, quindi riga per riga dal basso verso l'alto dell'immagine. I formati dei pixel e le loro implicazioni sono elencati di seguito:

* Il formato 1 bit per pixel (1bpp) supporta 2 colori distinti, (ad esempio: bianco e nero).
* Il formato 2 bit per pixel (2bpp) supporta 4 colori distinti e memorizza 4 pixel per 1 byte, il pixel più a sinistra è nei due bit più significativi. Ogni valore di pixel è un indice a 2 bit in una tabella con un massimo di 4 colori.
* Il formato a 4 bit per pixel (4bpp) supporta 16 colori distinti e memorizza 2 pixel per 1 byte, il pixel più a sinistra si trova nel nibble più significativo. Ogni valore di pixel è un indice a 4 bit in una tabella con un massimo di 16 colori.
* Il formato a 8 bit per pixel (8 bpp) supporta 256 colori distinti e memorizza 1 pixel per 1 byte. Ogni byte è un indice in una tabella fino a 256 colori.
* Il formato a 16 bit per pixel (16 bpp) supporta 65536 colori distinti e memorizza 1 pixel per WORD a 2 byte. Ogni WORD può definire i campioni alfa, rosso, verde e blu del pixel.
* Il formato pixel a 24 bit (24 bpp) supporta 16.777.216 colori distinti e memorizza un valore di 1 pixel per 3 byte. Ogni valore di pixel definisce i campioni rosso, verde e blu del pixel (8.8.8.0.0 nella notazione RGBAX). Nello specifico, nell'ordine: blu, verde e rosso (8 bit per ogni campione).
* Il formato a 32 bit per pixel (32 bpp) supporta 4.294.967.296 colori distinti e memorizza 1 pixel per DWORD a 4 byte. Ogni DWORD può definire i campioni alfa, rosso, verde e blu del pixel.

## Riferimenti ##

* [Formato Windows MetaFile](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Formato file BMP](https://en.wikipedia.org/wiki/BMP_file_format)

