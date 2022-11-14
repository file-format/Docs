{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato di file B3D; utilizzato nei giochi blitz3d e nelle API che possono aprire e creare file B3D.",
  "title" :"B3D - File modello entità Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Che cos'è un file B3D?

Un file con estensione .b3d è un file modello utilizzato da Blitz3D che può contenere modelli di videogiochi per personaggi, edifici, terreno e altri oggetti. Blitz3D è un linguaggio di programmazione utilizzato per creare **giochi blitz3d**. Blitz3D è un linguaggio di programmazione potente, flessibile e facile da usare progettato al solo scopo di scrivere videogiochi. Gli sviluppatori possono creare giochi 3D ricchi di azione, puzzle 2D, avventure, giochi di ruolo, qualsiasi cosa semplicemente utilizzando Blitz3D.

Il Blitz3D è basato sul linguaggio di programmazione BASIC; che è anche facile da imparare e da usare. Tutti questi fatti stanno rendendo Blitz l'ideale sia per i principianti che per i programmatori più esperti. Sebbene le sue caratteristiche siano considerate in qualche modo antiquate rispetto a quelle che si trovano nella maggior parte dei moderni motori 3D, Blitz3D continua ad essere utilizzato da molti programmatori di giochi in tutto il mondo.

## Breve storia di Blitz3D

Il Blitz3D è stato sostanzialmente rilasciato per il sistema operativo Microsoft Windows nel settembre 2001, per competere con altri linguaggi di sviluppo di giochi simili. Blitz3D era una versione aggiornata rispetto al precedente motore 2D BlitzBasic, che estendeva il suo set di comandi con l'aggiunta di un'API per un motore 3D basato su DirectX 7. Gli utenti di Blitz3D dovrebbero anche confrontare BlitzMax, che è un motore successivo di BlitzBasic. BlitzMax è una versione complessa ma più potente di Blitz3D, che supporta linguaggi di programmazione orientati agli oggetti. È un'API grafica aggiornata per adattarsi meglio ai caratteri Unicode, OpenGL e all'esportazione su OSX e Linux anziché solo su Windows.

## Esempio B3D
Un file b3d che contiene 1 pezzo TEXS, 1 pezzo BRUS e 1 pezzo NODE, sarà simile al seguente:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
Una mesh semplice, non animata e non strutturata sarà simile a questa:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## Riferimenti
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASE](https://en.wikipedia.org/wiki/Blitz_BASIC)

