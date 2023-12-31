{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo u3d", "formato de arquivo u3d", "o que é um arquivo u3d", "arquivo", "exemplo u3d", "extensão de arquivo u3d", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"U3D - Formato de arquivo 3D universal",
  "description":"Saiba mais sobre o formato de arquivo U3D e APIs que podem abrir e criar arquivos U3D.",
  "linktitle" : "U3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo U3D?

**U3D** (Universal 3D) é um formato de arquivo compactado e estrutura de dados para computação gráfica 3D. Ele contém informações do modelo 3D, como malhas de triângulos, iluminação, sombreamento, dados de movimento, linhas e pontos com cor e estrutura. O formato foi aceito como padrão [ECMA-363](https://www.ecma-international.org/publications-and-standards/standards/ecma-363/) em agosto de 2005. Documentos 3D [PDF](/pt/pdf/) suportam U3D incorporação de objetos e pode ser visualizado no Adobe Reader (versão 7 em diante).

O formato U3D foi desenvolvido tendo em vista o objetivo de estabelecer um padrão universal para armazenamento e troca de dados tridimensionais. No entanto, o formato encontra sua principal utilização na codificação para PDF 3D, em vez de ser usado como um formato de intercâmbio. O Acrobat 3D converte um tipo de arquivo 3D compatível para U3D ou PRC na conversão para PDF.

## Formato de arquivo U3D

Os arquivos U3D estão em formato de arquivo binário que passou por quatro edições, conforme descrito pelo documento de referência ECMA-363, resultando em atualização de especificações com cada edição. O arquivo PDF padrão ISO-32000 aceita U3D como anotação e tipo multimídia permitidos.

A primeira edição do U3D foi focada nas principais representações de propriedades gráficas 3D, como geometria, cor, texturas, iluminação, ossos e animação baseada em transformação. A segunda e terceira edições corrigiram algumas erratas na primeira edição, sendo a terceira versão o tipo mais utilizado em softwares industriais. A quarta edição fornece definições para primitivas de ordem superior (superfícies curvas). Especificações U3D estão disponíveis online para referência do usuário no site da ECMA.

### Tipos de dados em arquivos U3D

O arquivo binário conterá os seguintes tipos: U8, U16, U32, U64, I16, I32, F32, F64 e String.

* U8 : Um inteiro de 8 bits sem sinal
* U16 : Um inteiro de 16 bits sem sinal
* U32 : Um inteiro de 32 bits sem sinal
* U64 : Um inteiro de 64 bits sem sinal
* I16 : Um inteiro de 16 bits com sinal
* F32: Um flutuador de precisão simples IEEE.
* F64: Um flutuador de precisão dupla IEEE.
* String: Strings em um arquivo U3D começam com um inteiro não assinado de 16 bits que define o comprimento total dos caracteres na string. Strings são sempre processadas com distinção entre maiúsculas e minúsculas.

## Estrutura do arquivo U3D

Um arquivo U3D contém uma sequência de blocos. Existem 3 tipos diferentes de blocos em cada arquivo U3D.

* Bloco de cabeçalho de arquivo
* Bloco de Declaração
* Bloco de Continuação

O carregador determina o fim de um bloco se os dados desse bloco não forem necessários ou se um decodificador para esse tipo de bloco não estiver disponível.

{{< figure src="../u3d.png" alt="Formato de arquivo U3D" >}}

### Bloco de cabeçalho de arquivo
Um bloco de cabeçalho de arquivo contém informações de arquivo que são usadas pelo carregado para determinar como ler o arquivo.

### Bloco de declaração

Os blocos de declaração contêm informações sobre os objetos no arquivo. Os objetos em um bloco de declaração devem ser definidos.

### Bloco de Continuação

Informações adicionais para objetos declarados em um bloco de declaração são fornecidas no bloco de continuação. Cada Bloco de Continuação deve estar associado a um Bloco de Declaração.


## Referências ##

* [Formato de arquivo U3D - Wikipedia](https://en.wikipedia.org/wiki/Universal_3D)
* [Especificações de formato de arquivo ECMA U3D](https://ecma-international.org/publications-and-standards/standards/ecma-363/)

