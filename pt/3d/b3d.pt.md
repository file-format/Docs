{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aprenda sobre o formato de arquivo B3D; usado em jogos blitz3d e APIs que podem abrir e criar arquivos B3D.",
  "title" :"B3D - Arquivo de modelo de entidade Blitz3D",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## O que é um arquivo B3D?

Um arquivo com extensão .b3d é um arquivo de modelo usado pelo Blitz3D que pode conter modelos de videogame para personagens, edifícios, terrenos e outros objetos. O Blitz3D é uma linguagem de programação usada para criar **jogos blitz3d**. Blitz3D é uma linguagem de programação poderosa, flexível e fácil de usar projetada com o único propósito de escrever videogames. Os desenvolvedores podem criar jogos 3D cheios de ação, quebra-cabeças 2D, aventuras, RPGS, qualquer coisa usando o Blitz3D.

O Blitz3D é baseado na linguagem de programação BASIC; que também é fácil de aprender e usar. Todos esses fatos estão tornando o Blitz ideal para iniciantes e programadores mais experientes. Embora seus recursos sejam considerados um pouco antiquados do que os encontrados na maioria dos mecanismos 3D modernos, o Blitz3D continua sendo usado por muitos programadores de jogos em todo o mundo.

## Breve história do Blitz3D

O Blitz3D foi lançado basicamente para o sistema operacional Microsoft Windows em setembro de 2001, para competir com outras linguagens de desenvolvimento de jogos semelhantes. Blitz3D foi uma versão atualizada sobre o mecanismo 2D anterior BlitzBasic, que estendeu seu conjunto de comandos com a adição de uma API para um mecanismo 3D baseado em DirectX 7. Os usuários do Blitz3D também devem comparar o BlitzMax, que é um mecanismo posterior do BlitzBasic. O BlitzMax é uma versão complexa, porém mais poderosa, do Blitz3D, que suporta linguagens de programação orientadas a objetos. É uma API gráfica atualizada para se adequar melhor aos caracteres Unicode, OpenGL e exportar para OSX e Linux em vez de apenas Windows.

## Exemplo B3D
Um arquivo b3d que contém 1 pedaço TEXS, 1 pedaço BRUS e 1 pedaço NODE, terá a seguinte aparência:

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
Uma malha simples, sem animação e sem textura ficará assim:

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


## Referências
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

