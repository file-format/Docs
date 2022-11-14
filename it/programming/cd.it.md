{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "cos'è un file cd", "come aprire un file cd", "estensione", "file", "file cd", "formato file cd", "estensione file cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - File diagramma di classe di Visual Studio",
  "description":"Scopri il formato di file CD e le API che possono creare e aprire file CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Che cos'è un file CD?

Un file con estensione .cd è un file del diagramma di classe di Visual Studio che fornisce informazioni sulla struttura e sulla relazione tra tutte le classi nella soluzione corrente. Una soluzione di Visual Studio (rappresentata da [.sln](/it/programming/sln/)) può contenere uno o più progetti, ognuno con più classi diverse. Il file del diagramma di classe può essere generato facendo clic con il pulsante destro del mouse sul progetto e selezionando l'opzione diagramma di classe.

## Formato file diagramma di classe (.cd) - Ulteriori informazioni

Un file del diagramma di classe viene salvato in un formato di file XML standard che rappresenta le classi in un progetto come nodi XML. Se Visual Studio non è disponibile, questi file di diagramma di classe possono essere aperti in qualsiasi programma applicativo che supporta l'apertura di file XML.

### Come aggiungere diagrammi di classe al progetto di Visual Studio

In Visual Studio, apri la soluzione/progetto per cui vuoi aggiungere il diagramma di classe. Quindi, fai clic con il pulsante destro del mouse sul nodo del progetto e scegli Aggiungi > Nuovo elemento. In alternativa, premi CTRL+MAIUSC+A.

* Si apre la finestra di dialogo Aggiungi nuovo elemento.

* Espandi Elementi comuni > Generale, quindi seleziona Diagramma classi dall'elenco dei modelli. Per i progetti Visual C++, cerca nella categoria Utilità per trovare il modello Diagramma classi.

### Esporta diagrammi di classe (CD) in immagini

Visual Studio consente di convertire/esportare diagrammi di classe in immagini come [PNG](/it/image/png/), [JPEG](/it/image/jpeg/) e [BMP](/it/image/bmp/). Questi file di diagrammi di classe esportati possono essere utilizzati per scopi di documentazione e conservazione dei record del pacchetto di dati tecnici (TDP). Per convertire un diagramma di classe in un'immagine, è possibile usare i passaggi seguenti da Microsoft Visual Studio.

1. Apri il file del diagramma di classe (.cd).
1. Dal menu Diagramma di classe o dal menu di scelta rapida della superficie del diagramma, scegliere Esporta diagramma come immagine.
1. Selezionare un diagramma.
1. Seleziona il formato che desideri.
1. Scegliere Esporta per terminare l'esportazione.

## Riferimenti

* [Classi di progettazione in Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

