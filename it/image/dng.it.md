{
  "date" : "2019-10-11",
  "keywords" :[ "file dng", "formato file dng", "cos'è un file dng", "file", "esempio dng", "estensione file dng", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Formato file immagine fotocamera digitale",
  "description":"Scopri il formato di file DNG e le API che possono creare e aprire file DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Che cos'è un file DNG?

DNG è un formato di immagine della fotocamera digitale utilizzato per l'archiviazione di file grezzi. È stato sviluppato da Adobe nel settembre 2004. Fondamentalmente è stato sviluppato per la fotografia digitale. DNG è un'estensione del formato standard [TIFF](/it/image/tiff/)/EP e utilizza i metadati in modo significativo. Per manipolare i dati grezzi dalle fotocamere digitali con la facilità della flessibilità e del controllo artistico, i fotografi scelgono i file raw della fotocamera. I formati JPEG e TIFF memorizzano le immagini che vengono elaborate dalla fotocamera, pertanto non è disponibile molto spazio per le modifiche in tali formati.

## Storia e versioni del formato file DNG

Finora ci sono state 5 versioni della specifica DNG finora. La versione 1.0.0.0 è stata lanciata nel settembre 2004 insieme al rilascio di "2.3" (ACR e DNG Converter). Nel febbraio 2005 è stata pubblicata la versione 1.1.0.0. Nel maggio 2008 è stata rilasciata la versione 1.2.0.0 utilizzata in "4.4". La versione 1.3.0.0 è stata pubblicata nel giugno 2009. La versione 1.4.0.0 è apparsa nel 2012.

## Formato file DNG

Mentre i file Camera Raw acquisiscono dati non elaborati o poco elaborati direttamente dal sensore. Poiché sono simili ai negativi su pellicola, i formati raw da fotocamera sono anche noti come "negativi digitali". Il vantaggio dei formati grezzi è il maggiore controllo artistico per l'utente finale. L'utente può regolare vari intervalli di parametri in base ai requisiti come bilanciamento del bianco, mappatura dei toni, riduzione del rumore, nitidezza e così via. D'altra parte, il file raw della fotocamera deve essere elaborato per qualsiasi utilizzo tramite qualsiasi software o tramite un convertitore.

Poiché non era disponibile un formato standard per i file raw da fotocamera, ha creato molteplici problemi per l'utente finale. Questi problemi sono stati affrontati da Adobe e hanno definito un formato non proprietario per i file raw da fotocamera. Il formato è noto come Digital Negative o DNG. DNG può essere utilizzato da un'ampia gamma di hardware e software per l'elaborazione di file grezzi. Inoltre, DNG può essere utilizzato anche come formato intermedio per la memorizzazione di immagini catturate originariamente da fotocamere dotate di formati raw proprietari.

### Specifiche del formato file DNG

In questa sezione descriveremo il formato DNG come un'estensione di TIFF 6.0.

* **Estensioni file**: DNG utilizza le estensioni “.DNG” o “.TIF”.
* **Alberi SubIFD**: DNG non supporta catene SubIFD, invece DNG consiglia l'uso di alberi SubIFD come menzionato nelle specifiche TIFF-EP. La qualità e la risoluzione più elevate possono utilizzare NewSubFileType pari a 0, mentre le miniature di qualità ridotta devono utilizzare NewSubFileType uguale a 1. Si consiglia inoltre, sebbene non sia necessario, che il primo IFD abbia una miniatura di bassa qualità o risoluzione.
* **Ordine dei byte**: l'ordine dei byte deve essere supportato dai lettori DNG, anche per i file di un particolare modello di telecamera.
* **Pixel mascherati**: la maggior parte dei sensori della fotocamera calcola i pixel completamente mascherati sul bordo del sensore tramite la codifica del nero. Questi pixel possono essere inclusi o tagliati prima che l'immagine venga archiviata in formato DNG. Se i pixel mascherati non vengono tagliati, l'area di questi pixel deve essere menzionata nel tag ActiveArea. Le informazioni raccolte da questi pixel sul livello di codifica del nero devono essere utilizzate prima che i dati grezzi vengano archiviati o possono essere incluse nel file DNG che specifica il livello di nero.
* **Pixel difettosi**: prima di memorizzare i dati grezzi come DNG, i pixel difettosi dovrebbero essere esclusi.
* **Metadati**: i metadati possono essere inclusi in DNG in uno dei seguenti modi:
** Utilizzando tag di metadati TIFF-EP o EXIF
** Attraverso il tag di metadati IPTC (33723)
** Utilizzo del tag di metadati XMP (700)
* **Dati proprietari**: normalmente i fornitori includono dati proprietari in file non elaborati per essere utilizzati dai propri convertitori. DNG memorizza i propri dati proprietari in tag privati, IFD privati e in un MakerNote privato. I fornitori devono utilizzare i tag DNGPrivateData e MakerNoteSafety per assicurarsi che le applicazioni che modificano i file DNG conservino questi dati proprietari.

Di seguito sono riportate alcune importanti restrizioni ed estensioni dei tag TIFF.

**Bit per campione**

Sono supportati da 8 a 32 bit/campione. Deve esserci la stessa profondità per ogni campione quando SamplesPerPixel non è uguale a 1. Ma se BitsPerSample non è uguale a 8 o 16 o 32, allora i bit devono essere compressi in byte usando il FillOrder predefinito TIFF di 1 (big-endian).

**Compressione**

Sono supportati due valori di tag di compressione:

* Valore n. 1: dati non compressi.
* Valore n. 7: dati compressi JPEG, DCT JPEG di base o compressione JPEG senza perdita di dati.

**Interpretazione fotometrica**

I seguenti valori sono supportati solo per miniature e anteprime IFD:

* 1 = Nero è zero. Si presume che si trovi in uno spazio colore gamma 2.2.
* 2 = RGB. Si presume che si trovi nello spazio colore sRGB.
* 6 = YCbCr. Utilizzato per immagini di anteprima con codifica JPEG.

I seguenti valori sono supportati per l'IFD non elaborato e si presume siano lo spazio colore nativo della fotocamera:

* 32803 # CFA (matrice di filtri colorati).
* 34892 # LinearRaw.

**Orientamento**

Il tag di orientamento viene utilizzato per i browser di file in modo che possano eseguire la rotazione senza perdita di file DNG. I lettori DNG devono supportare tutti i possibili orientamenti, inclusi gli orientamenti speculari.

## Funzionalità nell'ultima versione di DNG

DNG versione 1.4 ottobre 2012 ha le seguenti funzionalità avanzate.

* Ritaglio utente predefinito
* Trasparenza
* Virgola mobile (HDR)
* Compressione con perdita
* Proxy

## Riferimenti ##

* [Specifiche DNG - Di Adobe](https://www.kronometric.org/phot/processing/DNG/dng_spec_1.4.0.0.pdf)
* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - Il formato di archivio pubblico per i dati grezzi della fotocamera digitale](https://helpx.adobe.com/photoshop/digital-negative.html)

