{
  "date" : "2021-08-13",
  "keywords" :[ "file sdi", "formato file sdi", "cos'è un file sdi", "file", "esempio sdi", "estensione file sdi", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file SDI e le API che possono creare e aprire file SDI.",
  "title" :"SDI - File immagine distribuzione sistema Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Che cos'è un file SDI?
Il file con estensione .sdi contiene un BLOB di caricamento, un BLOB di avvio e una parte BLOB; comunemente utilizzato da Windows Embedded Studio per creare dischi RAM o dischi di avvio per il caricamento e l'installazione di Windows. SDI è l'abbreviazione di System Deployment Image. Windows Embedded Studio è un programma utilizzato per creare immagini disco per Windows. In realtà questo programma contiene il programma SDI File Manager e uno strumento a riga di comando chiamato **sdimgr.exe**, entrambi possono essere utilizzati per distribuire, creare e modificare immagini SDI.

## Formato file SDI
Il formato di file SDI è ampiamente utilizzato per consentire l'uso di un disco virtuale per l'avvio di un sistema. Alcune versioni di Microsoft Windows abilitano l'**avvio dalla RAM**, che è importante per caricare un file SDI in memoria e quindi avviarlo da esso. Il formato di file SDI si abilita anche per l'avvio dalla rete utilizzando PXE (Preboot Execution Environment). Viene anche utilizzato per l'imaging del disco rigido.
### Sezioni di file SDI
Il file SDI stesso può essere suddiviso nelle seguenti sezioni:
- **Boot BLOB**: contiene il programma di avvio effettivo, STARTROM.COM. Questo è un analogo al settore di avvio di un disco rigido.
- **Load BLOB**: in genere contiene NTLDR e viene avviato dal BLOB di avvio.
- **Part BLOB**: contiene il runtime di avvio effettivo; include anche i file boot.ini e ntdetect.com che dovrebbero trovarsi nella directory principale del runtime.
- **Disk BLOB**: questa è un'immagine HDD piatta che inizia con un MBR. Viene utilizzato per l'imaging del disco rigido anziché per l'avvio. Inoltre, solo i BLOB su disco possono essere montati con le utilità di Microsoft.


## Riferimenti

* [Immagine di distribuzione del sistema - di Wikipedia](https://en.wikipedia.org/wiki/System_Deployment_Image)


