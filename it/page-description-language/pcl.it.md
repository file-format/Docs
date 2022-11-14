{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Scopri il formato di file PCL e le API che possono creare e aprire file PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file PCL? ##

PCL sta per Printer Command Language, un linguaggio di descrizione della pagina introdotto da Hewlett Packard (HP). HP ha creato PCL per fornire un modo efficiente per controllare le funzioni della stampante su molti dispositivi di stampa diversi. Il formato è stato originariamente sviluppato per le stampanti HP a matrice di punti e a getto d'inchiostro, ma con il passare del tempo ha fatto parte di varie stampanti termiche, a matrice e di pagine. Il formato ha subito diverse revisioni diverse, risultando in diverse versioni in cui ogni versione è stata migliorata per soddisfare le esigenze del tempo rispetto alle funzioni di controllo della stampante. Oggi, PCL è il linguaggio di stampa più diffuso nell'ultimo mercato delle stampanti.

## Versioni PCL ##

Le versioni PCL differiscono per funzionalità (ad es. supporto del tipo di font: font bitmap, font scalabili (Intellifonts, font TrueType), metodi di compressione grafica raster, supporto grafico HP-GL/2).

**PCL 1:** intorno al 1980 - La funzionalità Print and Space è l'insieme di funzioni di base fornite per l'output di workstation semplice, conveniente e per utente singolo.

**PCL 2:** intorno al 1980 - La funzionalità EDP (Elaborazione elettronica dei dati)/Transazione è un superset di PCL 1. Sono state aggiunte funzioni per la stampa di sistemi multiutente per uso generale.

**PCL 3**: 1984 - La funzionalità di elaborazione testi di Office è un superset di PCL 2. Sono state aggiunte funzioni per la produzione di documenti per ufficio di alta qualità e un dpi aumentato fino a 300 dpi. Consentiva l'uso di un numero limitato di caratteri e grafica bitmap e supportava HP-GL. PCL 3 è stato ampiamente imitato da altri produttori di stampanti ed è stato indicato da queste aziende come "Emulazione LaserJet Plus".
(Stampanti: famiglia HP DeskJet, stampante serie HP LaserJet, stampante serie HP LaserJet Plus)

**PCL3+:** utilizzato dalla famiglia di stampanti DeskJet e DesignJet.

**PCL3c:** Utilizzato dalla famiglia di stampanti DeskJet e DesignJet.

**PCL3e**: utilizzato dalla famiglia di stampanti DeskJet e DesignJet. Ora utilizzato anche in PhotoSmart.

**PCL3GUI**: utilizza RTL ed è utilizzato dalla famiglia di stampanti DeskJet e DesignJet.

**PCLSLEEK**: utilizza RTL ed è utilizzato dalla famiglia di stampanti DeskJet e DesignJet.

**PCL 4**: 1985 - La funzionalità di formattazione della pagina è un superset di PCL 3. Macro supportate, caratteri bitmap più grandi e grafica. (Stampanti: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - La funzionalità Office Publishing è un superset di PCL 4. Le nuove funzionalità di pubblicazione includono il ridimensionamento dei caratteri e la grafica HP-GL/2 (vettoriale). (Stampanti: HP LaserJet III)

**PCL 5e:** 1994 - Questa è una revisione importante, che include nuove funzionalità come il sistema di compressione adattiva, la codifica dei caratteri a 2 byte, il supporto per i caratteri vettoriali e i comandi di configurazione bidirezionale. Include operazioni logiche (corrisponde a GDI ROP) per migliorare il supporto di Windows prima dei tracciati di ritaglio. (Stampanti: HP LaserJet 4)

**PCL 5j:** Nuove funzionalità come il supporto dei caratteri a 2 byte per i caratteri scalabili residenti in giapponese, la scrittura verticale, i formati carta giapponesi e le stringhe di caratteri. (Stampanti: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Il supporto colore e le operazioni logiche sono state aggiunte a PCL5. PCL5c precede PCL5e. Alcuni modelli supportano anche i tracciati di ritaglio. (Stampanti: HP Color LaserJet, HP PaintJet 300 XL (prima stampante con PCL5c), HP DeskJet 1200C/1600C (questi numeri di modello sono stati riutilizzati e i modelli più recenti non sono PCL 5c)

**PCL 5ce:** Supporta i caratteri tipografici scalabili Agfa Microtype. (Stampanti: stampante HP 2500c Pro)

**PCL 6 / XL:** 1996 - PCL 6 o PCL XL è un nuovo formato introdotto nel 1995, che non è compatibile con nessuna versione precedente di PCL. (Stampanti: HP LaserJet 5, 5M e 5N)

## Panoramica PCL 6 ##

HP ha introdotto PCL 6 nel 1996, che è stata la successiva evoluzione del linguaggio PCL e delle relative tecnologie. Ha i seguenti componenti:

**PCL 6 Enhanced:** fornisce una versione ottimizzata per la stampa da interfacce utente grafiche (GUI) come MS Windows e OS/2

**PCL 6 Standard:** fornisce una compatibilità completa con le precedenti stampanti HP LaserJet

**Sintesi font PCL:** fornisce font scalabili, gestione dei font e archiviazione di moduli e font.

La versione estesa PCL XL è più vicina al GDI utilizzato da molte applicazioni. Fa in modo che avvengano meno traduzioni, il che si traduce in maggiori capacità WYSIWYG e prestazioni migliori con le applicazioni che supportano gli escape implementati dal driver Enhanced. L'output del driver avanzato (PCL XL) potrebbe non corrispondere all'output del driver standard. Se l'output non è quello previsto, scegli invece il driver Standard (PCL5e).

I comandi PCL 6 Enhanced sono progettati per soddisfare in modo ottimale i requisiti di stampa grafica per le applicazioni basate su GUI. Nella maggior parte dei casi, per ogni comando di stampa grafica che una GUI desidera eseguire, esiste un comando PCL 6 Enhanced corrispondente. Ciò riduce il numero di comandi necessari per descrivere una pagina grafica. Ciascun comando in PCL 6 Enhanced è progettato per richiedere un trasferimento dati minimo dal PC host alla stampante. Ciò riduce la quantità di dati necessari per descrivere una pagina.

Il sistema di stampa Windows per la maggior parte delle stampanti HP LaserJet fornisce due driver separati: Standard e Avanzato. Il driver Standard fornisce la compatibilità con le versioni precedenti utilizzando i comandi PCL 6 Standard (PCL5e) per stampare testo semplice o pagine miste di testo e grafica. Il driver Enhanced utilizza i comandi PCL 6 Enhanced che sono stati ottimizzati per la stampa di pagine grafiche complesse.

## Revisioni della classe PCL 6 ##

#### Classe 1.1 ####

**Strumenti di disegno:** Supporta il disegno di linee, archi/ellissi/corde, rettangoli (arrotondati), poligoni, tracciati Bezier, tracciati ritagliati, immagini raster, linee di scansione, operazioni raster.
**Gestione del colore:** Supporta tavolozze a 1/4/8 bit, spazio colore RGB/grigio. Supporta modelli di mezzitoni personalizzati (massimo 256 modelli).
**Compressione:** Supporta RLE.
**Unità di misura:** Pollice, millimetro, decimo di millimetro.
**Gestione della carta:** Supporta set personalizzati o predefiniti di tipi di carta, inclusi Letter, Legal, A4, ecc. È possibile scegliere la carta dall'alimentazione manuale, vassoi e cassetti. La carta può essere stampata in fronte/retro orizzontalmente o verticalmente. La carta può essere orientata in verticale, in orizzontale o in rotazione di 180 gradi dei primi due.
**Font:** Supporta font bitmap o TrueType, punti di codice a 8 o 16 bit. La scelta del set di caratteri utilizza un codice di set di simboli diverso da PCL 5. Quando si utilizza il font bitmap, molti comandi di ridimensionamento non sono disponibili. Quando si utilizza il carattere TrueType, i descrittori di lunghezza variabile, i blocchi di continuazione non sono supportati. Il carattere del contorno può essere ruotato, ridimensionato o tagliato.

#### Classe 2.0 ####

**Compressione:** Aggiunta una compressione JPEG proprietaria chiamata JetReady.
**Gestione della carta:** i supporti possono essere reindirizzati a diversi scomparti di uscita (fino a 256). Aggiunti i formati dei supporti preimpostati A6 e B6 giapponesi. Aggiunta la terza cassetta preimpostata, 248 supporti per vassoio esterno.
**Carattere:** Il testo può essere scritto in verticale.

#### Classe 2.1 ####

**Gestione del colore:** Aggiunta funzione di corrispondenza del colore.
**Compressione:** Aggiunta riga delta.
**Gestione della carta:** Orientamento e formato del supporto sono opzionali quando si dichiara una nuova pagina. Aggiunti tipi di carta B5, JIS 8K, JIS 16K, JIS Exec.

#### Classe 3.0 ####

**Gestione del colore:** Consenti l'utilizzo di diverse impostazioni dei mezzitoni per grafica vettoriale o raster, testo. Supporta il semitono adattivo.
**Protocollo:** Supporta il passthrough PCL, consentendo l'utilizzo delle funzionalità PCL 5 da parte dei flussi PCL 6. Tuttavia, alcuni stati PCL 6 non vengono mantenuti quando si utilizza questa funzione.
**Carattere:** Supporta i caratteri PCL.
**Viewer/Converter:** PCLReader (freeware) può visualizzare, convertire o stampare qualsiasi livello di PCL 6 (incluso JetReady) su qualsiasi stampante.

## Riferimenti ##

* [PCL - Di Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

