{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "estensione", "file", "format", "Fumetti", "Fumetti File Format", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file CBC e le API che possono creare e aprire file CBC.",
  "title" :"CBC - Formato file raccolta fumetti",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## Che cos'è un file CBC?

Un file con estensione .cbc è una raccolta compressa di file di fumetti per eBook e contiene file [CBZ](/it/ebook/cbz/) e [CBR](/it/ebook/cbr/). È utilizzato da [Calibre](https://calibre-ebook.com/), un'applicazione di conversione di eBook, che è un gestore di e-book open source multipiattaforma e ti consente di gestire i tuoi ebook e convertirli in diversi formati . Un file CBC contiene un file .txt, comics.txt, che elenca altri file che fanno parte dell'archivio. Sono disponibili diverse applicazioni online in grado di convertire file CBC in [AZW3](/it/ebook/azw3), [EPUB](/it/ebook/epub/), [FB2](/it/ebook/fb2/), [MOBI](/it/ebook/ mobi/), [TXT](/it/elaborazione testi/txt/), [PDF](/it/pdf/) e altri formati di file popolari.

## Formato file CBC

I file CBC sono archivi compressi che contengono CBZ, CBR e un file di testo per elencare i contenuti. Il file di testo comics.txt è codificato in UTF8 e contiene un elenco dei file CBC che devono essere utilizzati dai lettori per organizzare le proprie raccolte. Un file CBC ha solitamente diversi attributi che consentono l'organizzazione di questa raccolta come Comic, Categoria, Editore, Serie, Edizione e Artista.

I contenuti di un file CBC di esempio sono elencati come segue:

* comics.txt - File di testo che contiene un elenco di file CBR e CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* File CBZ

dove il file comics.txt elenca i contenuti come segue:

* 1.cbz: primo capitolo
* 2.cbz: secondo capitolo
* 3.cbz: terzo capitolo

I lettori elaborano il file comics.txt e generano il sommario in base ai dati forniti.

## Riferimenti

* [Calibre](https://calibre-ebook.com/)

