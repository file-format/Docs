{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"File VPK - Formato file pacchetto applicazione PlayStation Vita",
  "description":"Scopri il formato di file VPK e le API che possono creare e aprire file VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Che cos'è un file VPK?

Un file con estensione .vpk è un file di pacchetto di archivio compresso utilizzato per installare app di terze parti sulla console di gioco Sony PlayStation Vita. Questi file possono essere installati solo sul jailbreak Vita PlayStation di HENkaku che ha consentito a PS Vita e PSTV di utilizzare contenuti personalizzati creati dall'utente. Un file di archivio VPK contiene tutti i contenuti che compongono il gioco, comprese immagini come file [PNG](/it/image/png/), file di impostazione come [.bin](/it/disc-and-media/bin/) e qualsiasi configurazione in formato file [XML](/it/web/xml/).

## Formato file VPK

I file VPK vengono salvati su disco come archivi [ZIP](/it/compression/zip/) compressi standard. Questi possono contenere più cartelle e altri file associati per le app di terze parti da installare su Vita Gaming Console. Per visualizzare il contenuto del file del pacchetto VPK, rinomina la sua estensione da .vpu a .zip ed estrai il contenuto utilizzando le utilità di decompressione standard come WinZip o WinRAR.

Valvesoftware dispone di informazioni dettagliate sul [formato file VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) a cui è possibile fare riferimento dal punto di vista dello sviluppatore.

## Come installare i file VPK?

I file VPK possono essere installati dall'utilità della riga di comando VPK.exe. Sul sistema operativo Windows, i file possono essere eliminati sul file vpk.exe che restituisce un \*.vpk contenente tutti i file compressi. In alternativa, lo strumento della riga di comando può essere utilizzato come segue.

### Crea VPK e aggiungi file

```
vpk <dirname>
```

### Estrai file VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Visualizzatore VPK

* [Visualizzatore VPK VRF](https://github.com/SteamDatabase/ValveResourceFormat)

## Riferimenti

* [Formato file VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [File VPK](https://developer.valvesoftware.com/wiki/VPK)

