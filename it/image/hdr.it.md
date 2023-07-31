{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file HDR - Che cos'è un file immagine HDR?",
  "description":"Scopri il formato di file HDR e le API che possono creare e aprire file HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Che cos'è un file HDR?

Un file HDR è un formato di file immagine raster High Dynamic Range (HDR) per la memorizzazione di foto di fotocamere digitali. Consente agli editor di foto di migliorare il colore e la luminosità delle immagini digitali con una gamma dinamica limitata. Questa modifica può migliorare la luminosità intorno agli angoli, ottenendo un'immagine quasi naturale. I file HDR vengono generalmente salvati come immagini raster a 32 bit. Adobe Photoshop può creare e aprire file HDR.

I file HDR sono anche conosciuti come HDRI.

## Formato file HDR - Ulteriori informazioni

Il formato file HDR si basa sul formato file originale Radiance Picture (.pic). I dati dei pixel di un file HDR vengono generalmente archiviati non compressi, ma in alcuni casi vengono compressi utilizzando un semplice sistema di codifica della lunghezza di esecuzione.

### Struttura del file HDR

Un file immagine HDR è costituito dalle tre sezioni seguenti:

* **Intestazione:** Un file HDR è identificato dai primi byte nel file immagine, ad esempio "#?RADIANCE".
* **Stringa di risoluzione:** L'intestazione è seguita da una singola riga di risoluzione composta da 4 valori; un'etichetta X e Y, ciascuna seguita da un valore numerico intero. L'ordine di X e Y indica la rotazione. La combinazione di X e Y con valori positivi e negativi copre tutti i possibili orientamenti e rotazioni dell'immagine.
* **Dati pixel:** I dati pixel di un file HDR sono non compressi o compressi utilizzando una codifica della lunghezza di esecuzione standard.

## API HDR/HDRI open source

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - Libreria multipiattaforma super veloce a intestazione singola [C++](/it/programming/cpp/) per ottenere dimensioni e formato dell'immagine senza caricare/decodificare.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - Libreria Rust per ottenere dimensioni e formato dell'immagine senza caricare/decodificare. Supporta [.avif](/it/image/avif/), [.bmp](/it/image/bmp/), [.cur](/it/image/cur/), [.dds](/it/image/dds/), [. gif](/it/image/gif/), hdr (pic), [heic (heif)](/it/image/heic/), [.icns](/it/image/icns/), [.ico](/it/image/ico /), [.jp2](/it/image/jp2/), [jpeg (jpg)](/it/image/jpeg/), [jpx](/it/image/jpx/), ktx, [png](/it/image/png /), [psd](/it/image/psd/), qoi, tga, tiff (tif) e webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - Implementazione Java di HdrHistogram.

## Riferimenti

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [imageinfo](https://github.com/xiaozhuai/imageinfo)

