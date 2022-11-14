{
  "date" : "2021-08-30",
  "keywords" :[ "file ipa", "formato file ipa", "cos'è un file ipa", "file", "esempio ipa", "estensione file ipa", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file IPA e le API che possono creare e aprire file IPA.",
  "title" :"IPA - File del pacchetto dell'applicazione iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Che cos'è un file IPA?
Un file con estensione .ipa appartiene a iOS ed è noto come file del pacchetto dell'applicazione. Si tratta di un file di archivio (compresso utilizzando [ZIP](/it/compression/zip/) compression) che memorizza un'applicazione iOS, ma tale applicazione può essere installata solo su dispositivi iOS o MacOS basati su ARM, come iPad, iPhone o Ipod touch. Principalmente, per installare i file IPA è possibile utilizzare iTunes, Apple Configurator 2 o qualsiasi software di terze parti.

## Formato file IPA
Gli sviluppatori IOS che stanno sviluppando le app utilizzando Apple Xcode hanno familiarità con i file IPA perché hanno bisogno di impacchettare le loro app sviluppate come file IPA per testare la distribuzione dell'app store. Sebbene i file IPA siano noti per essere installati come app iOS, puoi anche decomprimerli per visualizzare i dati dell'app contenuti. Poiché un file IPA contiene solo un binario per l'architettura ARM dei telefoni cellulari e non contiene un binario per l'architettura x86, molti file .ipa non possono essere installati su iPhone Simulator.
### Struttura di un file .ipa
L'esempio seguente mostra la struttura di un IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Quanto sopra è una struttura integrata che iTunes e App Store possono riconoscere. Secondo questa struttura:
- La directory Payload contiene tutti i dati dell'app.
- Il file iTunes Artwork è un'immagine PNG di 512×512 pixel, contenente l'icona dell'app per la visualizzazione in iTunes e l'app App Store sull'iPad.
- iTunesMetadata.plist contiene varie informazioni, che vanno dal nome e ID dello sviluppatore, alle informazioni sul copyright, all'identificatore del bundle, al nome dell'app, al genere, alla data di rilascio, alla data di acquisto, ecc.
- La cartella META-INF contiene solo metadati su quale programma è stato utilizzato per creare l'IPA.


## Riferimenti

* [.ipa - di Wikipedia](https://en.wikipedia.org/wiki/.ipa)


