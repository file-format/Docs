{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "file", "formato", "estensione", "API", "Set di fogli AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - File set di fogli AutoCAD",
  "description" :"Ulteriori informazioni sul file .dst e sulle API che possono creare e aprire file DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Che cos'è un file DST?

Un file DST è un file AutoCAD che contiene associazioni e informazioni per la definizione di gruppi di fogli. Questi sono archiviati nella cartella di archiviazione dei gruppi di fogli di default, Gruppi di fogli di AutoCAD. I file DST non contengono i layout di disegno effettivi, ma fanno riferimento a questi dai file [DWG](/it/cad/dwg/) e [DWT](/it/cad/dwt/) selezionati associati a questi gruppi di fogli. Nell'ambiente di rete, tutti i membri del team dovrebbero avere accesso in rete a questi file associati. I file DST vengono salvati su disco nel formato di file [XML](/it/web/xml/).

## Formato file DST - Ulteriori informazioni

I file DST vengono creati con lo strumento AutoDesk Sheet Set Manager (SSM). Quando un membro del team accede a un file, il file DST viene aperto brevemente e quindi archiviato con le informazioni aggiornate. L'accesso simultaneo allo stesso file DST è gestito dallo strumento SSM che mostra l'icona di un lucchetto quando il file è in accesso.

In qualsiasi momento, lo stato del foglio può trovarsi in uno dei seguenti stati.

* Il foglio è disponibile per la modifica.
* Il foglio è bloccato.
* Il foglio è mancante o trovato in una posizione di cartella imprevista.

## Riferimenti

* [Informazioni sull'utilizzo dei set di fogli dell'ora legale](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-577D8EA0-85F2 -4829-B4F9-8CAD6F7AAACC-htm.html)
* [Ulteriori informazioni sui set di fogli](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-34D889BC-19AD- 4CD1-ADB1-F359D9B515FB-htm.html)
* [Mastering AutoCAD Sheet Sets](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

