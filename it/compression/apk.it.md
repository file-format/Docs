{
  "date" : "2019-10-11",
  "keywords" :[ "file apk", "formato file apk", "cos'è un file apk", "file", "esempio apk", "estensione file apk", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - Che cos'è un file APK?",
  "description":"Scopri cos'è un file APK e le API che possono creare e aprire file APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## Che cos'è un file APK?

Un file con estensione .apk è un file dell'app Google Android che viene utilizzato per installare app (applicazioni) sui dispositivi Android. Viene creato come file eseguibile utilizzando l'IDE ufficiale di Google Android Studio e viene caricato su Google Play Store per essere scaricato e installato dagli utenti finali. I file APK possono essere generati e resi disponibili per l'installazione manuale anche prima della pubblicazione su Google Play Store. Questo aiuta a testare la funzionalità e il comportamento del file del pacchetto APK generato. Pertanto, è necessario essere sicuri che il file APK provenga da una fonte attendibile e non contenga malware.

## Formato file APK

I file APK sono compressi nel formato di file [ZIP](/it/compression/zip/) che può essere aperto con qualsiasi software di apertura di file ZIP. L'estensione .apk di tale file può essere rinominata in .zip e aprire il file in qualsiasi applicazione ZIP o estrarne il contenuto.

## Contenuto del pacchetto APK

Un unico file APK contiene tutti i file necessari per la sua installazione ed esecuzione. Un file APK, se estratto con un'applicazione ZIP, contiene i seguenti file e cartelle.

* `META-INF/`: Directory che contiene il file manifest, la firma e un elenco di risorse nell'archivio
* `lib/`: Directory contenente codice compilato relativo a piattaforme specifiche come armeabi-v7a, x86, arm64-v8a, ecc.
* `res/`: Directory contenente risorse non compilate come immagini
* `assets/`: Directory contenente gli asset delle applicazioni, che possono essere recuperati da AssetManager.
* `androidManifest.xml`: contiene il nome, le informazioni sulla versione e il contenuto del file APK
* `classes.dex`: queste sono classi Java compilate che possono essere eseguite su macchine virtuali Dalvik e da Android Runtime
* `resources.arsc`: file di risorse compilato come stringhe

## Come installare il file APK sul dispositivo Android?

Per installare un file APK sui tuoi dispositivi Android, è possibile utilizzare i seguenti passaggi.

1. Scarica l'APK utilizzando il browser web
2. Toccalo: dovresti quindi essere in grado di vederlo in download nella barra in alto del tuo dispositivo
3. Una volta scaricato, apri Download, tocca il file APK e tocca Sì quando richiesto.

Seguendo questi passaggi verrà avviata l'installazione dell'app sul tuo dispositivo.

## Riferimenti

* [Formato file APK](https://en.wikipedia.org/wiki/Android_application_package)

