{
  "date" : "2021-06-24",
  "keywords" :[ "PART", "parziale", "estensione", "file", "formato", "web", "scaricato" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PART - File parzialmente scaricato",
  "description":"Scopri il formato di file PART e le API che possono creare e aprire file PART.",
  "linktitle" : "PART",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Che cos'è un file PART? ##

Un file di parte o un'estensione .part è un file parzialmente scaricato. Viene utilizzato quando i download sono in corso o sono stati interrotti a causa di qualsiasi problema, dando al download manager l'opportunità di riprendere il download quando possibile.
Ciò significa che il browser, come Firefox o programmi di trasferimento file come eMule, eMule plus, FlashGet, ecc. memorizza una parte del file, chiamata Part file, mentre è in corso il download sul tuo dispositivo. Questo file di parte ti mostrerà se il download è in corso o è stato interrotto prima del completamento. Non solo questo, ma il file PART memorizza tutti i dati fino al completamento del download, motivo per cui alcuni di essi possono essere ripresi in seguito se si desidera riavviare il download.

## Formato file PARTE ##

There are few browsers that break large download files into smaller downloads and assign each portion a .part extension. These files can be seen in the “Download” folder. Once the download is finished, the browser will combine all the PART files to give a final downloaded file. For example, while downloading a file from Firefox, the download manager will store the data being downloaded in a PART file and replaces the name with certain characters, and add a .part extension at the end, such as **doodle.or** becomes **JKzMn.or.part**. After completion, Firefox will remove the .part extension and the file will be ready to launch.
