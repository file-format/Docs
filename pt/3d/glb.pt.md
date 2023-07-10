{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","arquivo", "formato", "tipo de arquivo", "extensão","o que é um arquivo GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Saiba mais sobre o formato de arquivo GLB e APIs que podem abrir e criar arquivos GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## O que é um arquivo GLB?

GLB é a representação em formato de arquivo binário de modelos 3D salvos no formato de transmissão GL ([glTF](/pt/3d/gltf/)). Informações sobre modelos 3D como hierarquia de nós, câmeras, materiais, animações e malhas em formato binário. Esse formato binário armazena o ativo glTF (JSON, .bin e imagens) em um blob binário. Também evita o problema de aumento no tamanho do arquivo que acontece no caso de glTF. O formato de arquivo GLB resulta em tamanhos de arquivo compactos, carregamento rápido, representação de cena 3D completa e extensibilidade para desenvolvimento posterior. O formato usa model/gltf-binary como tipo MIME.

## Formato de arquivo GLB - Mais informações

Os métodos de entrega de conteúdo usados pelo glTF resultam em processamento extra para decodificar os dados binários codificados em base 64 e também aumentam o tamanho do arquivo em 33%. Esses métodos de entrega, que contribuíram para a formação do formato de arquivo GLB, incluem:

* glTF JSON aponta para dados binários externos (geometria, quadros-chave, skins) e imagens.
* glTF JSON incorpora dados binários codificados em base64 e imagens em linha usando URIs de dados.

O GLB como formato de contêiner foi introduzido como formato de arquivo binário para representação do ativo glTF em um blob binário para evitar os problemas causados pelo glTF. O formato de arquivo GLB [especificações](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) deve ser referido para qualquer implementação de leitor/gravador do mesmo para desenvolvimento de aplicativos .

## Estrutura do arquivo GLB

O formato de arquivo GLB é baseado em little endian e sua estrutura mostra que ele contém:

* Um preâmbulo de 12 bytes, intitulado cabeçalho.
* Um ou mais blocos que contêm conteúdo JSON e dados binários.

#### Cabeçalho GLB

O cabeçalho do formato de arquivo GLB consiste em três entradas de 4 bytes:

* uint32 magic - magic é igual a 0x46546C67. É uma cadeia de caracteres ASCII glTF e pode ser usada para identificar dados como glTF binário
* versão uint32 - indica a versão do formato do contêiner Binary glTF
* uin32 length - o comprimento total do Binary glTF, incluindo Header e todos os pedaços em bytes

#### Pedaços

Cada pedaço em um arquivo GLB tem a seguinte estrutura:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - comprimento de chunkData em bytes
* `chunkType` - indica indica o tipo de pedaço
* `chunkData` - carga binária do pedaço

onde os tipos de pedaços são:

|# |Tipo de Bloco|ASCII|Descrição|Ocorrências
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Conteúdo JSON estruturado|1
|2.|0x004E4942|BIN|Buffer binário|0 ou 1

O início e o fim de cada bloco devem ser alinhados ao limite de 4 bytes e o preenchimento deve ser usado para essa finalidade.

##### Conteúdo JSON estruturado

Esta deve ser a primeira parte do ativo Binary glTF e permite que a implementação recupere progressivamente recursos de partes subsequentes. Isso também fornece a capacidade de ler apenas um subconjunto selecionado de recursos de um ativo Binary glTF, como o LOD mais grosseiro de uma malha. Para atender aos requisitos de alinhamento, esse pedaço deve ser preenchido com caracteres de espaço à direita (0x20).

##### Buffer binário #####

Este pedaço contém a carga binária para geometria, quadros-chave de animação, capas e imagens. Ele deve ser a segunda parte do ativo Binary glTF e deve ser preenchido com zeros à direita (0x00) para atender aos requisitos de alinhamento.

## Referências ##

* [Especificações de formato de arquivo GLB - Khronos](/pt/3D/GLTF/)

