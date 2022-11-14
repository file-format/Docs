{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "file", "estensione", "formato", "eBook", "Libro digitale" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file LRF e le API che possono creare e aprire file LRF.",
  "title" :"Formato file LRF - Un file lettore portatile Sony",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## Che cos'è un file LRF?

Un file con estensione .lrf è un file Broad Band eBook (BBeB) che contiene i dati per un Sony BBeB, inclusi testo, immagini e dati di impaginazione. Il file viene salvato in un formato binario compresso che contiene un'intestazione, un numero specificato di oggetti e un indice di oggetti. I file LRF e LRX racchiudono i due formati di libri BBeB disponibili. I file LRF non sono crittografati e possono essere compilati da file [LRX](/it/ebook/lrf/). I file LRF possono essere convertiti da diversi altri tipi di file inclusi PDF e HTML. Se il tuo computer non riesce ad aprire il file LRF, probabilmente non hai installato il software per aprire o modificare i file LRF. I programmi che possono aprire file LRF sono Calibre, BookDesigner, Makelrf e Canon Book Creator per Windows, Calibre per Linux, Calibre e Sony Reader per Macintosh.

## Breve storia

Il tipo di file LRF è innanzitutto associato a Line Rider da [inXile entertainment](https://en.wikipedia.org/wiki/InXile_Entertainment). Il Line Rider è un giocattolo di fisica di Internet ed è stato inventato nel settembre 2006 da uno studente universitario sloveno, Boštjan Čadež. Gli eReader eBook del marchio Sony (come i lettori Sony PRS-500 e Sony Librie) utilizzano l'estensione del file LRF per i loro documenti e testi. Questo tipo di file proprietario è ora obsoleto, così come i relativi file LRS e LRX. Questi tre tipi di file costituivano l'eBook BroadBand (BBeB) che è stato interrotto nel 2010 quando Sony ha iniziato a vendere i propri ebook nel formato EPUB.

## Formato file LRF

Specifiche dettagliate del formato file LRF sono disponibili su [archivio web](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat). Un file LRF è composto da:
* un'intestazione
* un certo numero di oggetti
* un indice di oggetto.

Tutti questi valori sono nell'ordine Intel (LSB first).

### Intestazione LRF

|Offset (esadecimale) |Dimensione (byte) |Nome/significato| Valore di esempio|
---|---|---|---|
|0 |8| Firma LRF| 4C 00 52 00 46 00 00 00 = "LRF" in Unicode|
|8 |2| versione?| 999 nella maggior parte dei file|
|A |2| "Psuedo-crittografia" |byte chiave 48|
|0C |4| RootObjectID| 0x0044|
|10 |8| NumeroOggetti |342|
|18 |8| ObjectIndexOffset| 0x00093440|
|20 |4| sconosciuto| 0|
|24 |1| Bandiere| (16 - da dietro a davanti, 1 = da davanti a dietro) 16|
|25 |1| sconosciuto |(imbottitura?) 0|
|26 |2| sconosciuto| 1600|
|28 |2| sconosciuto| (imbottitura?) 0|
|2A |2| Altezza?| 600|
|2C |2| Larghezza?| 800|
|2E |1| sconosciuto| 24|
|2F |1| sconosciuto |(imbottitura?) 0|
|30 |0x14| sconosciuto| zeri|
|44 |4| ID oggetto del solo oggetto PlaneStream (0x1E)| 0x0042|
|48 |4| sconosciuto |0x1536|
|4C |2| DimensioneComp.XML| 0x035C|


## Riferimenti

* [Formato file LRF](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - Di Wikipedia](https://en.wikipedia.org/wiki/BBeB)

