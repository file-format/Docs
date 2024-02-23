{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Scopri il formato file MCR e le API che possono creare e aprire file MCR.",
  "title": "MCR: formato file regionale di Minecraft",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-itr"
}
},
  "lastmod": "2022-12-14"
}

## Cos'è un file MCR?

Il formato file Minecraft MCR è un formato dati utilizzato da Minecraft per archiviare porzioni di terreno di un mondo Minecraft. Si basa sul formato NBT (Named Binary Tag), sviluppato dagli sviluppatori del popolare motore di gioco open source Minecraft Forge. Il tipo di file MCR è stato introdotto all'inizio e successivamente è stato sostituito da [MCA file format](/game/mca/).

## Formato file MCR

Il formato file MCR è strutturato come una serie di tag binari denominati, ciascuno dei quali contiene un tipo specifico di dati. Il tag di livello superiore è il tag Livello, che contiene tutti i dati per un singolo livello di gioco. All'interno del tag Level, ci sono molti altri tag con nome che memorizzano diversi tipi di dati, come il tag Data, che memorizza informazioni sul mondo di gioco, e i tag Entities e TileEntities, che memorizzano dati sul mondo di gioco. rispettivamente oggetti di gioco ed entità di tessere nel mondo.

## Cosa c'è nel formato file MCR?

Nel formato file Minecraft MCR, una regione è un'area di blocco 32x32 del mondo di gioco. Il formato MCR divide il mondo di gioco in regioni per gestire i dati in modo più efficiente e consentire un caricamento e un salvataggio più rapidi dei livelli di gioco. Ogni regione è archiviata in un file separato e il formato file MCR utilizza un sistema di coordinate per identificare la posizione di ciascuna regione all'interno del mondo di gioco. Le coordinate di una regione sono determinate dalle coordinate del blocco dell'angolo inferiore sinistro della regione. Ad esempio, una regione con coordinate (-1,0) si troverebbe una regione a sinistra e zero regioni più in basso rispetto all'origine del mondo di gioco.

## Specifiche del formato file MCR

Le specifiche del formato file MCR sono disponibili pubblicamente. Le specifiche per il formato NBT, su cui si basa il formato MCR, sono disponibili sul sito web di Minecraft Forge. Inoltre, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) contiene anche informazioni dettagliate sul formato file MCR, inclusa la sua struttura e i vari tipi di dati che supporta.

### Dati compressi nei file MCR

Il formato file Minecraft MCR supporta la compressione. Il formato file MCR è basato su [NBT format](https://minecraft.fandom.com/wiki/NBT_format) che consente di archiviare i dati in un formato compresso. Ciò aiuta a ridurre le dimensioni dei file MCR e a renderli più efficienti da trasferire e archiviare. Questa è una caratteristica importante del formato file MCR, poiché consente ai giocatori di condividere grandi dati sul terreno di Minecraft World con altri.

## Riferimenti

* [Editor mondiale per Minecraft](https://www.mcedit.net/)

* [Informazioni su Minecraft](https://www.minecraft.net/)

* [Formato file regionale](https://minecraft.fandom.com/wiki/Region_file_format)

* [Formato NBT](https://minecraft.fandom.com/wiki/NBT_format)


