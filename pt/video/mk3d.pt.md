{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo MK3D",
  "keywords" :[ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", "StereoMode", "video", "file", "format" ],
  "description":"Saiba mais sobre o formato de arquivo MK3D para vídeos 3D estereoscópicos criados pela Matroska e APIs que podem criar e abrir arquivos MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## O que é um arquivo MK3D? ##

Os arquivos MK3D pertencem à família de formatos de vídeo Matroska. Esses arquivos são, na verdade, vídeos ** 3D estereoscópicos** criados usando o formato Matroska 3D. O arquivo MKV Container usa o valor de um campo StereoMode para definir o tipo de material de vídeo 3D estereoscópico. Um valor StereoMode também está disponível para exibir os vídeos 3D estéreo antigos separando as cores ciano e vermelho (AnaGlyph)

## Detalhes técnicos ##
Os vídeos 3D podem ser compactados das duas maneiras a seguir:

- Faixa separada para cada olho.
- Combine cada rastreamento ocular em uma única faixa.

O contêiner de arquivo MKV oferece suporte a ambos.

Para os vídeos de trilha única que são mais fáceis com o material 3D dentro deles, você deve definir o campo **StereoMode** que decide se os planos são montados na trilha mono ou combinada esquerda direita. Você pode usar um dos seguintes valores de campo StereoMode:

|Valor | Descrição |
|---|---|
|0| mono|
|1| lado a lado (o olho esquerdo é o primeiro)|
|2| de cima para baixo (o olho direito é o primeiro)|
|3| de cima para baixo (o olho esquerdo é o primeiro)|
|4| checkboard (à direita é o primeiro)|
|5| checkboard (esquerda é a primeira)|
|6| linha intercalada (direita é a primeira)|
|7| linha intercalada (esquerda é a primeira)|
|8| coluna intercalada (direita é a primeira)|
|9| coluna intercalada (esquerda é a primeira)|
|10| anaglifo (ciano/vermelho)|
|11| lado a lado (o olho direito é o primeiro)|
|12| anaglifo (verde/magenta)|
|13| ambos os olhos entrelaçados em um Bloco (o olho esquerdo é o primeiro) (modo sequencial de campo)|
|14| ambos os olhos entrelaçados em um Bloco (o olho direito é o primeiro) (modo sequencial de campo)|

Para as várias faixas, o contêiner MKV precisa decidir a funcionalidade de cada faixa separadamente. O **TrackOperation** com **TrackCombinePlanes** são usados para fazer o trabalho.


## Referências ##

- [Notas de especificação Matroska](https://www.matroska.org/technical/notes.html)
- [Suporte de contêiner de arquivo MKV para vídeo 3D estéreo e arquivos MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- arquivos/)

