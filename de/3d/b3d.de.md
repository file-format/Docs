{
  "date" : "2021-04-19",
"Schlüsselwörter": [ "Blitz3D", "b3d", "Datei", "Erweiterung", "Format", "Blitz3D-Spiele" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das B3D-Dateiformat; wird in Blitz3D-Spielen und APIs verwendet, die B3D-Dateien öffnen und erstellen können.",
  "title" :"B3D - Blitz3D-Entitätsmodelldatei",
  "linktitle" :"B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## Was ist eine B3D-Datei?
Eine Datei mit der Erweiterung .b3d ist eine von Blitz3D verwendete Modelldatei, die Videospielmodelle für Charaktere, Gebäude, Gelände und andere Objekte enthalten kann. Blitz3D ist eine Programmiersprache, die zum Erstellen von **Blitz3D-Spielen** verwendet wird. Blitz3D ist eine leistungsstarke, flexible und benutzerfreundliche Programmiersprache, die ausschließlich zum Schreiben von Videospielen entwickelt wurde. Die Entwickler können mit Blitz3D actiongeladene 3D-Spiele, 2D-Puzzler, Abenteuer, Rollenspiele und was auch immer erstellen. Der Blitz3D basiert auf der Programmiersprache BASIC; die auch einfach zu erlernen und zu verwenden ist. All diese Fakten machen Blitz ideal für Anfänger und erfahrene Programmierer gleichermaßen. Obwohl seine Funktionen als etwas antiquiert angesehen werden, als sie in den meisten modernen 3D-Engines zu finden sind, wird Blitz3D weiterhin von vielen Spieleprogrammierern weltweit verwendet.

## Kurze Geschichte von Blitz3D
Blitz3D wurde grundsätzlich im September 2001 für das Microsoft Windows-Betriebssystem veröffentlicht, um mit anderen ähnlichen Spieleentwicklungssprachen zu konkurrieren. Blitz3D war eine aktualisierte Version der früheren 2D-Engine BlitzBasic, die ihren Befehlssatz um eine API für eine DirectX 7-basierte 3D-Engine erweiterte. Die Benutzer von Blitz3D sollten auch BlitzMax vergleichen, eine spätere Engine von BlitzBasic. Der BlitzMax ist eine komplexe, aber leistungsfähigere Version von Blitz3D, die objektorientierte Programmiersprachen unterstützt. Es handelt sich um eine aktualisierte Grafik-API, die besser zu Unicode-Zeichen, OpenGL und zum Exportieren nach OSX und Linux statt nur nach Windows passt.

## B3D-Beispiel
Eine b3d-Datei, die 1 TEXS-Chunk, 1 BRUS-Chunk und 1 NODE-Chunk enthält, sieht folgendermaßen aus:

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
Ein einfaches, nicht animierendes und nicht texturiertes Netz sieht folgendermaßen aus:

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


## Verweise
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz-BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

