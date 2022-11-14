{
  "date" : "2021-06-29",
  "keywords" :[ "CUR", "estensione", "file", "formato", "immagine", "Bitmap indipendente dal dispositivo", "Formato file cursore", "Cursore", "Windows", "applicazione" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CUR - Formato file cursore",
  "description":"Scopri il formato di file CUR e le API che possono creare e aprire file CUR.",
  "linktitle" : "CUR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Che cos'è un file CUR? ##

Un file CUR è un formato di file cursore statico di Microsoft Windows. Fondamentalmente, sono immagini fisse identiche ai file ICO (icona) in ogni modo tranne l'estensione. Sia CUR che [ICO](/it/image/ico/) sono stabiliti sulla base della specifica Device-Independent Bitmap [DIB](/it/image/dib/) (Device-Independent Bitmap). L'impostazione predefinita, così come il cursore personalizzato come il puntatore del mouse di Windows per il sistema operativo Windows, sono archiviati nei file CUR. Può essere una freccia per l'uso normale, una clessidra rotante per mostrare i periodi di attesa o una I-bar per la modifica del testo. I file CUR vengono forniti con il pacchetto di installazione dei temi desktop personalizzati per garantire che il cursore di Windows corrisponda al tema desktop personalizzato.

## Specifica tecnica ##

I file CUR sono file di sistema binario che possono essere trovati su dispositivi che funzionano con il sistema operativo Microsoft Windows. Le immagini del puntatore CUR sono disponibili in diverse dimensioni standard come 16 × 16, 32 × 32, ecc. I file CUR sono molto simili ai file ICO; entrambi sono costituiti da piccole immagini fisse. Solo l'estensione dei file CUR e ICO è diversa. Inoltre, la spiegazione di un hotspot nell'intestazione del file CUR è distinta dal file ICO. L'hotspot interpreta l'offset dei pixel dall'angolo in alto a sinistra al punto in cui stai puntando il mouse. I sistemi Windows utilizzano ancora i file CUR, ma ora i cursori animati di solito hanno l'estensione del file ANI invece di CUR.

## Breve storia ##

Il file CUR è costituito dal file ICO. Il primo formato di file CUR è stato incorporato nel sistema operativo Windows 1.0 di Microsoft nel 1981 per semplificare l'utilizzo commerciale. Presto furono introdotti più cursori interattivi che consentivano agli utenti di modificare le preferenze del cursore dalle opzioni preinstallate disponibili. Tuttavia, è facile modificare un file CUR da soli anche se si hanno conoscenze tecniche insufficienti.


## Esempio CUR ##

I file CUR possono essere trovati in *C:\Windows\Cursors* :

{{< figure src="../cur.png" alt="Formato file CUR" >}}

