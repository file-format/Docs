{
  "date" : "2020-03-16",
  "keywords" :[ "Arquivo STL", "Formato", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo STL e APIs que podem criar e abrir arquivos STL.",
  "title" :"Formato de arquivo STL",
  "linktitle" : "STL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## O que é arquivo STL?

STL, abreviatura de estereolitrografia, é um formato de arquivo intercambiável que representa a geometria tridimensional da superfície. O formato de arquivo encontra seu uso em vários campos, como prototipagem rápida, impressão 3D e fabricação assistida por computador. Representa uma superfície como uma série de pequenos triângulos, conhecidos como facetas, onde cada faceta é descrita por uma direção perpendicular e três pontos representando os vértices do triângulo. Os dados resultantes são usados por aplicativos para determinar a seção transversal da forma 3D a ser construída pelo fabber. Não há informações disponíveis no formato de arquivo STL para representação de cor, textura ou outros atributos comuns do modelo [CAD](/pt/cad/).

## Breve história ##

O desenvolvimento do formato de arquivo STL remonta a 1987. Foi desenvolvido pela 3D Systems para uso em impressoras 3D comerciais. Uma versão revisada do formato de arquivo STL, conhecido como STL 2.0, foi proposta em 2009 com atualizações no formato de arquivo.

## Especificações de formato de arquivo ##

Um arquivo STL representa uma geometria de superfície usando facetas. As facetas definem a superfície de um objeto 3D e são identificadas exclusivamente por uma unidade normal, que é uma linha perpendicular ao triângulo com comprimento de 1,0 e por três vértices. Há um total de 12 números armazenados para cada faceta como Normal e cada vértice é especificado por três coordenadas cada. O arquivo StL não contém nenhuma informação de escala; as coordenadas estão em unidades arbitrárias.

As especificações do formato de arquivo STL podem ser examinadas a partir de dois aspectos.

### Orientação das Facetas ###

A orientação de uma faceta é determinada pela direção da unidade normal e pela ordem na qual os vértices são listados. A orientação das facetas é especificada de duas maneiras, como segue:

* A direção do normal é para fora
* Os vértices são listados no sentido anti-horário de fora, obedecendo à regra da mão direita.

### Regra de vértice para vértice ###

De acordo com essa regra, cada triângulo compartilha dois vértices com cada um de seus triângulos adjacentes. Assim, um vértice de um triângulo não pode estar ao lado de outro triângulo.

## Formatos de arquivo ##

STL está disponível em ASCII, bem como representações binárias para formato de arquivo compacto.

### Formato STL ASCII ###

A versão ASCII do formato de arquivo STL é escrita em ASCII simples. No entanto, devido ao seu grande tamanho, o formato do arquivo não é selecionado como formato preferencial para uso. A sintaxe de um arquivo ASCII STL é a seguinte:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
As palavras em negrito representam palavras-chave que devem estar sempre em minúsculas. Símbolos em itálico são variáveis que devem ser substituídas por valores especificados pelo usuário. Os dados numéricos nas linhas **facet normal** e **vertex** são floats de precisão simples, por exemplo, 1,23456E+789. Uma coordenada **facetada normal** pode ter um sinal de menos à esquerda; uma coordenada de **vértice** não pode.

### Formato binário STL ###

O formato binário usa a representação numérica de inteiro e ponto flutuante IEEE. O formato do arquivo é representado da seguinte forma:

|Campo|Informações|
---|---|
|Cabeçalho|80 caracteres|
|Número de Triângulos|Inteiro sem sinal little endian de 4 bytes|
|Dados para cada triângulo|12 números de ponto flutuante de 32 bits|

Uma visão mais elaborada do formato do arquivo é mostrada abaixo.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## Referências ##

* [O formato STL](http://www.fabbers.com/tech/STL_Format)
* [STL - pela Wikipedia](https://en.wikipedia.org/wiki/STL_(file_format))

