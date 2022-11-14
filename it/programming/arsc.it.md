{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc", "cos'è un file arsc", "come aprire il file arsc", "estensione", "file", "file arsc", "formato file arsc", "estensione file arsc" ,"Esempio di file arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - File della tabella delle risorse del pacchetto Android",
  "description":"Scopri il formato di file ARSC e le API che possono creare e aprire file ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Che cos'è un file ARSC?

Un file ARSC è un file di tabella delle risorse Android che contiene l'elenco delle risorse dell'applicazione in un formato tabella. Contiene informazioni come nomi di risorse, proprietà e ID. I file ARSC fanno parte dei pacchetti APK utilizzati per installare queste app Android. Tutte le risorse come immagini, layout, stili e stringhe, in un'applicazione Android vengono convertite in file binari quando viene generato il file APK. Allo stesso modo viene generato anche il file ARSC, contenente l'elenco di tutte le risorse compilate del programma e i loro ID.

## Formato file ARSC

I file con estensione .arsc sono file binari generati dopo che il compilatore, come ANT (Eclipse) o Gradle (AS), ha compilato il codice dell'applicazione Android per produrre il file [APK](/it/compression/apk/). Puoi estrarre il file APK utilizzando qualsiasi utilità di archiviazione come WinZip per visualizzarne il contenuto, che sono i file di classe java compilati, ad esempio classes.dex. Oltre a questi, contiene anche questo file ARSC che contiene meta-informazioni su:

* I nodi XML
* Gli attributi
* Gli ID risorsa

Le risorse in un file APK vengono riferite dagli ID risorsa, mentre gli attributi vengono risolti in un valore in fase di esecuzione. Lo strumento Android aapt raccoglie tutte le risorse definite nei file in fase di compilazione e assegna loro ID risorsa. Dopo che gli identificatori sono stati assegnati alle risorse compilate, viene generato un file R.java dal codice sorgente e da resources.arsc.

## Riferimenti

* [Struttura della tabella delle risorse binarie](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

