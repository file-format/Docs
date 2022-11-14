{
  "date" : "2022-02-16",
  "keywords" :[ "file obb", "formato file obb", "cos'è un file obb", "file", "esempio obb", "estensione file obb", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file OBB - File BLOB binario opaco Android",
  "description":"Scopri il formato di file OBB e le API che possono creare e aprire file OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Che cos'è un file OBB?

Un file OBB è un file di espansione che contiene dati aggiuntivi oltre al file Android [APK](/it/compression/apk/). Google Play Store non consente di avere un file APK Android con dimensioni superiori a 100 MB. Tuttavia, alcune applicazioni potrebbero richiedere l'hosting di grafica ad alta definizione, file multimediali o altre risorse di grandi dimensioni oltre ai file APK. È qui che entrano in gioco i tipi di file OBB. Google Play consente di allegare questi file di espansione come supplemento al file APK.

## Formato file OBB

I file OBB vengono salvati come file binari insieme ai file APK. Quando un APK accompagna i file OBB, Google Play ospita i file di espansione sul suo server e non viene addebitato alcun costo aggiuntivo allo sviluppatore. Questi file aggiuntivi vengono archiviati nella memoria condivisa del dispositivo su una scheda SD o una partizione montabile tramite USB quando l'app viene scaricata per l'installazione.

I file OBB vengono scaricati e installati al momento del download. Ma in alcuni casi, questi vengono scaricati per l'installazione quando l'applicazione viene eseguita per la prima volta.

### Dimensione massima del file OBB

Google Play Store ti consente di caricare file di espansione OBB di dimensioni fino a 2 GB. Si consiglia di caricare file di grandi dimensioni come file compressi [ZIP](/it/compression/zip/) per un caricamento efficiente via Internet.

Questi file di espansione possono essere ospitati come file di espansione principale **principale** per risorse aggiuntive richieste dall'app o come file di espansione patch opzionale destinato a piccoli aggiornamenti al file di espansione principale.

## Riferimenti

* [Sviluppatori Android - File di espansione](https://developer.android.com/google/play/expansion-files)

