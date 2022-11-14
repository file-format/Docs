{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file FZPZ - File di parti frizzanti",
  "description":"Scopri cos'è un file FZPZ e le API che possono creare e aprire file FZPZ.",
  "linktitle" : "FZPZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-20"
}

## Che cos'è un file FZPZ?

Un file FZPZ è un componente/parte utilizzato nella progettazione di un circuito elettronico creato con l'applicazione di progettazione e prototipazione di circuiti **Fritzing**. È un archivio compresso che contiene un file [FZP](/it/cad/fzp/) e quattro immagini [SVG](/it/image/svg/) che descrivono la parte complessiva di Fritzing. Il vantaggio dell'utilizzo di questi file è che gli utenti possono condividere i propri file FZPZ con ciascuno dal punto di vista della riutilizzabilità. La condivisione delle parti FZPZ aiuta a integrare le parti del circuito per creare progetti PCB più grandi in modo rapido.

## Formato file FZPZ - Ulteriori informazioni

I file FZPZ vengono salvati su disco come archivi [ZIP](/it/compression/zip/) compressi. È possibile rinominare l'estensione da .fzpz a .zip e utilizzare qualsiasi utilità di decompressione standard come WinZIP per estrarre i file dall'archivio.

### Informazioni sulla struttura del file FZPZ

Come accennato, un file FZPZ è un file di archivio che contiene file multipli per la rappresentazione di una parte utilizzata nel circuito stampato. La FZPZ contiene i seguenti file:

* `Quattro file SVG` - che rappresentano la breadboard, lo schema, il PCB e le immagini delle icone della parte
* `File FZP` - Un file XML che contiene informazioni sulle proprietà, sui connettori e sui bus della parte

I file sono generalmente denominati come segue.

* part.file.fzp
* svg.breadboard.file.svg
* svg.icon.file.svg
* svg.pbc.file.svg
* svg.schematic.file.svg

## Riferimenti ##

* [Nuove parti con estensione fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

