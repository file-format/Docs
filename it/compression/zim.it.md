{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file ZIM - File archivio OpenZIM",
  "description":"Scopri il formato di file ZIM e le API che possono creare e aprire file ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Che cos'è un file ZIM? ##

I file con estensione .zim sono archivi creati per archiviare il contenuto Wiki offline. È considerato il formato di file aperto più adatto per la memorizzazione di Wikipedia su una USB. Memorizza i contenuti del sito in un formato compatto. Il suo nome deriva da "Zeno IMproved" che era il precedente formato di file Zeno. ZIM è gestito da [openZIM ](https://openzim.org/)project sponsorizzato da Wikimedia CH e supportato dalla Wikimedia Foundation. I file ZIM possono essere aperti da applicazioni come Kiwix e ZIMReader. Il progetto OpenZIM ha ospitato l'implementazione del formato di file ZIM su [Github](https://github.com/openzim) per il contributo della comunità OpenSource.

## Specifiche del formato file ZIM

Il formato file ZIM è stato sviluppato su [Zeno file format](https://openzim.org/wiki/Zeno_file_format) e non è compatibile con le versioni precedenti. Le specifiche del formato del file ZIM sono [disponibili online](https://openzim.org/wiki/ZIM_file_format) da openZIM per riferimento dello sviluppatore. OpenZIM ha fornito l'implementazione open source C++, [LibZim](https://openzim.org/wiki/Zimlib), per leggere e scrivere file ZIM.

Il formato file ZIM utilizza la compressione LZMA2 per rendere il contenuto compatto.

{{< figure src="../ZIM_File_Format.jpeg" alt="Formato file ZIM" >}}


### Intestazione ZIM

Un file ZIM inizia con un'intestazione che è all'offset 0. Tutti i costituenti sono basati su little-endian e tutti gli interi sono interi senza segno, ad esempio uint_16, uint_32, uint_64.

|Nome campo |Tipo| Compensazione| Lunghezza| Descrizione|
---|---|---|---|---|
|numero magico| intero| 0| 4| Numero magico per riconoscere il formato del file, deve essere 72173914 (0x44D495A)|
|MajorVersion| intero| 4| 2| Versione principale del formato file ZIM (5 o 6)|
|versione minore| intero| 6| 2| Versione secondaria del formato file ZIM|
|uuid| intero| 8| 16| ID univoco di questo file zim|
|articoloConte| intero| 24| 4| numero totale di articoli|
|conteggio cluster| intero| 28| 4| numero totale di cluster|
|urlPtrPos| intero| 32| 8| posizione dell'elenco di puntatori di directory ordinato per URL|
|titoloPtrPos| intero| 40| 8| posizione dell'elenco puntatori di directory ordinato per Titolo|
|clusterPtrPos| intero| 48| 8| posizione dell'elenco dei puntatori del cluster|
|mimeListPos| intero| 56| 8| posizione dell'elenco dei tipi MIME (anche dimensione dell'intestazione)|
|pagina principale| intero| 64| 4| pagina principale o 0xffffffff se nessuna pagina principale|
|pagina layout| intero| 68| 4| pagina di layout o 0xffffffffff se nessuna pagina di layout|
|checksumPos| intero| 72| 8| puntatore al checksum md5 di questo file senza il checksum stesso. Questo punta sempre 16 byte prima della fine del file.|

## Riferimenti ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

