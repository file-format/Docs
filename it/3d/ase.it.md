{
  "date" : "2021-01-22",
  "keywords" :[ "ASE", "file", "formato", "tipo di file", "estensione", "cos'è un file ASE?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file ASE e le API che possono aprire e creare file ASE.",
  "title" :"ASE - File di esportazione della scena ASCII Autodesk",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-01-22"
}

## Che cos'è un file ASE?

Un file con estensione .ase è un formato di file Autodesk ASCII Scene Export che è una rappresentazione ASCII di una scena, contenente informazioni 2D o 3D durante l'esportazione dei dati della scena utilizzando Autodesk. Autodesk fornisce opzioni per includere i componenti della scena durante l'esportazione dei dati della scena. È possibile includere la definizione della mesh insieme alle informazioni sui vertici e sulla faccia, la descrizione del materiale, la trasformazione dei dati di animazione per gli oggetti, la definizione della mesh completa di ogni n fotogrammi, i dati di animazione per le telecamere e le luci e le impostazioni dei giunti IK.

## Formato file ASE - Ulteriori informazioni

I file ASE sono file di testo archiviati in formato ASCII che possono essere aperti in qualsiasi editor di testo. Un file ASE può contenere i seguenti tipi di informazioni fornite da Autodesk.

### Opzioni di output

* `Definizione mesh` - Esporta la definizione di ogni mesh, comprese le informazioni sui vertici e sulle facce per gli oggetti geometrici. Inoltre, l'attivazione di questa opzione abilita gli elementi nella casella di gruppo Opzioni mesh, descritti di seguito.
* `Materiali` - Include la descrizione del materiale. Se un materiale non è assegnato a un oggetto, il suo colore wireframe viene esportato. Tutti i livelli di un albero materiale sono inclusi, quindi questo può produrre molto testo.
* `Transform Animation Keys` - Include i dati di animazione di trasformazione per gli oggetti. Se l'oggetto è una telecamera o un riflettore target, questo includerà i dati di animazione target.
* `Mesh animato` - Esporta una definizione di mesh completa di ogni n frame. La frequenza è specificata dallo spinner Controller Output, descritto di seguito. Ciascun blocco contiene le stesse informazioni specificate nella casella di gruppo Opzioni mesh, descritta di seguito. L'attivazione può comportare un file di grandi dimensioni, anche per scene di piccole dimensioni.
* `Impostazioni telecamera/luce animate` - Esporta i dati di animazione per telecamere e luci, come colore, intensità, decadimento, distorsione mappa e così via. Emette un blocco ogni n fotogrammi, come specificato dallo spinner Controller Output.
* `Giunti cinematici inversi` - Esporta le impostazioni del giunto IK nel ramo Gerarchia.

### Tipi di oggetti

Gli elementi qui consentono di specificare quale categoria di oggetto si desidera includere nell'output. Puoi includere oggetti geometrici, forme, fotocamere, luci e oggetti ausiliari.

* Geometrico
* Forme
* Macchine fotografiche
* Luci
* Aiutanti

### Opzioni mesh

* `Normali mesh` - Esporta le normali di faccia e vertice. Viene elencata per prima la normale della faccia, seguita dalle normali dei tre vertici che supportano la faccia. Attivando questo si ottiene un file molto più grande.
* `Coordinate di mappatura`: esporta un elenco di vertici e facce di mappatura, in base alle strutture TVert e TVFace descritte nel 3ds Max Software Development Kit. Se un oggetto utilizza la mappatura dei volti, viene esportato un elenco di mappe dei volti contenente le coordinate UVW per ciascuna faccia.
* `Colori dei vertici` - Esporta i colori dei vertici.

### Uscita controller

* `Usa chiavi` - Esporta i valori delle chiavi. Se il controller non utilizza le chiavi, viene utilizzato il metodo Force Sample. Nel caso dei controller di trasformazione, l'opzione Usa chiavi funziona solo se tutti i controller di trasformazione sono Linear/TCB o Bezier. Se una delle tracce di trasformazione utilizza un diverso tipo di controller, il metodo Force Sample viene utilizzato per tutte le tracce di trasformazione.
* `Forza campioni`: campiona i valori del controller in base alla frequenza specificata in Frames per Sample Controller.

## Riferimenti

* [Autodesk - Esportazione in ASCII](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2020/ENU/3DSMax-Data-Exchange/files/GUID-98B2388D -A3A7-4096-8E81-888A3F9D6069-htm.html)

