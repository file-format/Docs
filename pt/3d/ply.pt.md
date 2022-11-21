{
  "date" : "2019-12-12",
  "keywords" :[ "PLY", "arquivo", "extensão", "formato", "formato de arquivo 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo PLY e APIs que podem criar e abrir arquivos PLY.",
  "title" :"PLY - Formato de arquivo 3D de polígono",
  "linktitle" : "PLY",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PLY?

PLY, Polygon File Format, representa o formato de arquivo 3D que armazena objetos gráficos descritos como uma coleção de polígonos. O objetivo desse formato de arquivo era estabelecer um tipo de arquivo simples e fácil que fosse geral o suficiente para ser útil para uma ampla variedade de modelos. O formato de arquivo PLY vem como formato ASCII e binário para armazenamento compacto e para salvamento e carregamento rápidos. O formato do arquivo é usado por diferentes aplicativos que oferecem suporte para leitura de arquivos 3D.

Objetos em formato PLY são descritos por uma coleção de vértices, faces e outros elementos, juntamente com propriedades como cor e direção normal que podem ser anexadas a esses elementos. Outras propriedades que também podem ser armazenadas com o objeto incluem:

* Superfícies normais
* coordenadas de textura
*transparência
* confiança de dados de intervalo
* propriedades para a frente e o verso de um polígono

Um objeto representado pelo formato PLY pode ser o resultado de várias fontes, como objetos digitalizados à mão, objetos poligonais de aplicativos de modelagem, dados de alcance, triângulos de cubos de marcha, dados de terreno e modelos de radiosidade.

## Breve história

O formato PLY foi desenvolvido na década de 1990 por Greg Turk e outros no laboratório gráfico de Stanford e é por isso que também é conhecido como Stanford Triangle Format. O formato do arquivo tem a versão 1.0 desde então e nenhuma outra modificação foi feita.

## Formato de arquivo PLY

Um objeto PLY simples consiste em uma coleção de elementos para representação do objeto. Ele consiste em uma lista de (x,y,z) triplos de um vértice e uma lista de faces que são realmente índices na lista de vértices. Vértices e faces são dois exemplos de elementos e a maioria do arquivo PLY consiste nesses dois elementos. Novas propriedades também podem ser criadas e anexadas aos elementos de um objeto, mas elas devem ser adicionadas de forma que os programas antigos não quebrem quando essas novas propriedades são encontradas. Tais propriedades também podem ser descartadas lendo aplicativos. Além disso, novos elementos podem ser criados e propriedades podem ser definidas com este elemento também.

### Estrutura do arquivo

A estrutura de arquivo de um formato de arquivo PLY é a seguinte:

|Campo
---|
|Cabeçalho do arquivo
|Lista de vértices
|Lista de rostos
|Lista de outros elementos

#### Estrutura de exemplo

Usaremos o seguinte exemplo abaixo em nossa discussão subsequente para várias partes de um formato de arquivo PLY.

```
ply
format ascii 1.0           { ascii/binary, format version number }
comment made by Greg Turk  { comments keyword specified, like all lines }
comment this file is a cube
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
element face 6             { there are 6 "face" elements in the file }
property list uchar int vertex_index { "vertex_indices" is a list of ints }
end_header                 { delimits the end of the header }
0 0 0                      { start of vertex list }
0 0 1
0 1 1
0 1 0
1 0 0
1 0 1
1 1 1
1 1 0
4 0 1 2 3                  { start of face list }
4 7 6 5 4
4 0 4 5 1
4 1 5 6 2
4 2 6 7 3
4 3 7 4 0
```

#### Cabeçalho do arquivo

O cabeçalho do formato de arquivo PLY consiste em texto ASCII tanto para o formato ASCII quanto para o formato binário. O início e o fim da seção de cabeçalho são identificados pelas palavras-chave ply e end-header. O início do cabeçalho tem a palavra mágica ply que é usada para reconhecimento do formato de arquivo PLY pelos leitores. A próxima linha mostra o número da versão para este arquivo. Os comentários em um formato de arquivo PLY começam com a palavra-chave comment no início de cada linha de comentário.

#### Palavra-chave do elemento

A palavra-chave element então diz o que está dentro do arquivo. Ele é seguido por propriedades para esse tipo de elemento específico, onde cada propriedade tem seu tipo de propriedade e ordem especificada conforme mostrado abaixo:

```
element vertex 8           { define "vertex" element, 8 of them in file }
property float x           { vertex contains float "x" coordinate }
property float y           { y coordinate is also a vertex property }
property float z           { z coordinate, too }
```

Neste exemplo em particular, o elemento de vértice específico possui 3 propriedades do tipo float com sua ordem especificada.

#### Tipos de tipos de dados

Existem dois tipos de tipos de dados que uma propriedade pode ter.

`Scalar`: Os tipos de dados escalares são mostrados abaixo:

|#Nome|#Tipo|#Número de Bytes
|caracter|caractere|1
|uchar|caractere sem sinal|1
|curto|curto inteiro|2
|curto|inteiro curto não assinado|2
|int|Inteiro|4
|uint|inteiro sem sinal|4
|float|float de precisão simples|4
|double|float de precisão dupla|8

`List`: Existe uma forma especial de definições de propriedades que usa o tipo de dados de lista. Um exemplo disso é do arquivo cubo acima:

`lista de propriedades uchar int vertex_index`

Isso significa que a propriedade "vertex_index" contém primeiro um caractere não assinado informando quantos índices a propriedade contém, seguido por uma lista contendo esses números inteiros. Cada inteiro nesta lista de comprimento variável é um índice para um vértice.

## Referências ##

* [Formato de arquivo PLY](http://paulbourke.net/dataformats/ply/)
* [PLY - Por Wikipedia](https://en.wikipedia.org/wiki/PLY_(file_format))

