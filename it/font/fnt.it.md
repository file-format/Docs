{
  "date" : "2020-08-20",
  "keywords" :[ "file fnt", "formato file fnt", "cos'è un file fnt", "file", "esempio fnt", "estensione file fnt", "estensione", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - File dei caratteri di Windows",
  "description":"Scopri il formato di file FNT e le API che possono creare e aprire file FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Che cos'è un file FNT?

Un file con estensione .fnt è un file di font che memorizza informazioni generiche sui font sui sistemi operativi Windows. I file FNT sono stati per lo più sostituiti dai formati di file TrueType (.TTF) e OpenType (.OTF) e al momento è un formato di file di caratteri obsoleto. Questi file possono memorizzare un singolo valutatore o un carattere vettoriale. Tutti i driver di dispositivo supportano i caratteri di Windows 2.x. Tuttavia, non tutti i driver di dispositivo
supportare la versione di Windows 3.0.

## Formato file FNT

I file FNT sono in grado di memorizzare un singolo carattere raster o vettoriale. I formati vettoriali sono usati più frequentemente da GDI rispetto al raster in cui il glifo di ogni carta è definito utilizzando una piccola bitmap. L'ovvia ragione per la sostituzione di .fnt con .ttf e .otf è il suo formato raster.

### Intestazione del file dei caratteri
L'inizio di entrambi i file di font raster e vettoriali è comune, seguito da informazioni diverse per ogni tipo di file. L'intestazione del file di carattere include per Windows 3.0 include sei nuovi campi come segue che sono impostati su zero per garantire la compatibilità con le versioni future di Windows.

* dFlag
* dfAspace
* dfBspazio
* dfCspace
* dfColorPointer
* dfRiservato1

Per informazioni dettagliate sulle intestazioni per Windows 3.0 e 2.0, visitare il [Microsoft KnowledgeBase Archive](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Riferimenti
* [Formato file font](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Come installare o rimuovere un font in Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8-7613-c76f-88d043b334b8)

