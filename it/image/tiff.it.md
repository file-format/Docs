{
  "date" : "2019-10-11",
  "keywords" :[ "file tiff", "formato file tiff", "cos'è un file tiff", "file", "esempio tiff", "estensione file tiff", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF - Formato file immagine",
  "description":"Scopri il formato di file TIFF e le API che possono creare e aprire file TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file TIFF?

TIFF o TIF, Tagged Image File Format, rappresenta immagini raster destinate all'uso su una varietà di dispositivi conformi a questo standard di formato file. È in grado di descrivere dati di immagini a due livelli, in scala di grigi, a colori ea colori in diversi spazi colore. Supporta schemi di compressione lossy e lossless per scegliere tra spazio e tempo per le applicazioni che utilizzano il formato. Il formato non dipende dalla macchina ed è libero da limiti come processore, sistema operativo o file system.

## Breve storia del formato di file TIFF

Il formato file TIFF è stato inizialmente creato da Aldus Corporation nell'autunno del 1986, dopo una serie di incontri con vari produttori di scanner e sviluppatori di software. Lo scopo principale del formato di file TIFF era fornire un formato di file di immagine scansionato comune per tutti i fornitori di scanner desktop. A partire dal supporto per il solo formato di immagine binario, il formato si è evoluto al supporto di immagini in scala di grigi ea colori con il passare del tempo. La versione iniziale delle specifiche del formato di file TIFF può essere etichettata come Reivision 3.0 poiché esistevano due versioni precedenti della bozza. Un'importante revisione 5.0 è stata pubblicata nel 1988 che ha aggiunto il supporto per le immagini dei colori della tavolozza e la compressione LZW. La revisione 6.0 dei formati di file TIFF è stata pubblicata nel 1992 in seguito. Nel 1994, Adobe Systems ha acquisito Aldus e le specifiche sono ora disponibili e gestite da Adobe Systems.

## Specifiche del formato file TIFF

Il formato di file TIFF è estensibile e ha subito diverse revisioni che consentono l'inclusione di una quantità illimitata di informazioni private o per scopi speciali. Un file TIFF inizia con un'intestazione di 8 byte in cui i byte sono numeri da 0 a N. Il file TIFF più grande possibile è lungo 2**32 byte. Il file inizia con un'intestazione di file immagine a 8 byte che punta a un file immagine direttamente (IFD). Un IFD contiene informazioni sull'immagine e puntatori ai dati dell'immagine reale.

### Intestazione del file TIFF

L'intestazione del file TIFF a 8 byte contiene le seguenti informazioni:

**Byte 0-1:** L'ordine dei byte utilizzato all'interno del file. I valori legali sono: “II”(4949.H)“MM” (4D4D.H).

Nel formato "II", l'ordine dei byte va sempre dal byte meno significativo al byte più significativo, sia per gli interi a 16 bit che a 32 bit. Questo è chiamato ordine dei byte little-endian. Nel formato "MM", l'ordine dei byte va sempre dal più significativo al meno significativo, sia per gli interi a 16 bit che a 32 bit. Questo è chiamato ordine dei byte big-endian.

**Byte 2-3:** Un numero arbitrario ma scelto con cura (42) che identifica ulteriormente il file come file TIFF. L'ordine dei byte dipende dal valore di Byte 0-1.

**Byte 4-7:** L'offset (in byte) del primo IFD. La directory può trovarsi in qualsiasi posizione nel file dopo l'intestazione, ma deve iniziare su un limite di parola. In particolare, una directory di file di immagine può seguire i dati di immagine che descrive. I lettori devono seguire i puntatori ovunque essi conducano. Il termine byte offset è sempre usato in questo documento per riferirsi a una posizione rispetto all'inizio del file TIFF. Il primo byte del file ha un offset di 0.

### Directory dei file di immagine

Un IFD contiene informazioni sull'immagine e puntatori ai dati effettivi dell'immagine. Consiste in un conteggio di 2 byte del numero di voci della directory (cioè il numero di campi), seguito da una sequenza di voci di campo di 12 byte , seguito da un offset di 4 byte dell'IFD successivo (o 0 se nessuno). Ci deve essere almeno 1 IFD in un file TIFF e ogni IFD deve avere almeno una voce.

#### Voce IFD

Ciascuna voce IFD a 12 byte è nel formato seguente.


|Byte|Descrizione
---|---|
|0-1|Il tag che identifica il campo
|2-3|Il tipo di campo
|4-7|Conteggio del tipo indicato
|8-11|The Value Offset, l'offset del file (in byte) del valore per il campo. Il valore dovrebbe iniziare su un limite di parola; il corrispondente Value Offset sarà quindi un numero pari. Questo offset del file può puntare in qualsiasi punto del file, anche dopo i dati dell'immagine

Un campo TIFF è un'entità logica costituita dal tag TIFF e dal suo valore. Questo concetto logico è implementato come voce IFD, più il valore effettivo se non rientra nella parte valore/offset, gli ultimi 4 byte della voce IFD. I termini campo TIFF e voce IFD sono intercambiabili nella maggior parte dei contesti.

### TIFF di riferimento ###

Baseline TIFF è il fulcro di TIFF, gli elementi essenziali che tutti gli sviluppatori TIFF tradizionali dovrebbero supportare nei loro prodotti. La conformità al formato TIFF è subordinata al rispetto dei requisiti TIFF di base. Questi requisiti sono ben documentati nel documento delle specifiche 6.0.

#### Più immagini per file ####

Potrebbe esserci più di un IFD in un file TIFF. Ogni IFD definisce un sottofile. Un possibile utilizzo dei file secondari è quello di descrivere immagini correlate, come le pagine di una trasmissione di facsimile. Un lettore TIFF Baseline non è necessario per leggere alcun IFD oltre al primo.

#### Tipi di immagine ####

L'immagine TIFF di base ha i seguenti tipi:

**Bilivello:** Un'immagine bilivello contiene due colori: bianco e nero. TIFF consente a un'applicazione di scrivere dati bilivello in un formato bianco è zero o nero è zero. Il campo che registra queste informazioni è chiamato **Interpretazione Fotometrica**.

* RGB a colori

Le informazioni sull'interpretazione fotometrica per le immagini Bilevel sono le seguenti:

Etichetta = 262 (106.H)
Tipo = CORTO
**I valori**

|Valore|Descrizione|
---|---|
|0|Per le immagini bilivello e in scala di grigi: 0 è rappresentato come bianco. Il valore massimo è rappresentato come nero. Questo è il valore normale per Compression#2|
|1|Il nero è zero. Per le immagini bilivello e in scala di grigi: 0 viene visualizzato come nero. Il valore massimo viene rappresentato come bianco. Se questo valore è specificato per Compression#2, l'immagine dovrebbe essere visualizzata e stampata al contrario.|

**Scala di grigi:** Le immagini in scala di grigi sono una generalizzazione delle immagini bilivello. Le immagini bilivello possono memorizzare solo dati immagine in bianco e nero, ma le immagini in scala di grigi possono anche memorizzare sfumature di grigio. Per descrivere tali immagini, è necessario aggiungere o modificare i seguenti campi. Gli altri campi obbligatori sono gli stessi richiesti per le immagini bilivello. Per le immagini in scala di grigi, Compressione # 1 o 32773 (PackBits). In Baseline TIFF, le immagini in scala di grigi possono essere archiviate come dati non compressi o compresse con l'algoritmo PackBits.

Le informazioni su **BitsPerSample** per le immagini in scala di grigi sono le seguenti:

Etichetta = 258 (102.H)
Tipo = CORTO

Il numero di bit per componente. I valori consentiti per le immagini in scala di grigi TIFF di base sono 4 e 8, consentendo 16 o 256 distinte sfumature di grigio.

**Colore tavolozza:** Le immagini a colori tavolozza sono simili alle immagini in scala di grigi. Hanno ancora un componente per pixel, ma il valore del componente viene utilizzato come indice in una tabella di ricerca RGB completa. Per descrivere tali immagini, è necessario aggiungere o modificare i seguenti campi. Gli altri campi obbligatori sono gli stessi delle immagini in scala di grigi.
Le informazioni sull'interpretazione fotometrica per l'immagine Palette-Color sono le seguenti:

Interpretazione fotometrica = 3 (Colore tavolozza).
ColorMapTag = 320 (140.H)
Tipo = CORTO
N = 3 * (2 bit per campione)

Questo campo definisce una mappa dei colori Rosso-Verde-Blu (spesso chiamata tabella di ricerca) per le immagini dei colori della tavolozza. In un'immagine a colori della tavolozza, un valore pixel viene utilizzato per indicizzare in una tabella di ricerca RGB. Ad esempio, un pixel del colore della tavolozza con un valore di 0 verrebbe visualizzato in base alla 0a tripletta di rosso, verde e blu. In una ColorMap TIFF, tutti i valori del rosso vengono prima, seguiti dai valori del verde, quindi i valori del blu. Nella ColorMap, il nero è rappresentato da 0,0,0 e il bianco è rappresentato da 65535, 65535, 65535.

**RGB a colori:** In un'immagine RGB, ogni pixel è composto da tre componenti: rosso, verde e blu. Non esiste ColorMap. Per descrivere un'immagine RGB, è necessario aggiungere o modificare i seguenti campi e valori. Gli altri campi obbligatori sono gli stessi richiesti per le immagini a colori della tavolozza.

Bit per campione = 8,8,8. Ciascun componente ha una profondità di 8 bit in un'immagine RGB TIFF di base.

PhotometricInterpretation = 2 (RGB) e non c'è ColorMap.

Etichetta = 277 (115.H)
Tipo = CORTO
Il numero di componenti per pixel. Questo numero è 3 per le immagini RGB, a meno che non siano presenti campioni aggiuntivi.

## Riferimenti ##

* [Formato file TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

