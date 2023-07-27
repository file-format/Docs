{
  "date" : "2019-12-12",
  "keywords" :[ "FBX", "arquivo", "extensão", "formato", "formato de arquivo 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo FBX e APIs que podem criá-los e abri-los.",
  "title" :"FBX - Formato de arquivo 3D FilmBox",
  "linktitle" : "FBX",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo FBX?

FBX, FilmBox, é um formato de arquivo 3D popular que foi originalmente desenvolvido por Kaydara para MotionBuilder. Foi adquirido pela Autodesk Inc em 2006 e agora é um dos principais formatos de troca 3D usados por muitas ferramentas 3D. O FBX está disponível em formato de arquivo binário e ASCII. O formato foi estabelecido para fornecer interoperabilidade entre aplicativos de criação de conteúdo digital. Existem muitas ferramentas disponíveis para conversão de/para o formato de arquivo FBX.

## Formato de arquivo FBX - Mais informações

O FBX é um formato proprietário e as especificações sobre seu formato de arquivo binário não estão disponíveis oficialmente. Um SDK C++ FBX é fornecido pela Autodesk para leitura, gravação e conversão de/para arquivo FBX. Um script de importação e exportação Python para FBX também está disponível no software Blender que não usa o SDK do FBX.

### Estrutura de arquivo baseada em texto

A estrutura de arquivos baseada em texto é uma estrutura de árvore documentada com identificadores claramente nomeados. Consiste em uma lista aninhada de nós organizados em hierarquia onde cada nó possui:

* Um identificador NodeType (nome da classe)
* Uma tupla de propriedades associadas a ela, os elementos da tupla são os tipos de dados primitivos usuais: ##float, integer, string## etc.
* Uma lista que contém nós no mesmo formato (recursivamente).

Estes podem ser representados logicamente da seguinte forma:

```
NodeType: SomeProperty0a, SomeProperty0b, ... , {

 NestedNodeType1 : SomeProperty1a, ...
 NestedNodeType2 : SomeProperty2a, ... , {
 ... Sub-scope
 }

 ...
}
```

Alguns dos nós padrão são definidos como lista implícita onde cada item consiste em uma lista aninhada. Qualquer aplicação que pretenda acessar a geometria do FBX, deve analisar esses conteúdos e dar-lhes um significado útil. Um exemplo de arquivo FBX baseado em texto é dado abaixo:

```
; FBX ...
; Copyright (C) 1997-2008 ...
; All rights reserved.
; ----------------------------------------------------
FBXHeaderExtension: {
    FBXHeaderVersion: 1003
    FBXVersion: 6000
    CurrentCameraResolution: {
        CameraName: "Model::Producer Perspective"
        CameraResolutionMode: "Window Size"
        CameraResolutionW: 1
        CameraResolutionH: 1
}
    CreationTimeStamp: {
    ...
}
}
;Object definitions
;------------------------------------------------------------------
Definitions: {
    Count: 2
    ObjectType: "Model" {
    Count: 2
}
}
...
```

## Estrutura de arquivos binários de arquivos FBX

Conforme declarado anteriormente, as especificações de formato de arquivo FBX não estão disponíveis publicamente para FBX. Como o Blender Foundation implementa o formato de arquivo FBX sem usar o SDK fornecido pela empresa, alguns dos detalhes sobre o formato de arquivo binário estão [disponíveis](https://code.blender.org/2013/08/fbx-binary-file-format-specification/) como parte de sua implementação.

A estrutura dos arquivos binários segue a seguinte ordem:

* Cabeçalho
* Registro de objetos
* Rodapé

### Cabeçalho FBX

As informações do cabeçalho do arquivo são compostas por 27 bytes.

* Bytes 0 - 20: Kaydara FBX Binary \x00 (arquivo mágico, com 2 espaços no final, depois um terminador NULL).
* Bytes 21 - 22: [0x1A, 0x00]## (desconhecido, mas todos os arquivos observados mostram esses bytes).
* Bytes 23 - 26: unsigned int, o número da versão. 7300 para a versão 7.3, por exemplo.

### Registro de objeto ###

O cabeçalho é seguido por um registro de objeto que é um registro de nó completo com nome vazio e lista de propriedades vazia. Ele recursivamente contém toda a formação do arquivo.

### Rodapé ###

A seção FBX Footer fica no final do arquivo cujo conteúdo é desconhecido.

## Formatos de Gravação ##

Os registros em um arquivo FBX são categorizados como:

* Registros de nós
* Registros de propriedade

### Formato de registro do nó ###

Cada Node Record Format é nomeado e possui o seguinte layout de memória.


|Tamanho (Bytes)|Tipo de Data|Nome
--- | ---|---|
|4|UInt32|EndOffset
|4|UInt32|NumProperties
|4|UInt32|PropertyListLen
|1|UInt8|NameLen
|NomeComprimento|caracter|Nome
|?|?|Propriedade[n], onde n = 0:PropertyListLen
|Opcional| |
|?|?|Lista Aninhada
|13|uint8[]|Null-Record

Onde:

* `EndOffset` é a distância do início do arquivo até o final do registro do nó (ou seja, o primeiro byte do que vem a seguir). Isso pode ser usado para pular facilmente registros desconhecidos ou não necessários.
* `NumProperties` é o número de propriedades na tupla de valor associada ao nó. Uma lista aninhada como último elemento não é contada como propriedade.
* `PropertyListLen` é o comprimento da lista de propriedades. Este é o tamanho necessário para armazenar as propriedades ##NumProperties##, que depende do tipo de dados das propriedades.
* `NameLen` é o comprimento do nome do objeto, em caracteres. O único caso em que isso é 0 parece ser o nível superior das listas.
* `Name` é o nome do objeto. Não há terminação zero.
* `Property[n]` é a enésima propriedade. Para o formato, consulte a propriedade da seção Formato do Registro. As propriedades são escritas sequencialmente e sem preenchimento.
* `NestedList` é a lista aninhada, cuja presença é indicada por um registro NULL no final.

A existência de uma entrada de lista aninhada pode ser determinada verificando se há bytes restantes até que EndOffset seja alcançado. Nesse caso, o próximo registro do objeto deve ser lido diretamente após a última propriedade. O registro do objeto segue então 13 bytes zero, que se combinam com o EndOffset. O propósito ou requisito da entrada NULL não é conhecido e pode apontar para algum recurso de formato.

### Formato de registro de propriedade ###

Um registro de propriedade contém detalhes sobre as propriedades que fazem parte do Node. Um registro de propriedade tem o seguinte layout de memória:


|Tamanho (Bytes)|Tipo de Dados|Nome
--- | --- | ---
|1|char|TypeCode
|?|?|Dados

TypeCode representam códigos de caracteres que são ordenados em grupos que requerem tratamento semelhante. TypeCodes pode ser categorizado nos seguintes tipos e TypeCode pode ser um dos códigos de caracteres entre esses tipos.

#### Tipos primitivos ####

```
Y: 2 byte signed Integer
C: 1 bit boolean (1: true, 0: false) encoded as the LSB of a 1 Byte value.
I: 4 byte signed Integer
F: 4 byte single-precision IEEE 754 number
D: 8 byte double-precision IEEE 754 number
L: 8 byte signed Integer
```

Os dados no registro de tipo escalar primitivo são exatamente a representação binária do valor, em ordem de byte little-endian.

#### Tipos de matrizes ####

```
f: Array of 4 byte single-precision IEEE 754 number
d: Array of 8 byte double-precision IEEE 754 number
l: Array of 8 byte signed Integer
i: Array of 4 byte signed Integer
b: Array of 1 byte Booleans (always 0 or 1)
```

O Data for Array Type é mais complexo e está na estrutura a seguir.


|Tamanho (Bytes)|Tipo de Dados|Nome
--- | --- | ---
|4|Uint32|ArrayLength
|4|Uint32|Codificação
|4|Uint32|Comprimento compactado
|?|?|Conteúdo

### Tipos especiais ###

A seguir estão os TypeCodes de tipos especiais.

```
S: String
R: raw binary data
```

Ambos os TypeCodes são representados da seguinte forma:


|Tamanho (Bytes)|Tipo de Dados|Nome
--- | --- | ---
|4|Uin32|Comprimento
|Comprimento| |

A string não é terminada em zero e pode conter caracteres \0 (isso é realmente usado em algumas propriedades do FBX).

## Referências ##

* [FBX - O SDK da Autodesk](https://help.autodesk.com/view/FBX/2017/ENU/)
* [Especificações de formato de arquivo binário FBX](https://code.blender.org/2013/08/fbx-binary-file-format-specification/)
* [FBX - Wikipedia](https://en.wikipedia.org/wiki/FBX#File_format)

