{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file VHDX e le API che possono creare e aprire file VHDX.",
  "title" :"Formato file VHDX - Che cos'è un file VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Che cos'è un file VHDX?

Un file VHDX è un file immagine disco nel formato file Virtual Hard Disk v2. Contiene un intero sistema operativo che può essere caricato e utilizzato come qualsiasi normale macchina per testare software o eseguire software che richiede un sistema operativo specifico. Un VHDX, nonostante sia un'immagine disco completa, viene archiviato in un unico file. Software per macchine virtuali come Parallels Desktop, Windows Virtual Machine e Virtual Box possono caricare e aprire l'immagine del disco.

Il file VHDX può essere convertito in [VHD](/it/disc-and-media/vhd/) con Hyper-V Manager o in [VDI](/it/disc-and-media/vdi/) con VirtualBox.

## Formato file VHDX - Ulteriori informazioni

I dettagli del formato file VHDX sono completamente documentati e disponibili online come [Specifiche del formato file VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) su Documentazione Microsoft. È un'estensione del formato VHD e include funzionalità avanzate. Il formato file VHDX fornisce funzionalità aggiuntive disponibili nei livelli di file del disco rigido virtuale e del disco rigido virtuale. È più ottimizzato e offre risultati migliori per la configurazione e le capacità dell'hardware di archiviazione. È possibile aprire i file VHDX

### Supporto per dischi rigidi virtuali in VHDX

Supporta tre tipi di dischi rigidi virtuali.

1. **Disco rigido virtuale fisso**: disco rigido virtuale con dimensione dati fissa allocata. La dimensione del disco rigido virtuale non cambia con l'aggiunta o la rimozione di dati.

1. **Disco rigido virtuale dinamico** - Disco rigido virtuale con dimensione disco dinamica. La sua dimensione è in qualsiasi momento grande quanto i dati effettivi scritti su di esso e i metadati. La sua dimensione del file aumenta dinamicamente man mano che i dati vengono aggiunti o rimossi da esso.

1. **Differenza del disco rigido virtuale**: rappresenta la corrente del disco rigido virtuale come un insieme di blocchi modificati rispetto a un file del disco rigido virtuale padre.

## Riferimenti

* [Specifiche del formato file VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - di Wikipedia](https://en.wikipedia.org/wiki/VHD_(file_format))

