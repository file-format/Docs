{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo shp", "formato de arquivo shp", "o que é um arquivo shp", "arquivo", "exemplo shp", "extensão de arquivo shp", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHP - ESRI Shapefile",
  "description":"Saiba mais sobre o formato de arquivo SHP e APIs que podem criar e abrir arquivos SHP.",
  "linktitle" : "SHP",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo SHP?

SHP é a extensão de arquivo para um dos principais tipos de arquivo usados para representação do ESRI Shapefile. Ele representa informações geoespaciais na forma de dados vetoriais a serem usados por aplicativos de Sistemas de Informações Geográficas (GIS). O formato foi desenvolvido como especificações abertas para facilitar a interoperabilidade entre a ESRI e outros produtos de software.

## Representação de dados

Como mencionado, um formato shapefile descreve informações geoespaciais de um conjunto de dados como recursos vetoriais. Esses recursos de vetor incluem:

* pontos
* linhas
* polígonos

Esses recursos combinados podem representar quase qualquer tipo de forma, como poços de água, limites de países, pontos espaciais, fluxo de rios, lagos, etc. Cada recurso vetorial pode ter atributos que realmente definem o propósito desse recurso. Por exemplo, um shapefile contendo cidades de Los Angeles pode ter o nome da cidade e a temperatura como atributos que dão uma representação significativa aos dados espaciais.

## Arquivos associados

Um arquivo shp autônomo não pode ser usado por aplicativos de software para dar significado aos dados que ele contém. Para dar sentido às informações contidas em tal arquivo, um shapefile utiliza os seguintes arquivos obrigatórios adicionais.

* arquivo shx - arquivo de índice
* arquivo dbf - um arquivo dBASE que armazena todos os atributos das formas no arquivo principal
* arquivo prj - armazena as informações do projeto do arquivo

Também pode haver outros arquivos opcionais que compartilhem o mesmo nome do arquivo principal.

## Especificações de formato de arquivo SHP

As especificações abertas do shapefile estão disponíveis online na ESRI na forma de [Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) e elabora a estrutura geral do arquivo em detalhes. As informações no arquivo .shp principal consistem em cabeçalhos e registros. O cabeçalho do arquivo de tamanho fixo é seguido por registros de tamanho variável, onde cada registro é composto por um cabeçalho de registro de tamanho fixo seguido pelo conteúdo do registro de tamanho variável.

### Cabeçalho do arquivo SHP principal

O cabeçalho do arquivo principal começa no início do arquivo e tem 100 bytes de comprimento. A organização deste cabeçalho de arquivo principal junto com a posição do byte, valor, tipo e ordem dos bytes é mostrada na tabela a seguir.


|Bytes|Campo|Valor|Tipo|Ordem dos Bytes
---|---|---|---|---|
|0-3|Código do arquivo|9994|Inteiro|Big Endian
|4-23|Não utilizado|0|Inteiro|Big Endian
|24-27|Comprimento do arquivo|Comprimento do arquivo|Inteiro|Big Endian
|28-31|Versão|1000|Inteiro|Little Endian
|32-35|Tipo de forma|Tipo de forma|Inteiro|Little Endian
|36-67|Retângulo Delimitador Mínimo|Xmin, Ymin, Xmax e Ymax|double|Little Endian
|68-83|Caixa delimitadora|Zmin, Zmax|double|Little Endian
|84-99|Caixa delimitadora|Mmin, Mmax|double|

Deve-se notar que o valor do comprimento do arquivo é o comprimento total do arquivo em palavras de 16 bits que também inclui as cinquenta palavras de 16 bits que compõem o cabeçalho.

#### Tipos de forma

Os valores do campo de tipos de forma na tabela acima são os seguintes:


|Valor|Tipo de forma
---|---|
|0|Forma Nula
|1|Ponto
|3|Polilinha
|5|Polígono
|8|Multiponto
|11|Ponto Z
|13|PolyLineZ
|15|PolígonoZ
|18|MultipontoZ
|21|Ponto M
|23|PolyLineM
|25|PolígonoM
|28|MultipontoM
|31|MultiPatch

### Registros de dados ###

O cabeçalho do arquivo principal é seguido por registros de comprimento variável, onde cada registro consiste em um cabeçalho de registro de comprimento fixo seguido pelo conteúdo do registro de comprimento variável.

#### Cabeçalho do registro ####

O cabeçalho do registro contém informações sobre o número do registro e o comprimento do conteúdo do registro em um comprimento fixo de 8 bytes. A organização do cabeçalho do registro é mostrada a seguir:


|Bytes|Campo|Valor|Tipo|Ordem dos Bytes
---|---|---|---|---|
|0-3|Número do registro|Número do registro|Inteiro|Grande
|4-7|Tamanho do registro|Comprimento do registro|Inteiro|Grande

#### Conteúdo do Registro ####

O conteúdo de um registro de shapefile consiste em um tipo de forma seguido pelos dados geométricos dessa forma. Um tipo de forma de 0 representa uma forma nula que não possui dados geométricos para a forma. O comprimento do conteúdo do registro é reflexo das partes da forma e dos vértices. Vamos dar um exemplo do tipo Point Shape para elaborar como um registro contém informações sobre esse tipo de forma.

Um ponto representa uma determinada localização geográfica na ordem X,Y onde cada coordenada é representada por um valor de precisão dupla. A tabela a seguir mostra a disposição de um tipo de forma de ponto.


|Bytes|Tipo de forma|Valor|Tipo|Número|Ordem dos bytes
---|---|---|---|---|---|
|0-3|Tipo de forma|1|Inteiro|1|Pequeno
|4-11|X|X|duplo|1|Pequeno
|12-19|Y|Y|double|1|Pequeno

Exemplos de outros tipos de formas podem ser encontrados no documento de descrição técnica da ESRI.

## Referências ##

* [ESRI Shapefile Technical Description](http://www.esri.com/library/whitepapers/pdfs/shapefile.pdf) por ESRI

